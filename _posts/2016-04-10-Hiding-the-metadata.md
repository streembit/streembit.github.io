---
layout: post
title: Hiding the metadata
subtitle: Streembit, I2P, Tor and hiding the connection details.
author: "T Z Pardi"
categories: article
---

We've received question about metadata recently so I thought I'd go ahead and answer them. So, does Streemio hide the metadata and IP addresses of the users using Tor or I2P?

TL;DR - no.

It seems fully hiding the communication and connection metadata is not feasible, not even with Tor or I2P. The very nature of the Internet is that users are identified by their IP address. Therefore, the network providers will always know the origin of TCP/UDP requests. We can introduce as many routers, nodes, obfuscators. etc. to the communication chain as we want, but the request will have to go through at least one ISP backbone. This means that traceability cannot be avoided. Other issues with Tor and I2P are political. Many experts in the security community believe that majority of the Tor and I2P nodes are actually run by law enforcement as a convenient interception point to monitor the dark web.  After all, why should law enforcement bother with more expensive surveillance when running the Tor and I2P could give them a lot of useful metadata and traffic information? Law enforcement agencies have already demonstrated that they are fully capable of [using Tor/I2P to their advantage](http://www.theregister.co.uk/2016/03/29/fbi_tor/). So it seems that attempting to hide metadata is an uphill battle which users can never win.

While we very much respect and support the aims the of highly skilled Tor and I2P developers, Streembit tries to address the issue of privacy on a different layer by employing proven cryptography methods to keep the data safe from cyber criminals and the government: secure the communication with PPKI and end-to-end symmetric cryptography on a decentralized, peer to peer network.  We don’t claim that we can achieve the impossible and hide your metadata from the ISP. But we are certain that through well implemented cryptography, communication can be secured from both cyber criminals, industrial espionage and government mass surveillance. Also, Streembit addresses privacy requirements at a reasonably high level. No registration, email address nor personal details are required to use Streembit. It is a community driven P2P network in which the users’ personal details aren’t collected. 

--------
Check out [other open source projects](https://github.com/zsoltpardi) I have contributed. You can contact me at tzpardi@streembit.com if you have any questions or comments.



