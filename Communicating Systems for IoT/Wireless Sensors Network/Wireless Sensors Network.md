# Smart Devices

## Description

<div align="justify">

Wireless Sensor Networks is a course focused on the architectures and protocols of wireless sensor networks. Its objective is to provide a general understanding of wireless sensor networks, from the design phase to their implementation, while highlighting the cost, energy efficiency, robustness, and lifetime of the different approaches.

The course consists of eight lectures during which we first study the fundamentals of the physical and MAC layers, IoT architecture, and the associated research challenges (new physical layers, new MAC protocols, etc.). It also covers challenges specific to WSNs, such as synchronization, localization, and energy autonomy, and explains how energy, computation, and storage constraints guide architectural choices. The remainder of the course goes deeper into low‑power technologies and protocols typically used in WSNs.

The course also relies on active learning methods (participation and discussions) and on feedback from research carried out at LAAS‑CNRS (industrial and European projects in aeronautics, space, etc.). Case studies illustrate real-world challenges (flight instrumentation, Structural Health Monitoring, wireless passenger cabins) and introduce solutions such as UWB to meet the needs of constrained environments.

The course was complemented by three laboratory sessions aimed at designing and implementing the physical and MAC layers for a given application.

The assessment was based on three assignments:
- A first group assignment aimed at validating 50% of competency C1 (detailed in the Analysis section) through the study of WSN protocols (LoRa, Sigfox, BLE, Zigbee, etc.), assessed through a written report and an oral presentation.
- A second, individual assignment validating 50% of competency C2, consisting of an analysis and comparison of MAC layers for WSNs; this required a written report and a PowerPoint presentation.
- Finally, a presentation of the work carried out and the report related to the project.

## Technical Aspects

The project associated with the course aimed to design, implement, and evaluate a physical layer and MAC layer protocol dedicated to a wireless sensor network application. We chose to develop an application focused on a smart greenhouse, ensuring the collection of environmental data such as temperature and humidity, with the objective of monitoring the internal conditions of the greenhouse.

First, we highlighted the trade-offs introduced by the different technical solutions (range versus data rate, robustness versus energy consumption, simplicity versus flexibility).

This analysis enabled us to select the most suitable approach for our application, particularly with regard to medium access mechanisms (CSMA, TDMA, hybrid protocols, etc.), and to consider their impact in terms of energy consumption and network performance, as well as the most appropriate type of modulation.

The project was carried out in a group of seven people, with a clear distribution of tasks. As far as I am concerned, I mainly worked on the design and implementation of the MAC layer.

After a reflection phase, we chose to directly implement the MAC layer using the GNU Radio tool, in order to facilitate its interfacing with the physical layer. We thus developed Python scripts integrated into GNU Radio, enabling the implementation of a customized ALOHA MAC protocol.

<div align="center">
  <img width="700" alt="image" src="https://github.com/user-attachments/assets/40b0869b-ee0c-4da3-b351-c550a4d17b6a" />
  <p><em>Figure 1: MAC GNU radio architecture</em></p>
</div>

The design and testing of the MAC layer proved to be relatively simple due to the simplicity of the ALOHA protocol. However, the use of GNU Radio turned out to be more complex. Understanding the structure of the Python blocks and their interfacing with the physical layer required a significant investment in time and effort

### Analytical


#### Learning Outcomes Assessment - Wireless Sensor Network


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| D. Dragomirescu     | Be able to analyse and evaluate protocoles dedicated to Wireless Sensor Networks / IoT | 4 / 4 | TP Report + Portfolio |


I was able to develop skills in the analysis and evaluation of protocols for wireless sensor networks (WSNs). I applied this expertise in various assessed assignments, notably during a comparative study of WSN protocols carried out as part of a group project.

In this context, I focused more specifically on the Sigfox protocol, conducting a multi-criteria analysis (range, energy consumption, data rate, cost, latency, etc.). I also attended the presentations given by other students, which allowed me to gain an initial overview of the limitations and use cases of several technologies such as LoRa, Sigfox, BLE, and Zigbee.

Finally, through this individual analytical approach, I had the opportunity to study and more importantly, to compare different existing MAC protocols. This work enabled me to better understand the relevance of each category of MAC mechanisms and to identify which protocol is best suited depending on the usage context and network constraints.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| D. Dragomirescu     | Understand and master the optimisation of IoT communication protocols at MAC level  / IoT | 4 / 4 | TP Report + Portfolio |

During the individual analysis, I observed that there are MAC protocols suited to specific types of usage. Through this approach, I studied the main medium access methods (contention-based, scheduled/TDMA, and hybrid approaches), as well as their impact on key criteria such as energy consumption, latency, effective throughput, reliability (collisions, losses), and scalability (node density).

This methodology enabled me to identify the most appropriate MAC protocol depending on the context (periodic or event-driven traffic, real-time constraints, autonomy, radio environment) and to pinpoint several options (duty cycling, tuning of listening windows, backoff mechanisms, scheduling, etc.).

The project also allowed me to consolidate the foundations acquired in radio communications and medium access by designing a MAC layer for a wireless sensor network myself.


## Source

</div>

