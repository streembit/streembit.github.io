---
layout: page
title: Roadmap
permalink: /roadmap
---

#### Version 1.2.0


Features

* Network bootstrapping without preconfigured IP addresses. Options are IP scanning, in the case of local networks multicasting such as SDP RFC4566, SAP RFC2974 or Source-Specific Multicast RFC4607, and IPv6 anycast or BGP anycast using IPv6 anycast address group (see RFC2373 section 2.6 and https://www.ietf.org/proceedings/51/I-D/draft-ietf-ipngwg-ipv6-anycast-analysis-00.txt).
* Hide completely the contact information from the distibuted ledger. Currently the contacts publish their access information (IP address, publick key) to the DHT. We will encrypt that info with the contacts' ECDH key. (This feature will require the contacts exchange their ECDH keys with each other via another media/channel)
* Run Streembit as a background process and add Streembit icon to the taskbar, so contacts can have a better user experience.
* Android and iPhone implementation of Streembit
* Add built in STUN server implementation, so the seeds can provide the STUN functionality to the peers
* Peer to peer group video and audio chats to support the communication of large groups, teams and university classes.
* Record video and audio chat.
* Use mnemonic code for generating deterministic PPK cryptography key pairs so the PPK key pairs don't have to be saved to the device, it can be generated on-demand and stored in memory.
* Add hardware reference designs for ATMEL Xplained, STM32 Nucleo and Arduino development boards.
* Enable auditing and smart contracts by rolling out a blockhain implementation. 
* Integrate the latest standards and development from the [W3C WoT](https://github.com/w3c/web-of-things-framework) standardization initiative.
