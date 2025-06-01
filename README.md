# 🛡️ Global Attack Detection Fusion Model

A unified **Fusion Classifier** built on top of specialized models for **Malware**, **Phishing**, **DDoS**, and **IoT Network Attacks**. This global model leverages ensemble learning to enhance cyber threat detection accuracy across varied attack surfaces, with visual interfaces, interactive simulations, and evaluation metrics.

---

## 📌 Overview

In the current threat landscape, relying on a single model for intrusion detection is insufficient. This project introduces a **Global Fusion Model** that consolidates predictions from four attack-specific classifiers:

- **Malware Detection Model**
- **Phishing Detection Model**
- **DDoS Attack Classifier**
- **IoT Network Intrusion Model**

The fusion classifier acts as a decision-maker, improving generalization across datasets, especially with casual/random sampling, noisy inputs, or real-time packet streams.

---

## 🧠 Attack-Specific Models

|        Model         |           Technique          | 
|----------------------|------------------------------|
| Malware Detector     |   Graph Sage + OOD Testing   |
| Phishing Classifier  | Graph Sage + Casual sampling | 
| DDoS Detector        | Graph Sage + Casual sampling | 
| IoT Intrusion Model  | Graph Sage + Casual sampling | 

Each model is trained and validated individually before being integrated into the **fusion classifier**.

---

## 🧪 Global Fusion Model

**Architecture**:  
The fusion classifier is built using a **meta-learning approach**, primarily:
- Soft Voting
- Weighted Averaging
- Stack Ensemble

**Features**:  
- Attack-type-specific preprocessing  
- Modular pipelines  
- Model confidence tracking  
- Automatic fallback to high-confidence local models  

---

## 🎛️ Visual Interface

The dashboard provides:
- Class probabilites of the attack predicted by model.
- Real-time threat classification
- Attack-type probability visualization
- Logs & system warnings
- Accuracy metric graphs
- Probable Reasoning to support gooabl and local prediction.

Built using **Streamlit** for simplicity and interaction.

---

## 🧪 Simulation & Causal Sampling

We simulate network behavior under random and causal sampling to:
- Test model generalizability
- Observe misclassification under adversarial inputs
- Measure performance degradation

**Simulation **:
- Visual Interface to demonstate the difference between casual and random sampling with respect to false positive rates and accuracy.

---

## 📊 Results

| Metric         |  Global Fusion Model  |
|----------------|-----------------------|
| Accuracy       | **88.00%**            |
| Precision      | **85.29%**            |
| Recall         | **96.67%**            |
| F1 Score       | **90.62%**            |
| ROC-AUC        | **96.25%**            |

---

## 🚀 Installation

```bash
git clone https://github.com/spk-22/Graph-Shield.git
python global.py
```
For visual inteface
```bash
python web_app.py
```
For simulation demonstrating difference between casual and random sampling, run the below HTML file for visualization
```bash
sampling_comparison_simulation.html
````
