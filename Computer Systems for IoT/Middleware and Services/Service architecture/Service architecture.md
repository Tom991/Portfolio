# Service architecture

## Description

<div align="justify">

Service Architecture is a course within the Middleware and Services teaching unit, dedicated to service-oriented architecture, REST APIs, and the transition toward microservices. Modern information systems often integrate heterogeneous applications (languages, platforms, etc.). While some middleware solutions exist, they are often associated with strong environmental constraints and high integration costs.

This course aims to present an alternative based on the use of microservices.

The course is structured into six lecture sessions delivered in the form of MOOCs (Massive Open Online Courses). Through three MOOCs, students progress from a monolithic application to service-oriented architectures (SOA), then to REST/ROA architectures, and finally to the use of microservices, which represent the culmination of the course.

These lectures are complemented by various exercises on Moodle, in the form of quizzes and self‑assessment questions. In addition to the lectures, ten tutorial (TD) sessions are associated with this course. Closely following the progression of the lectures, these sessions rely on technical tutorials designed to help students become familiar with the tools used.

The course also includes a project, for which four practical lab (TP) sessions are scheduled. Assessment for this course is carried out directly based on the completed project.

## Analytical

### Tutorials

All of these tutorial sessions offer a progressive learning path, starting with the understanding of services and moving toward the design of more modern and industrializable architectures. The first step consists of becoming familiar with the SOAP approach. The objective was to understand that a Web service can be consumed and documented based on a description, independently of its implementation.

In a second phase, the tutorials allowed us to develop small basic programs in order to become familiar with the different methods. In particular, we were able to implement a SOAP Web service from a description and test it using SOAPUI.

The next stage of the learning path introduces REST architecture, presented as a more resource‑oriented and widely used alternative based on HTTP. The functionalities previously expressed as SOAP operations are redesigned as REST APIs. We were thus able to implement and deploy RESTful Web services and test them using Postman.

Finally, the last tutorial session extends the reflection by addressing the transition from services to a microservices approach. Based on an e‑commerce context, the system is decomposed into more autonomous components, clarifying the responsibilities of each microservice and reflecting on data management. Implementation with Spring Boot simplifies the process by enabling automatic generation of the POM file.

### Course Project

The project consists of developing a Web application based on a microservices architecture. The principle is to collect information from sensors, analyze it, and then use this data to support decision‑making and potentially trigger actions. The general idea is similar to room management systems (temperature, presence, opening/closing, lighting).

We therefore developed an application for a restaurant. The main objective is to facilitate service organization by providing an overview of the status of tables. The application indicates whether a table is occupied, free, or needs to be cleaned, in order to better guide customers and optimize dining‑room management. In addition, the application provides information about available dishes, helping staff quickly know what remains and better manage service.

To achieve this, we implemented a total of seven microservices. Four microservices cover the business functionalities described above. We also added a configuration server, allowing configuration files to be externalized in Git. This approach simplifies parameter management and makes it easier to update microservice configurations, potentially in real time.

Furthermore, we integrated a discovery microservice in order to avoid dependency on a fixed port number: if the port of a microservice changes, it can still be automatically located. Finally, a gateway microservice was set up to provide a single, homogeneous entry point to all microservices, thereby simplifying communication and access to the different functionalities.

### Hackaton

During the hackathon, I participated in the design and deployment of a bus management application based on a microservices architecture in JavaScript. The project aimed to develop a complete solution enabling the collection of data from a presence sensor connected to a microcontroller, its processing and storage, and the provision of a dedicated user interface.

<div align="center">
<img width="500" alt="image" src="https://github.com/user-attachments/assets/a91b924c-0945-45ab-b814-0296987fce08" />
  <p><em>Figure 1: Front-end service</em></p>
</div>

This experience, carried out prior to the main project, allowed me to understand the value and the challenges of a microservices architecture.


#### Learning Outcomes Assessment - Middleware for Internet of Things

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| N. Guermouche     | Develop a distributed architecture using  web services | 4 / 4 | Project |

I was able to acquire this skill progressively throughout the course, first during the tutorial sessions and then during the final project.

Within the scope of the project, I was required to design and implement Web services, distribute responsibilities among several autonomous components, and ensure communication between them. 

This approach allowed me to better understand the challenges related to service orchestration and data exchange management. As a result, in our final project, the application is based on an architecture composed of seven distinct microservices, each fulfilling a specific and clearly defined function. This organization enhanced the modularity, maintainability, and scalability of the application.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| N. Guermouche     | Deploy and configure an SOA using SOAP | 4 / 4 | Project |

The tutorial sessions dedicated to SOAP allowed me to implement a SOAP Web service based on a description (WSDL), configure it, and deploy it. These exercises provided me with an overview of the different stages involved in deploying a SOAP-based architecture.

During these sessions, I also gained an understanding of SOAP‑specific mechanisms, such as XML message exchanges. This approach enabled me to assess the heaviness introduced by SOAP, both in terms of implementation complexity and communication overhead.

I am now able to deploy a SOA based on SOAP; however, I would not choose this solution unless specific constraints required it, preferring lighter approaches such as REST services in most use cases.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| N. Guermouche     | Deploy and configure an SOA using REST | 4 / 4 | Project |

REST architecture was then introduced as a lighter alternative to SOAP, resource‑oriented and based on the HTTP protocol. I was able to design and deploy RESTful APIs by rethinking and reimplementing the functionalities previously developed using SOAP.

This hands‑on experience allowed me to clearly understand the conceptual and practical differences between the two approaches: REST promotes simplicity, efficiency, and flexibility through the use of standard HTTP methods (GET, POST, PUT, DELETE), whereas SOAP enforces a strict structure and introduces additional overhead due to XML messaging.

Thanks to this experience, I am now able to deploy a REST based SOA.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| N. Guermouche     | Design, develop, and deploy a microservice architecture | 4 / 4 | Project |

This skill represents the culmination of the course and was fully applied within the context of the final project. I was able to design microservices by performing a functional decomposition, with each service being autonomous and responsible for a specific functionality.

I also implemented the essential components of a complete microservices architecture, such as a configuration server and a discovery service.

This experience allowed me to understand the key advantages of such an architecture, including modularity, scalability, resilience, and service independence. As a result, I was able to design, develop, and deploy a complete distributed application.


| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| N. Guermouche     | Understand the related concepts and features of a Service Oriented Architecture | 4 / 4 | Project |

I understand the main concepts and principles of Service Oriented Architecture (SOA). I am able to identify services, understand their roles and interactions, and explain how they communicate within a distributed system. I also understand the benefits of SOA, such as modularity, reusability, and interoperability between applications.


## Source

</div>



