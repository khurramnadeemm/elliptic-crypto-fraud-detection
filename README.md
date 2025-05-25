# Elliptic Dataset – Cryptocurrency Transaction Classification

This project utilizes the publicly available Elliptic dataset to detect illicit cryptocurrency transactions on the Bitcoin blockchain using a range of machine learning models.

---

## Project Objective

To classify transactions into three categories:
- **Illicit**
- **Licit**
- **Unknown**

By applying machine learning, we aim to assist financial institutions and regulators in identifying potentially fraudulent blockchain activity and minimizing financial crime.

---

## Datasets & Approach

The project was divided into **two distinct analyses**:

1. **Transaction-Level Analysis**  
2. **Wallet-Level Analysis**  

For both, we implemented and compared five machine learning models:
- Logistic Regression  
- Random Forest  
- LightGBM  
- XGBoost  
- Multilayer Perceptron (MLP)

### Goal: Detecting Illicit Transactions

- **Primary Metric**: **Recall**  
  In fraud detection, **missing an illicit transaction is more dangerous** than flagging a false positive. Hence, recall was prioritized over precision.

---

## Models Performance Summary

**Wallet-Level Analysis**

| Model Name                | Precision | Recall | F1 Score | Micro-Average F1 |
| ------------------------- | --------- | ------ | -------- | ---------------- |
| **Random Forest**         | 0.909     | 0.780  | 0.840    | 0.989            |
| **XGBoost**               | 0.893     | 0.808  | 0.848    | 0.989            |
| **Multilayer Perceptron** | 0.842     | 0.412  | 0.553    | 0.976            |
| **LightGBM**              | 0.384     | 0.919  | 0.542    | 0.944            |
| **Logistic Regression**   | 0.491     | 0.057  | 0.102    | 0.964            |

**Transaction-Level Analysis**

| Model Name                | Precision | Recall | F1 Score | Micro-Average F1 |
| ------------------------- | --------- | ------ | -------- | ---------------- |
| **Random Forest**         | 0.965     | 0.719  | 0.824    | 0.980            |
| **XGBoost**               | 0.922     | 0.730  | 0.815    | 0.978            |
| **LightGBM**              | 0.608     | 0.740  | 0.667    | 0.951            |
| **Multilayer Perceptron** | 0.622     | 0.597  | 0.609    | 0.949            |
| **Logistic Regression**   | 0.323     | 0.704  | 0.443    | 0.883            |




### Key Takeaways:

- **XGBoost** and **Random Forest** consistently provided the **best balance** between **precision** and **recall** on both transaction and wallet levels.
- **LightGBM** demonstrated **high recall**, which is valuable in use cases where **sensitivity is more critical than precision**.
- **Logistic Regression** underperformed, particularly in wallet-level analysis, showing limitations for **complex, imbalanced datasets**.
- We recommend **XGBoost** for its **robust balance**, making it suitable for **practical deployment in fraud detection systems**.

---

## Team Members

- Mohammad Khurram – 25902  
- Muhammad Saifuddin Khan – 26036  
- Mohammad Ashar – 26099  
- Soban Ahmed Siddiqui – 26646  
- Syed Hashaam Ahmed – 26104  
