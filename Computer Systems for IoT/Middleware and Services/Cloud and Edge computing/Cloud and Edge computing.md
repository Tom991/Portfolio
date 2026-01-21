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

This lab was based on the study of a concrete use case: an autonomous vehicle. In this context, part of the processing was offloaded to nearby edge nodes in order to reduce the embedded computational load while still enabling fast decision-making.
To achieve this, we had to deploy an infrastructure based on a Kubernetes cluster for resource and service management. The objective was to maximize system efficiency while minimizing latency.

<div align="center">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/e403d1cc-06f6-4ec8-9c5a-79bc6f5523a9" />
  <p><em>Figure 1: Illustration project</em></p>
</div>

### Analytical

#### Learning Outcomes Assessment - Cloud and Edge computing

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Understand and master the new mobile networks technologies | 3 / 3 | TP Report |

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Understand the concept of cloud computing | 3 / 3 | TP Report |

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Understand the architecture of IaaS provider | 3 / 3 | TP Report |

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Deploy a service-based applications in the cloud | 3 / 3 | TP Report |

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Automate the service-based applications provisioning with service orchestrators | 3 / 3 | TP Report |

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| S.Yangui     | Deploy service-based applications in cloud-edge continuum and setup QoS management techniques | 3 / 3 | TP Report |

## Source

</div>








