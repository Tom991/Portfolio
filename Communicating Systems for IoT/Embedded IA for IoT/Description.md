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

The first laboratory session aimed to consolidate the fundamentals of the course. Its objective was to design, train, and optimize a fall detection model based on images, relying on the CAUCAFall dataset. To achieve this, we used a CNN through TensorFlow and Keras, while taking into account constraints related to embedded integration (lighter model and optimization).


This lab allowed us to face a supervised classification problem and to understand that a good score on the training set is not sufficient: a relevant model must primarily generalize well in order to account for dataset variability. We therefore deepened our understanding of overfitting and the importance of validating the model on unseen data.


Finally, this work was an opportunity to review several fundamentals related to data manipulation: loading, visualization, preprocessing, and then splitting the dataset into training, validation, and test sets.

### Innovative Project


As part of the innovative project, I was confronted with an embedded AI issue. The project focused on a quadruped robot (SOLO12) integrating an FPGA, on which a Multi-Layer Perceptron (MLP) neural network is deployed to enable the robot to move within its environment.

The MLP was already present in the initial project, but we redeveloped a new version in order to better understand the overall system architecture, hardware constraints, and implementation choices. The main challenge was therefore to design an MLP capable of processing 16-bit fixed-point inputs, as well as the associated weights, while complying with the resource constraints imposed by the FPGA target.

At first, I designed a simple perceptron, then progressively increased its complexity to meet functional requirements (support for n inputs, weight handling, accumulation). The “Layer” and “MLP” components mainly consisted of hierarchical structures based on the generation and interconnection of multiple perceptrons, and then multiple layers.

The part that increased in complexity the fastest was the analysis of the testbench. Indeed, a Layer instantiates multiple perceptrons and an MLP instantiates multiple layers: the size of the simulations grows very quickly, which makes validation more difficult (simulation time, volume of signals to observe, multiplication of test cases). It therefore becomes challenging to verify everything “by hand”.

### Analytical

#### Learning Outcomes Assessment – AI at the Edge

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| P. Leleux     | Able to explain the main concepts of Artificial Intelligence at the edge | 4 / 4 | Report from practical |

During this course unit, I consolidated and deepened my understanding of the fundamental concepts of artificial intelligence applied to IoT systems, particularly those related to supervised learning and their execution at the edge. I am now able to explain the theoretical principles underlying embedded AI.

In particular, I gained a clear understanding of the essential differences between cloud-based execution and edge-based execution. AI at the Edge offers major advantages in terms of latency, bandwidth consumption, data confidentiality, and system autonomy. However, these benefits come with strong constraints in terms of memory capacity, computational power, and energy consumption.

The general steps involved in implementing an AI workflow such as data preparation, model training, and model validation are similar to those studied in the AI course taken last year. Nevertheless, this unit enabled me to understand the specific techniques required to adapt AI models to embedded targets.

As part of the practical sessions, I applied model optimization methods suited to embedded AI. In particular, I implemented pruning techniques. In addition, I used TensorFlow Lite (TFLite) to perform weight quantization, significantly reducing the memory cost of the models.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| P. Leleux     | Dimension an AI tool for an application at the edge: communication bandwidth, latency, realiability of the model decisions, and privacy. | 4 / 4 | Report from practical |

During the laboratory sessions as well as the innovative project, I was required to design artificial intelligence solutions tailored for edge execution, taking into account key constraints such as communication bandwidth, latency, and reliability.

As part of the Fall Detection laboratory work, the CNN-based model had to be optimized for embedded deployment. I applied previously studied techniques such as pruning and quantization, which significantly reduced the model size while maintaining acceptable performance.

During the innovative project, data processing was carried out directly on an FPGA, thus avoiding large data transfers to the cloud. The choice of a compact MLP model quantized to 16 bits helped minimize the volume of exchanged data.

These projects enabled me to put into practice latency and performance optimization, in line with the constraints of embedded processing.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| P. Leleux     | Set up a machine learning workflow on heterogeneous IoT data (tabular, images, temporal series) | 3 / 3 | Report from practical |

This course, together with the associated practical work, enabled me to understand and implement the different stages of a machine learning workflow, adapted to the various types of data encountered in IoT systems.

During the practical sessions, I mainly worked on an application using image data as input. In doing so, I covered a large part of the workflow, from data preparation to model optimization and evaluation.

As part of the practical work, I carried out data preparation tasks (exploration, visualization, normalization) and built the training, validation, and test datasets. I then designed, trained, and evaluated a CNN for image analysis.

Overall, these practical sessions allowed me to concretely apply all the stages of a machine learning workflow, with the exception of the data collection and cleaning phases, which are particularly time- and resource-intensive. Nevertheless, I believe I have gained a solid overall understanding of the workflow and its adaptations to the constraints of IoT systems.

| **Instructor** | **Learning Outcome** | **Self‑Assessment (AE)** | **Evaluation Method** |
|---------------|----------------------|---------------------|----------------------|
| P. Leleux     | Use Python machine learning libraries and compression methods | 4 / 4 | Report from practical |

During the Embedded AI for IoT course, I worked with several Python libraries dedicated to machine learning, notably TensorFlow and Keras, as well as data manipulation and visualization tools such as NumPy and Matplotlib. These libraries enabled me to design, train, evaluate, and optimize machine learning models specifically tailored to the constraints of IoT systems.

</div>
