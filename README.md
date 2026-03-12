# Collaborative Anti-Money Laundering Detection using Federated Learning

## Overview
This project presents a privacy-preserving Anti-Money Laundering (AML) detection system using Machine Learning and Federated Learning techniques. The system enables multiple financial institutions to collaboratively train a global model for detecting suspicious financial transactions without sharing sensitive customer data.
The project compares three different learning approaches:
- Centralized Machine Learning
- Incremental Learning
- Federated Learning with Differential Privacy
The goal is to improve fraud detection accuracy while maintaining strong data privacy.
## Problem Statement
Traditional AML systems operate within individual banks and rely on rule-based methods, which often fail to detect complex cross-bank money laundering patterns. Additionally, privacy regulations prevent financial institutions from sharing customer transaction data.
This project solves this problem using Federated Learning, allowing banks to collaboratively train models without exposing sensitive information.
## Technologies Used

- Python
- XGBoost
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SMOTE (Imbalanced-learn)
- Federated Learning
- Differential Privacy
## Dataset
Dataset used: **HI-Small_Trans.csv**
Features include:
- Transaction ID
- Sender Account
- Receiver Account
- Transaction Amount
- Timestamp
- Transaction Type
- Is-Laundering (Target Variable)
Dataset size:
- Original dataset: ~20,000 transactions
- Balanced dataset after SMOTE: ~40,000 transactions
## Methodology
### 1. Data Preprocessing
- Handling missing values
- Feature engineering
- Data normalization
- Class imbalance handling using SMOTE
### 2. Model Implementation
Three models were implemented and compared:
#### Centralized Learning
- All data stored in a single server
- XGBoost model trained on full dataset

#### Incremental Learning
- Dataset divided into smaller batches
- Model updated sequentially

#### Federated Learning with Differential Privacy
- Multiple clients (banks) train local models
- Model updates shared instead of raw data
- Gaussian noise added to protect privacy
- Global model aggregation using FedAvg
## System Architecture
1. Data Collection and Preprocessing  
2. Local Model Training at Each Bank  
3. Differential Privacy Protection  
4. Secure Model Aggregation  
5. Global Model Update  
6. Suspicious Transaction Alert Generation
## Results
Model performance comparison:

| Model | Accuracy | Precision | Recall |
|------|------|------|------|
| Centralized Learning | 0.9995 | 0.72 | 0.21 |
| Federated Learning + DP | 0.9995 | 0.70 | 0.18 |
| Incremental Learning | 0.9995 | 0.64 | 0.15 |

Key observations:
- Centralized learning achieved the highest detection performance
- Federated learning provided strong privacy protection
- Incremental learning supported real-time data updates
## Key Features

- Privacy-preserving machine learning
- Multi-bank collaboration without data sharing
- Federated learning architecture
- Differential privacy implementation
- Automated suspicious transaction alert system
## Applications

- Financial fraud detection
- Banking risk management
- Anti-money laundering compliance
- Secure multi-institution AI systems
## Future Improvements

- Real-time fraud detection system
- Integration with banking APIs
- Graph-based anomaly detection
- Explainable AI for fraud detection
- Large-scale federated learning deployment

---

## Author

**Siva Hitesh Reddy K**

Integrated M.Tech – Computer Science and Engineering  
Specialization: Business Analytics  
Vellore Institute of Technology
