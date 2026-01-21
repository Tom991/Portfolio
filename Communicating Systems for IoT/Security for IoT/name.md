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

We chose to further explore the module devoted to the analysis of an ANT+ heart rate monitor.

<figure align="center">
  <img width="695" height="373" alt="image" src="https://github.com/user-attachments/assets/dbabf5b7-5a16-4e14-8aeb-9ba66c887380"/>
  <figcaption style="font-size: 0.9em; color: #555;">
    Figure 1: Heart rate monitor
  </figcaption>
</figure>

This module made it possible to cover the entire analysis chain: from signal acquisition to the exploitation of protocol weaknesses. This involved putting into practice several complementary approaches, such as signal capture and inspection using a Software Defined Radio, the implementation of a sniffer based on an nRF52840 chip, analysis of the fields, and reconstruction of the frame format. Finally, an identity spoofing attack was carried out, aiming to reproduce the behavior of a legitimate sensor.

The final (assessed) lab focused on an introduction to web security. Its objective was to analyze the security of a web application (JavaScript/PHP/MySQL), identify server-side and client-side vulnerabilities, and understand their exploitation methods. The lab was divided into two parts: server-side attacks and client-side attacks.

On the server side, the lab highlighted typical vulnerabilities such as SQL injections, file inclusions, and poor configurations (excessive permissions, information exposure via phpinfo, etc.), while also leading us toward best practices.

On the client side, the second part focused on attacks such as XSS (execution of HTML/JS in the browser), CSRF, and session hijacking through session cookie reuse, as well as their countermeasures: output encoding, CSRF tokens, and cookie security.

### Cryptology section

The objective of this lab was to implement our own certification authority in order to secure device authentication, relying on the mbedTLS library. mbedTLS is a lightweight C library designed by ARM to facilitate the implementation of TLS communications on embedded systems.

In the first part, we determined cryptographic parameters based on standard recommendations.

In the second part, we created our own Certification Authority (CA): generation of the CA key pair, creation of a self-signed root certificate, then generation of a key pair for a device, creation of a CSR (Certificate Signing Request), and issuance of a certificate signed by the CA. We then verified the validity of the device’s certificate.

Finally, we simulated a Man-In-The-Middle (MITM) attack on an unsecured channel to illustrate the risks of message interception and modification, and to show that authentication of keys and certificates is essential to counter this type of attack.

### Quantum section

During the practical component related to quantum communication, we carried out a lab session aimed at introducing the principles of quantum cryptography through the study of quantum key distribution using an instrumented experiment.

We were thus able to implement a secure communication system based on two distinct channels: a classical channel, used for the public exchange of information, and a quantum channel, which exploits the properties of light to distribute a secret key between two users. This setup provides a concrete illustration of how the laws of quantum mechanics make it possible to guarantee the security of information exchanges.


<figure>
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e0a82eb7-ffe1-4486-90b9-f04d092f44ec" />
  <figcaption></figcaption>
</figure>


### Innovative Project

### Analytical


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


