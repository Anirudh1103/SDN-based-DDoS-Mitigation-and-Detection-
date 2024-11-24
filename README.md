# **SDN-Based DDoS Mitigation and Detection System**

## **Project Overview**
This project implements a **Software-Defined Networking (SDN)-based system for detecting and mitigating Distributed Denial-of-Service (DDoS) attacks** in real-time. Leveraging the centralized control and programmability of SDN, the system identifies malicious traffic patterns and dynamically applies mitigation strategies to ensure uninterrupted network services. The project combines traffic analysis, machine learning, and SDN control mechanisms to create a robust and scalable solution for modern network security challenges.

---

## **Key Features**
- **Real-Time Traffic Monitoring**: The SDN controller collects traffic flow statistics from OpenFlow-enabled switches in real time.
- **DDoS Detection**: Machine learning models analyze network traffic to detect abnormal patterns indicative of DDoS attacks.
- **Dynamic Mitigation**: Upon detecting malicious traffic, the controller deploys mitigation strategies like blocking IP addresses, rate limiting, or redirecting traffic to a honeypot.
- **Scalability**: Designed to work with large-scale networks by utilizing the centralized control of SDN.
- **Customizability**: Detection thresholds and mitigation policies can be fine-tuned to adapt to specific network requirements.

---

## **Architecture**
The system architecture consists of the following components:
1. **SDN Controller**: Manages network traffic and applies mitigation rules. (e.g., Ryu, ONOS, OpenDaylight)
2. **OpenFlow-Enabled Switches**: Forward traffic flows based on rules set by the controller.
3. **Traffic Analysis and Detection Module**: Uses machine learning models to detect malicious traffic patterns.
4. **Mitigation Module**: Executes appropriate responses to DDoS attacks.
5. **Dataset**: Uses the **CIC-DDoS2019 dataset** for training and testing.

---

## **Technologies Used**
- **Programming Languages**: Python (for data preprocessing, machine learning, and SDN integration).
- **Machine Learning**: Scikit-learn, Pandas, NumPy.
- **SDN Tools**: Ryu Controller, Mininet.
- **Traffic Analysis**: Matplotlib, Seaborn for visualization.
- **Traffic Generators**: Tools like Scapy, Hping, or LOIC for traffic simulation.

---

## **Workflow**
1. **Data Preprocessing**:
   - Load and preprocess the **CIC-DDoS2019 dataset** to extract meaningful features.
   - Normalize and split the dataset into training and testing subsets.
   
2. **Model Training and Evaluation**:
   - Train a machine learning model to classify traffic as benign or malicious.
   - Evaluate the model using metrics such as accuracy, precision, recall, and F1-score.

3. **SDN Integration**:
   - Deploy the trained model into the SDN controller for real-time traffic analysis.
   - Monitor network flows, classify them, and apply mitigation policies dynamically.

4. **Mitigation Actions**:
   - The SDN controller updates flow tables in switches to block, throttle, or reroute malicious traffic.

5. **Testing and Validation**:
   - Simulate DDoS attacks in a test environment using Mininet.
   - Measure system performance in terms of detection accuracy, latency, and impact on legitimate traffic.

---

## **Usage Instructions**

### **1. Setting Up the Environment**
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
