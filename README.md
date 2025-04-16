# Network Traffic Anomaly Detection Using Machine Learning

**Author**  
Arish Dhingra

---

## Executive Summary

This project explores the use of machine learning to detect anomalies in network traffic — particularly malicious behavior such as Distributed Denial-of-Service (DDoS) attacks. Using the CICIDS 2017 dataset, the project performs exploratory data analysis (EDA) and develops a baseline logistic regression model to distinguish between benign and malicious traffic. The initial model achieves near-perfect accuracy, forming a strong foundation for further model enhancement and eventual real-time deployment.

---

## Rationale

In today’s hyper-connected world, even home and small business networks face persistent security threats. Most users have no visibility into what’s happening in their network traffic until it's too late. This project addresses that gap by applying machine learning techniques to identify abnormal activity in network logs — potentially helping detect threats like botnets, scanning, infiltration, and brute-force attempts before damage occurs.

---

## Research Question

**Can we detect anomalies in network traffic that may indicate suspicious or malicious activity using machine learning models trained on historical traffic patterns?**

---

## Data Sources

- **Primary dataset**: CICIDS 2017 (Canadian Institute for Cybersecurity)  
  - [Link to dataset](https://www.unb.ca/cic/datasets/ids-2017.html)  
  - Focused on `Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv`, which includes both benign and DDoS traffic.
- Future plan: augment with **live network traffic** from a home network using tools like Zeek and Wireshark.

---

## Methodology

- **Data Preprocessing**:
  - Cleaning missing and infinite values.
  - Removing features with extreme magnitudes or constant values.
  - Encoding labels and scaling numeric features.
- **Exploratory Data Analysis (EDA)**:
  - Correlation heatmaps.
  - Feature distributions and boxplots by traffic type.
- **Baseline Modeling**:
  - Logistic Regression to classify benign vs. attack traffic.
  - Model evaluation using classification report, confusion matrix, and ROC AUC.

---

## Results

| Metric        | Result     |
|---------------|------------|
| Accuracy      | 99.85%     |
| Precision     | 1.00       |
| Recall        | 1.00       |
| F1-Score      | 1.00       |
| ROC AUC Score | 0.9998     |

- Logistic Regression achieved near-perfect separation between benign and DDoS traffic.
- Confusion matrix showed only 67 misclassifications out of 45,000+ samples.
- Correlation analysis revealed redundant and highly correlated features, which were removed for clarity and model stability.

---

## Next Steps

- Implement additional models (Random Forest, Isolation Forest, Autoencoder).
- Explore unsupervised anomaly detection for unlabeled traffic.
- Perform feature selection and hyperparameter tuning.
- Set up real-time data pipeline using Zeek or Wireshark.
- Deploy the model using Docker + AWS and create a web-based dashboard or Slack alert integration.

---

## Outline of Project

- [Link to notebook 1: EDA + Data Cleaning](https://github.com/arishdhingra1/detect-anomalies-in-network-traffic-/blob/main/code/project.ipynb)

---

## Contact and Further Information

For questions, collaboration, or more details, please contact:  
📧 arish_dhingra@outlook.com  
