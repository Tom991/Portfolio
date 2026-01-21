# Security for IoT

## Description

<div align="justify">

The course Security for IoT, which is part of the Communicating Systems for IoT curriculum, provides an introduction to computer security applied to connected objects. It presents the fundamental concepts of cybersecurity while highlighting the specific characteristics and constraints related to embedded systems.

The course is organized into ten lectures. The first part is dedicated to the foundations of computer security, while the second focuses on the principles of cryptography.

The first part initially offers an overview of key notions (definitions, terminology, and presentation of the IoT context), then explores the security of human–machine interfaces, particularly in web and application environments.

The course then addresses the vulnerabilities of major wireless communication protocols such as Wi‑Fi, BLE, and Zigbee, including the presentation and classification of attack types and common weaknesses.

Finally, the course opens up to more advanced topics, such as formal verification, embedded systems security, security at the processor micro‑architecture level, as well as an introduction to quantum communication from a security perspective.

This course also includes a section dedicated to cryptography, serving as an introduction to the field. It first presents the historical foundations of encryption through classical mechanisms (substitution, Caesar cipher, Vigenère). It then covers modern cryptographic primitives, including symmetric and asymmetric encryption, as well as digital signatures, and explains their contributions to security.

The course also introduces concepts of standardization, discussing the role of competitions and public analyses (for example around AES or RSA) as well as that of standardization bodies (NIST, IETF, ISO). Finally, it presents the logic behind modern communications, notably key agreement mechanisms (e.g., Diffie–Hellman).

In addition to the lectures, we attended a one‑day introduction to quantum communications. The morning sessions were theoretical, presenting some fundamentals of cryptography as well as the basic principles of quantum mechanics and their applications to secure communications. The afternoon was dedicated to hands‑on experimentation.

This instruction was complemented by five practical lab sessions. We first carried out three labs on the first part, serving as an introduction to security, followed by two labs focusing on cryptography. Assessment included the writing of a report at the end of the final lab of the first part, addressing the vulnerabilities of a web application. The cryptography component was assessed based on our portfolio.


## Technical Aspects

### Security section

I was able to make full use of all the knowledge acquired during the various practical lab sessions of this course, both for aspects related to security and those related to cryptography and quantum communication.

We chose to further explore the module devoted to the analysis of an ANT+ heart rate monitor. [

<figure>
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e0a82eb7-ffe1-4486-90b9-f04d092f44ec" />
  <figcaption>Figure 1: Heart rate monitor</figcaption>
</figure>

This module made it possible to cover the entire analysis chain: from signal acquisition to the exploitation of protocol weaknesses. This involved putting into practice several complementary approaches, such as signal capture and inspection using a Software Defined Radio, the implementation of a sniffer based on an nRF52840 chip, analysis of the fields, and reconstruction of the frame format. Finally, an identity spoofing attack was carried out, aiming to reproduce the behavior of a legitimate sensor.

The final (assessed) lab focused on an introduction to web security. Its objective was to analyze the security of a web application (JavaScript/PHP/MySQL), identify server-side and client-side vulnerabilities, and understand their exploitation methods. The lab was divided into two parts: server-side attacks and client-side attacks.

On the server side, the lab highlighted typical vulnerabilities such as SQL injections, file inclusions, and poor configurations (excessive permissions, information exposure via phpinfo, etc.), while also leading us toward best practices.



### Innovative Project

### Analytical



<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e0a82eb7-ffe1-4486-90b9-f04d092f44ec" />

#### Learning Outcomes Assessment – AI at the Edge

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| R. Cayre     | Understand the fundamentals of security |  / 4 | TP Report + Portfolio |



| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| R. Cayre     | Be able to identify security weaknesses in an IoT architecture |  / 3 | TP Report + Portfolio |



| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| R. Cayre     | Be able to assess the impact of exploiting a security vulnerability in an IoT architecture |  / 3 | TP Report + Portfolio |



| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| R. Cayre     | Be able to propose adequate security counter-measures |  / 3 | TP Report + Portfolio |



| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| R. Cayre     | Be able to design secure communication protocols for IoT |  / 3 | TP Report + Portfolio |



| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| R. Cayre     | Understand the secure quantic communcations |  / 3 | TP Report + Portfolio |

## Source


</div>
