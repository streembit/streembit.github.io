---
layout: post
title: Streembit, right to privacy, NSA surveillance
subtitle: Streembit is a tool to preserve privacy and secure IoT devices
author: "T. Z. Pardi"
categories: article
---

We have been receiving questions and comments in regard to whether it is appropriate or not to design a secure communication tools such as Streembit when governments try to protect citizens from terrorists, and in order to do that the communication of criminals, terrorists (as well as law abiding citizens) is monitored in large scale government surveillance programs. 

The right to privacy is a fundamental human right. It seems that this is not subject to dispute. Everyone has the right to conduct private communication with family, friends and business associates. In the meantime, the mobile phones of law abiding working men and women is tapped or the metadata of their Skype, Viber and Telegram conversation is collected by patrolling government agencies. So, we designed Streembit with the aim of providing users with a tool to preserve privacy.  A majority of Americans (54%) disapprove of the U.S. government’s collection of telephone and internet data as part of [anti-terrorism efforts](http://pewrsr.ch/1LhsFVH). In July 2009, a [Liberty-YouGov poll](https://www.liberty-human-rights.org.uk/human-rights/privacy) found that 77 per cent of those questioned believed the UK has become a surveillance society. This is 20 per cent more than those questioned two years previously. 

Another feature of Streembit is [Internet of Things security](http://streembit.github.io/2016-02-23-What-is-Streembit/), which keeps your internet connected IoT devices safe from cyber criminals and government intrusion.

We also received questions about how effective Streembit is in keeping the data safe from the NSA super computers. Streembit implements end to end encryption between peers using session specific 256-bit AES keys. The 256-bit AES keys are exchanged with also session specific ECDH cryptography – we believe such strong, session specific cryptography will [keep your data safe](http://streembit.github.io/2016-02-24-Streembit-security/) even from powerful NSA super computers. 

I pointed out in a [previous post](http://streembit.github.io/2016-02-26-Corporations-ecosystem-and-privacy/):

> The Streembit passcode (which protects the user's PPK key pair) is relatively complex and it requires the following number of iterations with a brute force attack: $$26^2 \times 10 \times 33 \times 95^4 \times 8! / 4! \approx 3.05 \times 10^{16}$$. This means that 3,050,000,000,000 (3.05 trillion) times more iterations than the $$10^{4}$$ iterations are required to break the iPhone security. Please note that this is related to protect the PPK key pair. To protect real time communication, Streembit uses a randomly generated 256-bit AES session key that is never saved on the device and exchanged with between peers with a randomly generated ECDH key pair. This means, real time communication - which is the main functionality of Streembit - is secure even from the brute force attacks of NSA super computers and large zombie computer clusters of cyber criminals.


--------
Check out [other open source projects](https://github.com/zsoltpardi) I have contributed. You can contact me at tzpardi@streembit.com if you have any questions or comments.
