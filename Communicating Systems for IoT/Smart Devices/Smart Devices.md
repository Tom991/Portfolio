# Smart Devices

## Description

<div align="justify">

The Smart Devices course, integrated into the broader field of communicating systems for IoT, aims to introduce us to the design, development, and implementation of a device capable of measuring, processing, and transmitting data over a low‑bit‑rate network. 

This module follows an open-source-oriented approach, encouraging collaboration, knowledge sharing, and project reproducibility. 

The final objective of the project is to design a complete system, starting with the fabrication of a gas sensor, then developing a shield board to facilitate the integration of the sensor and various peripherals with a microcontroller. The collected data are then transmitted over a LoRa network.

To achieve this objective, the module is structured into three main parts:


1.	AIME Internship: Gas sensor fabrication

The AIME internship takes place over one week and is dedicated to the fabrication of a nanoparticle‑based gas sensor.

2.	Cours et TD : d’introduction à la chaîne de mesure et aux smart divices

These sessions, consisting of seven lectures, first introduce the fundamental principles of sensors and the measurement chain. Then, after the design of the gas sensor, work begins on the sensor datasheet.

3.	Travaux pratiques et projet

The laboratory sessions cover the entire development chain, from SPICE simulation of the sensor measurement and signal conditioning, to the design of a PCB integrating the sensor and the components required for LoRa communication. They also include the development of code for data acquisition and transmission, as well as the production of the associated documentation. This part of the course consists of 19 laboratory sessions. With the assistance of the instructors when needed, we were therefore able to work autonomously and make our own implementation and design choices.

The assessment of the module is based on all the deliverables produced, including the sensor datasheet, the shield design files created using KiCad, as well as all the developed code, both for the microcontroller and for the application and monitoring interface implemented using Node-RED.

## Technical Aspects

The teaching of this subject is structured around several complementary yet distinct components. The technical part has therefore been divided into several sections.

### AIME Internship

The internship at AIME (Atelier Interuniversitaire de Micro Nano Electronique) primarily aimed at the fabrication of a gas sensor based on a nanoparticle layer. The work covered the entire process, from cleanroom fabrication starting with oxidation to the integration of the sensitive layer by dielectrophoresis onto interdigitated electrodes. The sensors were then characterized under controlled atmospheres, with a particular focus on studying the impact of the operating temperature.

The internship consisted of four major stages:
1.	Synthesis of WO₃ nanoparticles (NPs)

We produced a nanostructured WO₃ solution, ready to be deposited onto the sensor electrodes.

2.	Fabrication of the microelectronic device

We carried out the main steps required for sensor fabrication: oxidation, polysilicon deposition, doping, successive photolithography steps, etching, metallization, and annealing. 

The chips were then diced, selected, and assembled, followed by wire bonding. This resulted in chips ready to receive the sensitive layer.

3.	Integration of the active nanoparticle layer

After depositing a drop of WO₃ solution onto the interdigitated electrode area, dielectrophoresis was performed to integrate the active layer.

4.	Electrical characterization under gas exposure

Finally, the sensor was characterized under controlled atmospheres by measuring its electrical response during alternating exposures to dry air and target gases (NH₃ and ethanol), and by evaluating the influence of operating conditions, particularly temperature.

### Project / Practical work

This project was carried out in a team of three. In order to work efficiently, we decided to divide the tasks: part of the group focused on the design and implementation of the PCB, while I was mainly responsible for the software development.

As a first step, I set up LoRa communication to enable the transmission of data acquired by the gas sensor. Once the LoRa link was operational and data transmission had been validated, we developed a test platform allowing us to progress without depending on the shield board. To achieve this, we reproduced and wired the electronic circuit designed during the laboratory sessions, enabling the acquisition of the sensor measurements.

<div align="center">
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/4922829b-d031-4923-88ac-cd30ac65d5a8" />
  <p><em>Figure 1: Setup of the prototype</em></p>
</div>


I then created a Node‑RED dashboard to monitor the sensor data via MQTT. This interface allows real-time visualization of the measurements, verification of the consistency of the transmitted data, and easier debugging of the system, including communication, acquisition, and data display.

<div align="center">
  <img width="880" alt="image" src="https://github.com/user-attachments/assets/6f4a940b-9614-49bf-a88e-d0818d4ed81b" />
  <p><em>Figure 2: Node-RED stream</em></p>
</div>

<div align="center">
  <img width="338" alt="image" src="https://github.com/user-attachments/assets/7d9e8fd5-443d-47ca-9ee3-aa81d351fb57" />
  <p><em>Figure 3: Node-RED dashboard</em></p>
</div>

Finally, we developed an embedded application responsible for both reading the gas sensor measurements and managing the display screen.


<div align="center">
  <img width="669" alt="image" src="https://github.com/user-attachments/assets/43ede4ee-ff13-4ea2-b5f0-6d707c109bbb" />
  <p><em>Figure 3: Node-RED dashboard</em></p>
</div>

### Analytical


#### Learning Outcomes Assessment – Microcontrollers and Open-Source Hardware, Embedded IA (M&OSH)

<table>
  <thead>
    <tr>
      <th><b>Instructor</b></th>
      <th><b>Learning Outcome</b></th>
      <th><b>Self‑Assessment (AE)</b></th>
      <th><b>Evaluation Method</b></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5">J. Grisolia, S. Lohez, B. Mestre, A. Biganzoli</td>
      <td>Understand microcontroller archictecture and how to use them</td>
      <td>4 / 4</td>
      <td>Portfolio</td>
    </tr>
    <tr>
      <td>Be able to design data acquisition system (sensor, conditioner, microcontroller) with respect to the application</td>
      <td>4 / 4</td>
      <td>Portfolio</td>
    </tr>
    <tr>
      <td>Be able to design a shield to accommodate the gas sensor</td>
      <td>4 / 4</td>
      <td>Portfolio</td>
    </tr>
    <tr>
      <td>Be abe to design the sofware to use the gas sensor and its HMI</td>
      <td>4 / 4</td>
      <td>Portfolio</td>
    </tr>
    <tr>
      <td>Be able to combine all of the above mentioned components into a smart device</td>
      <td>4 / 4</td>
      <td>Portfolio</td>
    </tr>
  </tbody>
</table>

Given my background in electronics and my prior experience with microcontrollers, this part of the project mainly allowed me to put these foundations into practice and apply them within a fully integrated system context. I made use of concepts related to peripherals and communication interfaces in order to build the embedded program. I believe I have gained a solid understanding of these notions and was able to apply them effectively.

The project also enabled me to implement a complete data acquisition chain, from the sensor to data exploitation: reading measurements via the microcontroller, taking into account the conditioning circuit designed during the laboratory sessions, and setting up a test platform to progress independently of the shield board. Although I had already previously worked on similar acquisition chains, this course provided an opportunity to reinforce and apply this knowledge in a structured and realistic context.

Even though the PCB design was handled by other members of the team, I was able to understand and take into account the constraints related to the shield design and contribute to integration-related decisions. Moreover, during my academic curriculum (3AE / 4AE), I have already designed two boards using CAD tools, which allowed me to provide input on layout and interfacing aspects. This contribution was notably reflected in hardware/software coordination, particularly by anticipating integration constraints.

#### Learning Outcomes Assessment – Sensors introduction

This experience allowed me to gain insight into the entire design, fabrication, and validation chain of a gas sensor, using tools and techniques derived from microelectronics.

I became familiar with cleanroom processes and developed an understanding of their logical and highly constrained sequence, from substrate preparation to the realization of a fully functional sensor. This approach helped me grasp how a device is built through the successive stacking of process steps, such as oxidation, thin‑film deposition, doping, photolithography, etching steps, metallization, and thermal annealing.

Throughout the process, I was also made aware of the importance of controlling the fabrication steps. Regular microscopic observations were carried out to verify the conformity of each step before continuing the process.

Finally, I sought to follow as many fabrication stages as possible. Although my knowledge of chemistry remains limited for fully understanding all the subtleties of the protocol, this experience enabled me to acquire a comprehensive and practical overview of sensor fabrication and integration.


#### Learning Outcomes Assessment – Sensors introduction

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| J. Grisolia     | Understand basic notions of sensors, data acquisition: physics, electronics and metrology point of view | 4 / 4 | TP Report + Portfolio |

The lectures enabled me to gain a better understanding of sensors, particularly from a physical and metrological perspective, thanks to the various practical exercises proposed during the sessions. These activities helped me better understand measurement principles, sources of error, and the performance characteristics associated with sensors.

Throughout my academic training, I had already acquired a solid foundation in electronics. This course allowed me to further develop this knowledge by more closely linking it to the physical aspects of sensors and data acquisition.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| J. Grisolia     | Be able to design the datasheet of the sensor manufactured | 4 / 4 | TP Report + Portfolio |

Writing the sensor datasheet was a particularly formative experience. It helped me understand the importance of cross‑disciplinary skills, combining physics and electronics, in order to accurately describe the operation and performance of a sensor. Thanks to this experience and my background in electronics, I now feel capable of carrying out this task autonomously in the future.

#### Learning Outcomes Assessment – Analog electronic labs

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| J. Grisolia     | Be able to design the electronic circuit of a sensor’s signal conditioner (design + simulation) | 4 / 4 | TP Report + Portfolio |

The analog electronics laboratory sessions enabled me to further develop my skills in designing signal conditioning circuits for sensors. During my academic background in electronics, I had already had the opportunity to design conditioning circuits, which allowed me to approach these sessions with solid foundations.

I am therefore able to design and simulate a signal conditioning circuit adapted to a given sensor, taking into account the signal characteristics and the measurement requirements. 

## Source

</div>


