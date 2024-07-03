# Real Time Traffic Classification using Machine Learning in SDN

## Project Overview

The **Real Time Traffic classifier in SDN** project aims to classify different types of network traffic flows such as DNS, Telnet, Ping, Voice, Game, and Video. This is achieved using machine learning algorithms and the Distributed Internet Traffic Generator (D-ITG) tool to simulate network traffic within a Software Defined Network (SDN) topology. The setup uses Open vSwitch (OVS) and various machine learning models to perform real-time traffic classification based on packet and byte information.

## Components

1. **Distributed Internet Traffic Generator (D-ITG)**: Simulates various types of network traffic.
2. **Mininet**: Creates a virtual network for simulating SDN environments.
3. **Open vSwitch (OVS)**: An open-source implementation of a distributed virtual multilayer switch.
4. **Machine Learning Algorithms**:
    - Logistic Regression
    - K-Means Clustering
    - K-Nearest Neighbors
    - Support Vector Classifier (SVC)
    - Gaussian Naive Bayes (NB)
    - Random Forest Classifier

## Network Topology

The system uses Mininet to create a simple network topology with three hosts connected through a single Open vSwitch, controlled remotely.

## Installation Steps

### 1. Install D-ITG

Clone and install D-ITG from the repository:
'''sh
git clone https://github.com/jbucar/ditg
cd ditg
make
'''

### 2. Install Mininet
Download and install Mininet from the official website:
[Mininet Download](https://mininet.org/download/)

### 3. Install Open vSwitch
Download and install Open vSwitch from the official website:
[Open vSwitch Download](https://www.openvswitch.org/download/)

### 4. Start Mininet Topology
Create and start the Mininet topology with the following command:
sudo mn --topo single,3 --mac --switch ovsk --controller remote

### 5. Start Real-Time Prediction
Run the traffic classifier script with the following command:
python3 traffic_classifier_python3.py supervised
