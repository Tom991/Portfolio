# Communication Protocols for LP‑WPAN

## Description

<div align="justify">

The Middleware for Internet of Things course is part of the teaching unit Middleware and Services. It is an introductory course aimed at presenting IoT architectures and technologies. Its main objective is to lead students to understand the mechanisms that ensure communication, data exchange, and data processing within IoT systems.

The course is structured into three lecture sessions. These sessions cover the fundamentals of IoT, its evolution, and its challenges. They also introduce IoT architectures and the interoperability issues associated with them. Finally, the course presents the oneM2M standard, detailing its architecture, common services, and resource model.

The course is complemented by four practical lab sessions allowing the implementation of IoT communications through the MQTT protocol, via the development of devices based on an ESP8266, as well as rapid prototyping using Node‑RED.

The assessment for this module is based on the completion of the lab sessions and the writing of a final report.

## Technical Aspects

Middleware deployment was carried out only during the practical sessions. In the context of the hackathon, setting up a middleware to ensure communication between the sensors and the remote infrastructure was a viable approach. However, since the middleware course had not yet been delivered at that time, we chose to rely on a REST interface instead.

The objective of the first lab sessions was to explore the possibilities offered by the MQTT protocol in the context of the Internet of Things. Initially, we answered several questions in order to gain a first overview of how MQTT works and its underlying principles.

We then deployed our own Mosquitto MQTT broker and used this setup to perform remote communications, including reading the state of a button and controlling an LED. Finally, we developed an application in collaboration with another team, involving two ESP devices communicating with each other via the MQTT protocol.

<div align="center">
  <img width="400" alt="image" src="https://github.com/user-attachments/assets/cfdc578f-5954-4b3c-b98e-0cfaf98ef733" />
  <p><em>Figure 1: Two ESP application</em></p>
</div>

Lab session 3 aimed to introduce us to fast prototyping, through the use of Node‑RED, a visual programming tool that enables rapid design of IoT applications. This tool facilitates the interconnection of connected objects, particularly via MQTT. We also experimented with data visualization using Node‑RED, by creating a dashboard serving as a supervision and monitoring interface.

Finally, during the last lab session, we discovered the specialized middleware Home Assistant. We connected ESP8266 devices to the system via MQTT. This home‑automation‑oriented middleware allows connected objects to be represented, supervised, and automated within a system. It provides features such as graphical user interfaces, data history, dashboards, and the deployment of logical rules, all without requiring heavy programming.

<div align="center">

  ```mermaid
graph TB
    A["Objets connectés<br/>(ESP8266)"]
    B["Communication<br/>Publish / Subscribe<br/>(MQTT)"]
    C[Home Assistant]
    C1[Abstraction des objets]
    C2[Gestion des états]
    C3[Automatisations]
    D[Interface utilisateur<br/>Visualisation]

    A --> B
    B --> C
    C --> C1
    C --> C2
    C --> C3
    C --> D
```
<p><em>Figure 2: Last tutorial architecture</em></p>
</div>


## Analytical

#### Learning Outcomes Assessment - Communication protocols for LP-WPAN

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| T. Monteil     |Know how to situate the main standards for the Internet of Things | 4 / 4 | Homework assessment. |

I developed this skill during the lecture sessions, which provided an overview of IoT standards and technologies. These courses enabled me to identify the main IoT standards and to understand their roles, particularly through the study of IoT‑oriented communication protocols such as MQTT, as well as standards like oneM2M.

The first practical sessions also helped reinforce this theoretical knowledge by requiring me to research and analyze additional information in order to answer the questions in the lab report.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| T. Monteil     | Deploy and configure an IoT architecture | 4 / 4 | Homework assessment. |

I am able to deploy and configure a complete IoT architecture. I was able to put this skill into practice on several occasions, particularly during the lab sessions of this module, during which I deployed an architecture ranging from connected devices to communication mechanisms, configuring components such as the MQTT broker through to data visualization.

This skill was also mobilized during the Smart Devices project, where I participated in the deployment of a complete IoT architecture, from the sensor to data monitoring, also using the MQTT protocol.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| T. Monteil     | Interact with the different resources of the architecture using REST services | 4 / 4 | Homework assessment. |

I did not directly use REST interfaces during the lab sessions of this module. However, I had the opportunity to implement such interfaces several times during the year, notably in service‑oriented architecture courses, as well as during the hackathon, during which we deployed a REST interface to ensure communication between the cloud and the microcontroller.

These experiences enabled me to interact with the various components of a distributed architecture using REST services.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| T. Monteil     | Integrate a new technology into the deployed architecture | 4 / 4 | Homework assessment. |

This skill was developed during the rapid prototyping and integration lab sessions, particularly through the use of tools such as Node‑RED and Home Assistant. By progressively integrating new technologies into an existing architecture and adapting communication interfaces, we were able to evolve our IoT system.

This allowed us to observe the impact of introducing a new middleware and its integration within an already deployed IoT architecture.


## Source

</div>
