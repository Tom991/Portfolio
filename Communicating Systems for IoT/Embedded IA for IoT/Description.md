# Embedded AI for IoT

## Description

<div align="justify">

The “Embedded AI for IoT” course is part of the “Communicating Systems for IoT” module. Its objective is to complement the artificial intelligence courses taught in the fourth year by incorporating the specific constraints of IoT and the principles of Edge AI. The course therefore focuses on adapting machine learning models to resource-constrained environments, as well as on the challenges involved in deploying them on embedded systems.

This course consists of six sessions. First, it aims to consolidate the foundations covered the previous year by reviewing the fundamental principles of AI, in particular the notions of supervised and unsupervised learning, as well as the key steps of an Edge AI workflow. The course then covers data collection, preprocessing, and data representations, before introducing the basics of classification and the associated evaluation methods.

A significant part is devoted to convolutional neural networks (CNNs), which are particularly useful for IoT applications such as vision, detection, and embedded classification. Finally, the last sessions address model optimization and compression techniques (model size reduction), which are essential to enable AI deployment on embedded devices.

This course was complemented by three practical laboratory sessions. During the first two, we developed a CNN designed to detect and distinguish falls. The final session was devoted to initiating the production of the final video.

The assessment for this course was based both on the submission of a Jupyter notebook, used as a report, and on an explanatory video presenting our approach, the chosen solutions, and the trade-offs made.

## Technical Aspects


I was able to put into practice the knowledge acquired during this course in two distinct contexts. On the one hand, during the laboratory sessions of the course. On the other hand, within the framework of the innovative project, where I reused these skills in a different environment (FPGA) from the one studied in class.

### Laboratory Work

The first laboratory session aimed to consolidate the fundamentals of the course. Its objective was to design, train, and optimize a fall detection model based on images, relying on the CAUCAFall dataset. To achieve this, we used a Convolutional Neural Network (CNN) through TensorFlow and Keras, while taking into account constraints related to embedded integration (lighter model and optimization).


This lab allowed us to face a supervised classification problem and to understand that a good score on the training set is not sufficient: a relevant model must primarily generalize well in order to account for dataset variability. We therefore deepened our understanding of overfitting and the importance of validating the model on unseen data.


Finally, this work was an opportunity to review several fundamentals related to data manipulation: loading, visualization, preprocessing, and then splitting the dataset into training, validation, and test sets.

### Innovative Project


As part of the innovative project, I was confronted with an embedded AI issue. The project focused on a quadruped robot (SOLO12) integrating an FPGA, on which a Multi-Layer Perceptron (MLP) neural network is deployed to enable the robot to move within its environment.

The MLP was already present in the initial project, but we redeveloped a new version in order to better understand the overall system architecture, hardware constraints, and implementation choices. The main challenge was therefore to design an MLP capable of processing 16-bit fixed-point inputs, as well as the associated weights, while complying with the resource constraints imposed by the FPGA target.

At first, I designed a simple perceptron, then progressively increased its complexity to meet functional requirements (support for n inputs, weight handling, accumulation). The “Layer” and “MLP” components mainly consisted of hierarchical structures based on the generation and interconnection of multiple perceptrons, and then multiple layers.

The part that increased in complexity the fastest was the analysis of the testbench. Indeed, a Layer instantiates multiple perceptrons and an MLP instantiates multiple layers: the size of the simulations grows very quickly, which makes validation more difficult (simulation time, volume of signals to observe, multiplication of test cases). It therefore becomes challenging to verify everything “by hand”.

</div>
