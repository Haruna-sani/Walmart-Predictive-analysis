# 📈 Walmart Predictive Analysis

This repository presents a deep learning-based time series analysis to predict the **adjusted closing price** of Walmart stock. Three different architectures were evaluated: **LSTM**, **CNN+GRU-LSTM**, and **CNN+Bi-LSTM**, using varying **learning rates** and **batch sizes**.

---

## 📊 Project Overview

The goal of this study is to compare the performance of multiple neural network models for financial time series forecasting. The models were trained and evaluated using two different batch sizes (`64` and `128`) and five different learning rates:  
`0.00001`, `0.0001`, `0.001`, `0.01`, `0.1`.

---

## 🧠 Models Used

- **LSTM (Long Short-Term Memory)**
- **CNN + GRU-LSTM**
- **CNN + Bi-LSTM (Bidirectional LSTM)**

Each model was evaluated based on **R-squared (R²)** score to assess prediction accuracy.

---

## 📁 Data

The dataset contains historical Walmart stock prices, including:
- `Date`
- `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`

---

## ⚙️ Results Summary

### 🔹 Batch Size: 64

| Model             | Optimal Learning Rate(s) | Max R² Score |
|------------------|--------------------------|--------------|
| **LSTM**         | `0.001`                  | **0.999**    |
| **CNN+GRU-LSTM** | `0.0001`                 | 0.997        |
| **CNN+Bi-LSTM**  | `0.0001`, `0.001`, `0.01`| 0.996        |

### 🔹 Batch Size: 128

| Model             | Optimal Learning Rate | Max R² Score |
|------------------|-----------------------|--------------|
| **LSTM**         | `0.001`               | **0.998**    |
| **CNN+GRU-LSTM** | `0.001`               | 0.997        |
| **CNN+Bi-LSTM**  | `0.0001`              | 0.996        |

---

## Optimal Model Selection

Based on the R² performance across different configurations:

- The **LSTM model** consistently outperformed the hybrid models under both batch sizes.
- At a **batch size of 64**, it achieved a near-perfect R² of **0.999** with a learning rate of **0.001**.
- Increasing the batch size to 128 slightly reduced performance, with R² dropping to **0.998**, but still remaining superior.

---

## Recommendation

- **Preferred Model**: `LSTM`
- **Optimal Configuration**:
  - **Batch Size**: `64`
  - **Learning Rate**: `0.001`
  - **R² Score**: `0.999`

For best results in predicting Walmart's adjusted close price, the standalone **LSTM model** trained with a **batch size of 64** and a **learning rate of 0.001** is recommended.

---

## Future Work

- Introduce attention mechanisms to capture long-range dependencies.
- Incorporate external economic indicators for multi-input forecasting.
- Experiment with transfer learning using pretrained time-series models.

---
