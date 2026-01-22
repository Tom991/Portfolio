# Cloud and Edge computing

## Description

<div align="justify">

The Cloud and Edge Computing course is part of the Middleware and Services teaching unit and is dedicated to distributed architectures and the Cloud/Fog/Edge paradigms. Its objective is to enable students to gain an understanding of Cloud and Edge environments. It thus helps to understand how to centralize, store, and process data and services that connected objects (often constrained in terms of energy, computation, storage, and networking capabilities) cannot handle on their own.

This course is structured around four lecture sessions. These first present the fundamentals of virtualization, particularly through the study of virtual machines and containers. The course then introduces the concept of cloud computing and describes the architecture of an Infrastructure-as-a-Service (IaaS) provider. Subsequent sessions address Cloud service models (IaaS, PaaS, and SaaS), application deployment and orchestration mechanisms, as well as issues related to scalability, availability, and resource management.

The course also covers the Fog and Edge Computing paradigms, highlighting their complementarity with the Cloud and their relevance for connected objects, notably in helping to address constraints related to latency, bandwidth requirements, and data proximity.

This teaching was complemented by six practical lab sessions. These first included an introductory lab to become familiar with the practical elements presented in the lectures, followed by a lab/project aimed at simulating a context close to real-world conditions. Assessment was based on the completion of a report at the end of the practical work.

## Technical Aspects

I was able to leverage the knowledge acquired during this course in two different contexts. First, as part of the lab/project work for the course itself, where these concepts were directly required to successfully complete the assigned tasks. Second, during the team project carried out as part of the hackathon, where I had to apply these skills in a more constrained environment (limited time and collaborative setting), adapting our approach to achieve a rapidly functional result.

### Practical Work of the Course
#### Introduction to Cloud Hypervisors
The first lab aimed to consolidate the basics of virtualization, to understand why virtualization is used, what it enables, and what trade-offs it introduces. Initially, it focused on learning how to distinguish between and choose appropriate execution environments according to a given use case namely between a VM (Virtual Machine) and a CT (Container). This included understanding the implications in terms of cost, resource consumption, performance, and security, as well as gaining insight into Type 1 and Type 2 hypervisors.

This lab also enabled initial hands-on experience with VirtualBox, Docker, and OpenStack, including configuration tasks (port forwarding, firewall rules, floating IPs, etc.) and basic VM operations (snapshot, restore, resize).

The lab concluded with an introduction to automation through the OpenStack client and the construction of a network topology enabling the deployment of a distributed application, representing a first step toward a real-world application.
Service Orchestration in a Hybrid Cloud/Edge Environment

#### Service Orchestration in a Hybrid Cloud/Edge Environment

This lab was based on the study of a concrete use case: an autonomous vehicle. In this context, part of the processing was offloaded to nearby edge nodes in order to reduce the embedded computational load while still enabling fast decision-making.

To achieve this, we had to deploy an infrastructure based on a Kubernetes cluster for resource and service management. The objective was to maximize system efficiency while minimizing latency.

<div align="center">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/e403d1cc-06f6-4ec8-9c5a-79bc6f5523a9" />
  <p><em>Figure 1: Illustration project</em></p>
</div>

### Hackaton
As part of the project developed during the hackathon presented in this section, I had the opportunity to take responsibility for the design and deployment of the cloud component of the system. The main objective was to enable the update of an application based on data transmitted by a presence sensor, via an ESP8266 microcontroller acting as a gateway.

To meet this requirement, I chose to deploy a virtual machine on the OpenStack infrastructure provided by INSA. This virtual machine centralized all the components of the project: it hosted the database, the application front end and back end, as well as the program responsible for receiving data and sending commands via HTTP requests.

After further analysis, this cloud architecture proved to be overly simple and monolithic. It was designed in the context of the hackathon, which required rapid development, but it presented several limitations, particularly in terms of resilience, security, and maintainability. In the event of a virtual machine failure, the entire system would become unavailable, and hosting all services on a single instance increased the attack surface and complicated future evolutions.

With more time, a more robust architecture would have been preferable. In particular, I would have better isolated the different services to improve fault tolerance and overall system security. For example, an architecture similar to the one studied during the practical labs could have been implemented: a first machine, placed on a private network exposed to the outside, would have been dedicated to handling HTTP requests and acting as the entry point. This machine would then have communicated with a second, isolated private network containing one machine per service (database, application back end, etc.). Such an approach would have enabled better separation of concerns, isolation of sensitive services, and greater system scalability.

### Analytical

#### Learning Outcomes Assessment - Cloud and Edge computing

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Understand and master the new mobile networks technologies | 3 / 3 | TP Report |

This skill was acquired from the very first lessons. I was then able to deepen my understanding and experiment with these two concepts during the practical sessions. In particular, the introductory lab enabled me to understand the fundamental principles of virtualization, as well as the differences in operation, performance, and use cases between virtual machines and containers.

It also allowed me to identify the trade-offs involved, in terms of costs, resource consumption, and performance.

Using VirtualBox and Docker helped me to concretely visualize these concepts through tools that are widely used in professional environments.

I now believe I am able to clearly explain these notions, represent them schematically, and justify the choice of one execution environment (virtual machine or container) over another, depending on the constraints imposed by the context

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Understand the concept of cloud computing | 3 / 3 | TP Report |

I believe I have developed a fairly good understanding of the different cloud computing models (IaaS, PaaS, and SaaS) covered in class. The courses helped me grasp the value of the cloud in terms of computing, storage, and service management, particularly with regard to flexibility, scalability, and cost optimization.

I have also understood how the cloud represents a particularly well-suited solution for deploying applications of all kinds, including those based on distributed architectures or incorporating IoT components.

In this context, the cloud facilitates large-scale data collection, processing, and analysis, while ensuring high service availability and simplified infrastructure management.

This knowledge now enables me to identify the most relevant cloud model based on an application’s needs, technical constraints, and requirements..

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Understand the architecture of IaaS provider | 3 / 3 | TP Report |

Using OpenStack allowed me to gain a better understanding of the architecture of an IaaS provider, both in terms of managing compute, network, and storage resources, and in implementing security mechanisms.

In particular, configuring security rules helped me to understand access management, network traffic filtering, and the challenges related to protecting exposed services.

I consider that I have acquired a solid understanding of how an IaaS platform operates, its principles, and its use cases, even though I do not consider myself an expert in its internal architecture. 

Nevertheless, I am able to explain the key concepts, describe the main components of an IaaS provider, and understand the general technical choices made to ensure infrastructure performance, availability, and security.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Deploy a service-based applications in the cloud | 3 / 3 | TP Report |

I was able to make use of this skill on several occasions, both during practical labs through the deployment of distributed applications and as part of the hackathon. These experiences allowed me to implement the different stages required for deploying a service-oriented application in the cloud.

I was thus able to configure execution environments, manage software dependencies, ensure communication between services, and monitor their overall proper functioning

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Automate the service-based applications provisioning with service orchestrators | 2 / 3 | TP Report |

I was able to set up and use a Kubernetes cluster as part of the practical labs, which allowed me to understand the fundamental principles of service orchestration and the automation of service-oriented application deployment.

In particular, I participated in configuring the cluster and deploying containerized services provided by Kubernetes (pods, services, deployments).

Although I have acquired an overall understanding of how Kubernetes works and of its key concepts, I believe that this skill is not yet fully mastered.

At this stage, I would not be able to independently deploy a complete Kubernetes architecture from scratch. Further exploration of the tool, through additional practice and experimentation, would be necessary for me to gain greater autonomy and confidence.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Deploy service-based applications in cloud-edge continuum and setup QoS management techniques | 3 / 3 | TP Report |

Teaching in this module enabled me to clearly understand the complementarity between Cloud, Fog, and Edge Computing. In particular, I understood the relevance of these approaches in reducing latency, leveraging data proximity, and enabling fast decision-making, which are essential elements for real-time applications.

These concepts were illustrated through a practical assignment based on the case of an autonomous vehicle, which highlighted the distribution of processing across the different layers (edge for immediate decisions). However, the limited time allocated to this practical work did not allow me to fully explore the concrete implementation aspects related to Edge Computing.


## Source

</div>








