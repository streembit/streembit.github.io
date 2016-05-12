---
layout: post
title: Hiding the metadata
subtitle: Streembit, I2P, Tor and hiding the connection details.
author: "T Z Pardi"
categories: article
---

We've received questions about hiding the metadata with Streembit, so I thought I’d go ahead and answer them. Does Streembit hide the metadata and IP addresses of the users using Tor or I2P?

It seems that fully hiding the communication related metadata is not feasible, not even with Tor nor I2P. The very nature of the Internet is that users are identified by their IP address. Therefore, the network providers will always know the origin of TCP/UDP requests. We can introduce as many routers, nodes, obfuscators, etc. to the communication chain as we want, but the request will have to go through at least one ISP backbone. This means that traceability cannot be avoided. Other issues with Tor and I2P are political. Many experts in the security community believe that the majority of the Tor and I2P nodes are actually run by law enforcement as a convenient interception point to monitor the dark web. After all, why should law enforcement bother with more expensive surveillance? Tor and I2P could give them a lot of useful metadata and traffic information. Law enforcement agencies have already demonstrated that they are fully capable of [using Tor/I2P to their advantage](http://www.ibtimes.co.uk/fbi-crack-tor-catch-1500-visitors-biggest-child-pornography-website-dark-web-1536417). So, it seems that attempting to hide metadata is an uphill battle that users can never win.

We very much respect and support the aims of the highly skilled Tor and I2P developers, but Streembit tries to address the issue of privacy on a different layer by employing proven cryptography methods. This keeps the data safe from cyber criminals and the government by securing the communication with PPKI and end-to-end symmetric cryptography on a decentralized, peer to peer network. We don’t claim that we can achieve the impossible and hide your metadata from the ISP. However, we are certain that through well implemented cryptography, communication can be secured from both cyber criminals, industrial espionage and government mass surveillance. Also, Streembit addresses privacy requirements at a reasonably high level. No registration, email address nor personal details are required to use Streembit. It is a community driven P2P network in which the personal details of the users aren't collected.

-------

Check out the [other open source projects](https://github.com/zsoltpardi) I have contributed. You can contact me at tzpardi@streembit.com if you have any questions or comments.





