# Communication Protocols for LP‑WPAN

## Description

<div align="justify">

The Communication Protocols for LP-WPAN course is part of the EU Wireless Communications program. It focuses on communication technologies and network protocols that enable the connection of intrinsically constrained IoT objects in terms of energy consumption, data rate, and frame size within wireless networks, in particular LP-WPANs (Low-Power Wireless Personal Area Networks). Special attention is given to the Internet protocol stack based on IPv6 for IoT networks.

The course first introduces the application requirements related to IoT. It then presents the fundamentals of LP-WPANs and the IEEE 802.15.4 standard, as well as the architectures defined by the IETF for IoT, based on the combination of IPv6, 6LoWPAN, and RPL, in order to enable their integration into constrained networks of the LP-WAN type.

The course is complemented by hands-on experimental activities aimed at implementing and observing IPv6 mechanisms, and then exploiting this connectivity to carry out application-level communications.

The teaching is organized around three lecture sessions and three tutorial sessions.

Assessment is based on homework assignments including a Moodle quiz, as well as a questionnaire serving as input to this part of the report, which focuses on the key principles of an IP-based IoT architecture and on the mechanisms that make IPv6 usable in LP-WPAN networks, notably through 6LoWPAN and the RPL routing protocol.

## Technical Aspects
I was able to mobilize the knowledge acquired during this course through two complementary components. On the one hand, through tutorial sessions (TD), whose objective was to move from a theoretical understanding of the IP architecture for IoT to its practical use (auto‑configuration, Neighbor Discovery, routing, data dissemination). On the other hand, through the work required as part of the assessment (homework/quiz), which led me to justify architectural choices and to explain why adaptations such as 6LoWPAN and RPL are necessary in constrained IoT networks.

### Tutorial sessions (TD)

The first lab/tutorial session aimed to familiarize us with the basics of IPv6 in an IoT context, particularly auto‑configuration, router advertisements, the use of multicast, and routing mechanisms, while assessing the benefits and constraints of IPv6 for IoT.

The scenario was based on a topology composed of end devices interconnected via an IoT network, emulated by an Ethernet switch acting as a radio gateway. This network was connected to a Network Gateway (Cisco router), itself connected to an application server.

<div align="center">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/c74d8ccd-4975-4aa9-856e-05eaa37e1c82" />
  <p><em>Figure 1: Network topology</em></p>
</div>

Initially, we carried out the initial configuration of the network interfaces of the end devices and verified their ability to join an IPv6 network. We then studied the address auto‑configuration mechanism by analyzing the exchanges occurring when the interfaces were activated.

The next phase focused on the auto‑configuration of global unicast addresses via the router. We enabled IPv6 forwarding on the gateway and observed the impact of Router Advertisements (RA) on host configuration, particularly in terms of addressing and routing tables.

During the second tutorial session, we further explored IPv6 in an IoT context, focusing on 6LoWPAN and the RPL protocol. The experimentation relied on an emulated network using mininet‑wifi, allowing us to simulate certain aspects of the IEEE 802.15.4 and 6LoWPAN stacks, notably IPv6 header compression.

First, we focused on 6LoWPAN compression with RPL disabled. Using Wireshark on the WPAN interface, we analyzed the exchanged frames (Router Solicitation, Neighbor Advertisement, etc.) in order to observe how 6LoWPAN compresses IPv6 header fields.

The second step consisted in restarting the emulation with RPL enabled. We then observed the construction of RPL routing by examining the routing tables of the nodes and the organization of the network’s logical topology.



## Analytical

#### Learning Outcomes Assessment - Communication protocols for LP-WPAN

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S. Abdellatif     | Understand the main benefits and limitations of adopting an Internet-based (i.e., IPv6) protocol stack for IoT access networks, including its underlying principles and how it differs from the legacy IPv6-based protocol stack | 2 / 2 | Homework assessment. |

Before these courses on LP‑WANs, I had never studied IPv6. I therefore approached this topic without any background on specific mechanisms such as auto‑configuration or Router Advertisements. However, the lab sessions and the networking fundamentals acquired during my third and fourth academic years allowed me to understand the key principles quite easily.

The need for protocols such as 6LoWPAN and RPL then becomes obvious when using IPv6 in an IoT context. The questionnaire also allowed me to step back and reflect on the benefits and fundamentals of these technologies.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S. Abdellatif     | Set up and operate a basic IPv6 based IoT Network | 2 / 2 | Homework assessment. |

After the experiments carried out during the tutorial and lab sessions, I feel capable of deploying and operating a small IPv6‑based IoT network: configuring and validating hosts, and verifying Router 

Advertisements and routing. However, I will most certainly need to carry out a significant number of trials before achieving a fully functional configuration.

## Source

</div>




