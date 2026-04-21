
# 🚀 Urban Service Demand Surge Prediction (SBPI + ML)

## 📌 Overview

This project focuses on predicting **urban service demand surges** using **New York City 311 residential noise complaint data**. Unlike traditional approaches that rely only on request volumes, this work incorporates **operational stress** through a novel metric called **Service Backlog Pressure Index (SBPI)**.

The system uses **time-series feature engineering** and machine learning models like **XGBoost** and **TabNet** to classify whether a given day will experience a surge in service demand.

---

## 🎯 Key Contributions

* 📊 Introduced **SBPI (Service Backlog Pressure Index)** to capture system stress
* ⏱️ Applied **time-series analysis** (lags, rolling averages, trends)
* ⚡ Designed a **surge detection mechanism** using 95th percentile threshold
* 🤖 Built and compared **XGBoost** and **TabNet** models
* 📈 Evaluated performance using precision, recall, F1-score

---

## 🧠 Methodology

### 1. Data

* NYC 311 Service Request Data
* Training: **2022–2024**
* Testing: **2025 (future generalization)**

### 2. Feature Engineering

* Time-based features: day, month, weekend
* Lag features: 1–3 days
* Rolling statistics: 3-day & 7-day averages
* Trend features: growth indicators
* SBPI (backlog-based stress metric)

### 3. Surge Definition

* Surge = days where requests exceed **95th percentile threshold**
* Formulated as a **binary classification problem**

### 4. Models Used

* **XGBoost** (primary model)
* **TabNet** (deep learning for tabular data)

---

## 📊 Results

| Model   | Accuracy | Precision | Recall | F1 Score |
| ------- | -------- | --------- | ------ | -------- |
| XGBoost | 0.927    | 0.625     | 0.789  | 0.698    |
| TabNet  | 0.707    | 0.240     | 0.816  | 0.371    |

✅ **XGBoost outperformed TabNet**, achieving strong balance between precision and recall.

---

## 📈 Visualizations

* Daily request trends
* Surge vs Non-surge comparison
* SBPI trend over time
* Demand vs system stress interaction

---

## 🛠️ Tech Stack

* Python (Pandas, NumPy, Scikit-learn)
* XGBoost
* PyTorch TabNet
* Matplotlib / Seaborn

---

## ⚙️ How to Run

```bash
# Clone repo
git clone https://github.com/your-username/project-name.git

# Install dependencies
pip install -r requirements.txt

# Run model
python main.py
```
