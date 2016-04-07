---
layout: post
title: Corporations, the ecosystem and privacy
subtitle: Decentralized systems can protect data from both government and cyber criminals
author: "T. Z. Pardi"
categories: article
---

  Apple, Google and WhatsApp did what they could by standing up for privacy and opposing to the latest compliance [requests of the FBI](http://bit.ly/1oLI78M). Apple CEO Tim Cook has gone as far as a law abiding citizen can go with [his statement](http://apple.co/1Lt7ReW). The problem is the extent of how much a business can fight back against the government. The government request highlights the single biggest fundamental flaw in the ecosystem and application architecture of iPhone: the closed ecosystem is run by a corporation and businesses by definition are subject to subpoenas and [government pressure](http://bit.ly/1nXnd6h).  
  There is no workaround to compliance and eventually businesses will have to surrender the privacy/security of the software to the government. It is naivety to assume the government won't be able to force businesses to collaborate. If it comes down to it, new laws and legislation will be adopted to press businesses to build back doors and incorporate master encryption keys [into their applications](http://bit.ly/1XJRpP0). Businesses are registered legal entities and as such they do not have human rights. Unlike citizens, businesses can't claim that their human rights are violated by the government because there is no such thing as human rights of a corporation.  
  One possible solution Streembit offers is to exclude the corporations and proprietary software from the ecosystem by implementing a community driven decentralized, P2P overlay network.This gives individuals full control over the software, infrastructure and data to individuals. After all, individuals can't be forced to [surrender their encryption passphrase](http://www.cnet.com/news/judge-man-cant-be-forced-to-divulge-encryption-passphrase).

Application architecture wise, the main issue is that Apple can bypass the security if the company choose to do so. This indicates a fundamental design flaw in the application architecture and ecosystem. No software developer should be able to bypass the security of its own application, except if the security design is less than adequate in the first place. 

On a technical note, open source systems should implement better key protection functions than iPhone does. The iPhone key protection is based on a 4-digit passcode and allows the breaking of the security in maximum 10,000 iterations using a brute force attack. Using 256-bit symmetric keys, the data is safe regardless of whether the attack is initiated by the super computers of NSA or the zombie computer cluster of cyber criminals. Brute-force attacks against 256-bit symmetric keys would be unfeasible until computers are built from something other than matter and occupy [something other than space](http://bit.ly/1QMctR8) This is [explained here](http://bit.ly/1Lv8zbz) and [here](http://bit.ly/1otrA9N). Therefore, we just need better key protection functions than the 4-digit passcode of iPhone. 

The Streembit passcode (that protects the user's PPKI key pair) is relatively complex. Even the weakest Streembit passcode requires the following number of iterations with a brute force attack: $$26^2 \times 10 \times 33 \times 95^4 \times 8! / 4! \approx 3.05 \times 10^{16}$$. This means 3,050,000,000,000  (3.05 trillion) times more iterations than the $$10^{4}$$ iterations are required to break the iPhone security.  
  Please note, this is related to the protection of the PPKI key pair. To protect real time communication, Streembit implements even more strong security by using a randomly generated 256-bit AES session key, which is never saved on the device and it is exchanged between peers with a randomly generated ECDH key pair. This means that real time communication, which is the main functionality of Streembit, is secure even from the brute force attacks of NSA super computers as well as from large zombie computer clusters of cyber criminals.

As for protecting a PPKI key pair or symmetric encryption keys, IMHO the best practice is, do not store the keys on the device instead of initialize it on-demand. If a deterministic cryptography key is generated on-demand and never stored by the device/computer, then there is nothing to break with a brute force attack. The next version (v.1.2.0) of Streembit will implement this functionality by using mnemonic code to generate deterministic keys. 

--------
Check out the [other open source projects](https://github.com/zsoltpardi) I have contributed. You can contact me at tzpardi@streembit.com if you have any questions or comments.


