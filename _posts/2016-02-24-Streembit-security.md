---
layout: post
title: Streembit security
subtitle: Secure the communication for humans and Internet of Things devices
author: "T. Z. Pardi"
categories: article
---

A growing number of homes are being exposed to security threats via Internet of Things devices. The simplest and most common instances of this are the various Internet connected home monitoring video cameras and baby monitors; which often connect to RTMP servers run by companies with unknown security policies, or use the default user name “admin” with a blank password for authentication. It is no wonder there have already been hacking events where cyber criminals compromised [home video cameras](http://bit.ly/1vUmBLb) on the scale of thousands of devices.  
  Security must be the primary concern for Internet of Things applications. It is troubling that robust security was not taken into account for the majority of Internet of Things implementations. The data of IoT devices is being harvested in an automated fashion, but who has access to the data? What functions can a human or another machine execute on the IoT device? Is my office door  vulnerable to being opened by a former employee who is no longer allowed on the premise? Is the data being forwarded by the IoT device compromised at all on its way to the end-user? Or did this data even originate from the authorized device? Existing systems tend to use custom authorization, and access control schemes with domain specific login portals for user name and password based logins; instead of, for example, using open standards and robust Public Private Key Infrastructure based security.  
  Apart from these IoT and machine-to-machine security issues, I also explained  [previous post](http://streembit.github.io/2016-02-23-What-is-Streembit/) how the security and privacy of human-to-human communication is compromised by various political and infrastructural (i.e. centralized computing) issues. So how does Streembit provide users and devices with security and privacy?

#### Streembit security
The cornerstone of Streembit security is elliptic curve public/private key cryptography infrastructure (PPKI). PPKI allows the implementation of robust security. We use PPKI to identify the entities of the system (based on their public key and PPKI signature), perform authentication, and ensure data integrity (using cryptography signatures).  
  Using the public/private key cryptography infrastructure paves the way for the deployment of a robust, secure authentication and access control scheme. The parties are identified by their public key. The authenticity of messages and the identities of the actors are then verified using PPKI cryptography routines. Using a PPKI infrastructure based security scheme greatly simplifies the authentication, access control, and identity management aspects of Internet-of-Things security.  
  The elliptic curve cryptography (ECC) scheme is particularly suitable for IoT devices. The small footprint of ECC allows security modules to be implemented on embedded devices. ECDH is a trusted and proven key agreement protocol. Using the ECDSA digital signature algorithm ensures data integrity.  
  The system performs public/private key infrastructure based authentication and access control functions to securely connect machines to machines or machines to humans. The Streembit security module of the IoT device must generate at least one public/private key pair for each connected IoT device. Human users generate their ECC public/private key pair when they create their account. The actors of the system publish their public keys to the network, where each entity knows the public key of the other connected human or machine. The system identifies each of the entities by their ECC public key.  
  The collision resistant SHA-256 hash function is used to create a hash of data which can be signed using the private key to guarantee data integrity, as well as provide information about the originator of the data. To ensure data integrity the messages, control commands, event data, requests, and responses are signed with the ECC private key; the signature can be verified using ECDSA. To ensure integrity of data, each entity must sign all messages with their private key. The messages in the Streembit network are based on the following standards: JSON Web Token (JWT), JSON Web Encryption (JWE), and JSON Web Signature (JWS).

#### Streembit security implementation and design summary
The basic premises of the Streembit security are

* Human users and Internet of Things devices use public/private key (PPK) infrastructure and PPK cryptography functions to secure messages
* Each actor of the system must generate a public/private key pair. (Typically keys are generated prior to configuring the device and will be burned into the devices' firmware).
* The device or user publishes the public key to other users of the system.
* The data integrity and authenticity of the messages is guaranteed with PPK signatures.
* Each session between users is secured with strong symmetric cryptography keys.
* All messages between users are secured with 128-bit and 256-bit AES symmetric encryption/decryption.
* The system uses elliptic curve Diffie Hellman (ECDH) key exchange algorithms to facilitate the exchange of session keys.

#### Protecting the ECC public/private key pair
The ultimate issue of all applications, systems and devices that encrypt data is the protection of the cryptography symmetric key or the protection of private key of the public/private key pair. Similarly to the iPhone and PGP, which both use passcode to protect their keys, Streembit requires users have a passcode to protect their PPKI private key. The Streembit passcode that protects the user’s PPK key pair is relatively complex and it requires the following minimum number of iterations with a brute force attack: $$26^2 \times 10 \times 33 \times 95^4 \times 8! / 4! \approx 3.05 \times 10^{16}$$. That means 3,050,000,000,000  (3.05 trillion) times more iterations than the $$10^{4}$$ iterations is required to break the iPhone security. (Of course if the passcode is longer than 8-digit then the number of iterations is even more). Please note, this is related to protecting the PPKI key pair.  
  To protect real time communication, Streembit uses a randomly generated 256-bit AES session key and exchanged between peers with a randomly generated ECDH key pair. This means that real time communication, which is the main functionality of Streembit, is secure even from the brute force attacks of NSA super computers and large zombie computer clusters of cyber criminals.


#### Mitigate the risk of Sybil attacks
A known issue with regards to peer-to-peer (P2P) networks and their practical limitation is that they are frequently subject to Sybil attacks. This means that malicious parties can compromise the network by generating and controlling large numbers of shadow identities. A malicious node may present multiple fake identities to a peer-to-peer network in order to appear and function as several distinct nodes.  
  A Sybil attack is most effective on anonymous and reputation systems where if the malicious nodes outnumber the honest nodes the outcome of the application could be compromised. For example, on a file sharing network a successful horizontal Sybil attack allows the attacker to sniff most of the control messages, hijack the system, and deliver bogus content. Contrarily, Streembit facilitates communication between contacts that you know, such as your family members, teammates, and business partners. You are also aware of the location and identity of your Internet of Things device(s) you control via Streembit, lessening the likelihood of a Sybil attack. Malicious nodes, regardless of their weight and presence on the network, are unable to change the public keys of your contacts (as the public key is based on the cryptographically secured PPK infrastructure).  
  Additionally, Streembit introduces another layer of security, private networks. Using private networks, the public keys of the contacts are loaded to the seed nodes manually; mitigating further the risk of a Sybil attack as well as a Man-in-the-middle attack (MITM). A Sybil attack, which generally speaking is a serious security issue for P2P networks such as file sharing applications, is much less of a problem for the Streembit P2P system.

#### How secure the cryptography of Streembit?
Both 128-bit and 256-bit AES symmetric encryption, the cryptography schemes of the messages in the Streembit network, are safe from any brute force attacks. [Bruce Schneier](https://www.schneier.com/blog/archives/2009/09/the_doghouse_cr.html) points out:
<blockquote>
These numbers have nothing to do with the technology of the devices; they are the maximums that thermodynamics will allow. And they strongly imply that brute-force attacks against 256-bit keys will be infeasible until computers are built from something other than matter and occupy something other than space.
</blockquote>

The following UML diagram describes the key exchange using ECDH and securing the message with 256-bit AES symmetric key between "User A" and "User B"
![Send message with key exchange](../img/streembit_send_msg_with_key_exchange.png)

--------
Check out [other open source projects](https://github.com/zsoltpardi) I have contributed. You can contact me at tzpardi@streembit.com if you have any questions or comments.


