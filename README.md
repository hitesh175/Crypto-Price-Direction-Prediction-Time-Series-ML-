
---

# 📈 Crypto Price Direction Prediction — Time-Series Machine Learning

This project builds a **time-series machine learning model** to predict short-term cryptocurrency price direction using high-frequency market data.

The objective is to classify whether the next 15-minute price movement will be **up or down**, based on historical price patterns and engineered technical features.

---

## 🎯 Project Objective

Financial markets are highly volatile and noisy.
This project aims to:

* Predict short-term crypto price direction
* Capture momentum and volatility patterns
* Avoid data leakage using strict chronological validation
* Compare multiple ML models and select the best performer

---

## 📊 Dataset

* 15-minute candlestick data
* 500,000+ records
* Multi-asset historical crypto data
* Features include open, high, low, close, volume

---

## 🛠 Methodology

### 1️⃣ Data Preparation

* Cleaned and structured time-series data
* Created target variable (price direction: up/down)
* Engineered 10+ lag-based and rolling volatility features

### 2️⃣ Feature Engineering

* Percentage returns
* Lag features
* Rolling statistics
* Volatility indicators

### 3️⃣ Model Development

Compared multiple classification algorithms:

* Logistic Regression
* K-Nearest Neighbors
* Decision Tree
* Random Forest

Applied **strict chronological train-test split** (last 365 days as out-of-sample test set) to eliminate data leakage.

---

## 🤖 Model Performance

* Baseline Accuracy: **52.12%**
* Optimized Random Forest Accuracy: **52.65%**
* Evaluated using:

  * Accuracy
  * Confusion Matrix
  * Feature Importance

The Random Forest model outperformed other classifiers under time-based validation.

---

## 📈 Key Insights

* Lag-based features improved predictive stability
* Volatility indicators helped capture short-term price behavior
* Time-aware validation is critical in financial ML to prevent leakage

---

## 🧰 Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

---

## ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/hitesh175/Crypto-Price-Direction-Prediction-Time-Series-ML-.git
cd Crypto-Price-Direction-Prediction-Time-Series-ML-
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook or script to train and evaluate the models.

---

## 🚀 Author

**Hitesh K R**
GitHub: [https://github.com/hitesh175](https://github.com/hitesh175)

---

