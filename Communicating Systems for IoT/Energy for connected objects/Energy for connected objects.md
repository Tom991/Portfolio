# Energy for connected objects

## Description

<div align="justify">

The Energy for Connected Objects course, integrated into the broader field “Communicating Systems for IoT”, focuses on issues related to the energy supply of connected objects. Its objective is to enable students to understand how to design partially or fully energy‑autonomous IoT systems, while taking into account constraints related to energy consumption, storage, and harvesting.

This course addresses the principles of energy production and management for connected objects. It presents electrical energy storage solutions as well as energy harvesting techniques based on ambient sources (light, mechanical, thermal, and electromagnetic energy). It also covers wireless power transfer methods, particularly those based on electromagnetic waves, highlighting both the opportunities they offer and their limitations in terms of cost and efficiency.

The course includes four lecture sessions introducing the state of the art and emphasizing the necessary trade‑offs between performance, autonomy, operating environment, and energy constraints.

The lectures are complemented by two lab sessions, whose objective is to implement energy‑supply solutions based on electromagnetic energy harvesting.

The assessment is based on the completion of a lab report, which is integrated into the student portfolio.

## Technical Aspects
I was able to apply the knowledge acquired in this course during the associated laboratory sessions, particularly by imagining and evaluating possible energy‑harvesting solutions for our innovative project.

The lab sessions aimed to concretely apply the concepts of electromagnetic energy harvesting. First, we analyzed the energy requirements of our system, namely the power supply of a red LED. We then studied different power‑supply strategies in order to determine whether it was feasible to directly use the harvested energy or whether intermediate energy storage was required.

We also characterized the voltage rectifier used in the system. To do so, we employed an Analog Discovery device to measure its frequency response, analyze the achieved efficiencies, and identify optimal operating conditions.

<div align="center">
  <img width="472" alt="image" src="https://github.com/user-attachments/assets/c3ccfc80-f4f4-4eb0-9223-a53db37e2810" />
  <p><em>Figure 1: Tutorial setup</em></p>
</div>

In addition, we studied the choice of the most suitable antenna for energy harvesting in our system, taking into account constraints related to efficiency and integration.

Finally, the lab sessions addressed wireless electromagnetic energy transfer via radiation. We estimated the maximum achievable range while complying with regulatory emission constraints and applying free‑space propagation equations. This analysis highlighted the trade‑offs between operating frequency, efficiency, and transmitted power.

The lab sessions also included an analytical component related to our innovative project available in the portfolio's github.

## Analytical

#### Learning Outcomes Assessment - Energy for connected objects

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| G.Loubet      | Know how to harvest/transfer, store and manage power for connected objects, and how to increase the power efficiency | 3 / 4 | TP Report + Portfolio |

By attending the lectures, I acquired a global understanding of energy harvesting and transfer techniques applicable to connected objects. These courses mainly allowed me to understand the general principles, identify potential energy sources, and grasp the order of magnitude of the involved power levels.

Implementing a simple electromagnetic energy‑transfer system during the lab sessions quickly showed me that, despite the apparent simplicity of the principle, practical implementation is highly constrained. The very low recoverable power, the significant losses at the various conversion stages, and the high sensitivity to external parameters make such systems difficult to exploit under real‑world conditions.

This course therefore mainly taught me to take a step back regarding energy‑supply solutions for IoT. Without considering myself an expert in these technologies, I am now able to reason about their feasibility, identify their limitations, and evaluate their relevance depending on the application context.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| G.Loubet      | Be able to optimize the power consumption of connected objects | 4 / 4 | TP Report + Portfolio + Innovative project |

During the lectures, I studied several principles for reducing energy consumption, both from a hardware and a software perspective. The course enabled me to identify the main contributors to energy consumption in an IoT system namely the radio, sensors, and microcontroller and to understand the importance of operating modes in limiting overall system consumption.

The work carried out in this course, as well as in the WSN course, helped me understand that energy‑consumption optimization relies on trade‑offs between performance, autonomy, and constraints. In particular, I observed the major impact of wireless communications on energy consumption and studied various strategies to reduce transmissions, especially through the analysis of MAC layers.

I also explored the use of low‑power operating modes, such as the microcontroller’s sleep mode, as a means to improve the autonomy of embedded systems.

Although I do not yet fully master energy‑optimization techniques, I am able to identify the main sources of consumption and to implement basic methods to reduce the energy consumption of an IoT system.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| G.Loubet      | Be able to design and implement an energy autonomous and battery-free connected object | 4 / 4 | TP Report + Portfolio + Innovative project |

During the lab sessions, I learned how to analyze the energy requirements of a simple system and evaluate the feasibility of an autonomous power supply by comparing the device’s consumption with the actual harvestable energy. I also implemented an electromagnetic energy‑harvesting chain.

Overall, this experience enabled me to understand that designing a battery‑free object requires extremely low energy consumption and, in the context of IoT integration, optimization of all sources of consumption.

I now believe I am capable of reasoning about the energy feasibility of a very simple connected object. However, for more complex IoT systems integrating a radio and additional resources, implementing a fully energy‑autonomous solution is much more challenging and likely requires significant technical trade‑offs.

## Source

</div>
