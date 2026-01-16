# AI-Driven Network Intrusion Detection System (NIDS)

## 🛡️ Project Overview
This project implements an advanced machine learning pipeline designed to detect and classify malicious network traffic. Utilizing the **CIC-IDS2017** dataset, the system distinguishes between benign activity and 15 varieties of cyberattacks (including DDoS, Botnets, and Brute Force) with high precision.



## 🚀 Key Features
* **Scalable Data Pipeline:** Processed 2.8M+ records using **Stratified Sampling** to ensure statistical representation of rare attack classes.
* **Feature Engineering:** Conducted correlation analysis to remove redundant features, reducing dimensionality by 30% to optimize inference speed.
* **Class Imbalance Handling:** Implemented **SMOTE** (Synthetic Minority Over-sampling Technique) to synthesize minority attack samples, ensuring a robust detection rate.
* **Hybrid Benchmarking:** Evaluated performance across Gradient Boosting (XGBoost), Random Forests, and Deep Learning (MLP) architectures.

## 📊 Performance Results
The models were optimized for **Recall** to minimize the risk of undetected threats (False Negatives).

| Model | Precision | Recall | F1-Score | Training Time |
| :--- | :--- | :--- | :--- | :--- |
| **XGBoost** | **0.9967** | **0.9995** | **0.9981** | **6.79s** |
| Random Forest | 0.9969 | 0.9964 | 0.9966 | 73.64s |
| Neural Network (MLP) | 0.8900 | 0.9900 | 0.9400 | ~30s |
| Logistic Regression | 0.6984 | 0.9536 | 0.8063 | 15.41s |



## 🛠️ Tech Stack
* **Languages:** Python
* **Machine Learning:** XGBoost, Scikit-learn, Imbalanced-learn (SMOTE)
* **Deep Learning:** TensorFlow / Keras
* **Data Analysis:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn


## 📈 Analysis & Conclusion
The XGBoost model was selected as the production candidate. While the Neural Network showed high generalization, XGBoost achieved a superior 99.95% Recall while remaining 10x faster to train than traditional ensemble methods. This efficiency makes it ideal for high-throughput, real-time network monitoring environments.
