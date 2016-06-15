---
layout: page
title: Roadmap
permalink: /roadmap
---

#### Version 1.2.0
Planned delivery 09/2016

Features

* Network bootstrapping without preconfigured IP addresses. Options are IP scanning or multicasting, SDP/SAP Block, RFC2974.
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
