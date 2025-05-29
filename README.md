# 🛒 SalesSens: Store Sales Forecasting with Machine Learning

This repository contains my solution to a time-series forecasting problem based on sales data from **Corporación Favorita**, a major Ecuadorian-based grocery retailer. The goal is to accurately predict unit sales of thousands of items across various stores using machine learning models.

---

## 🎯 Project Goal

The aim of this project is to forecast future sales using historical data involving:

- Item and store metadata
- Dates
- Promotions
- Unit sales
---

## 📦 Models Used

To improve prediction accuracy, I experimented with and compared several gradient boosting models:

- **XGBoost** (`xgboost`)
- **CatBoostRegressor** (`catboost`)
- **LightGBM** (`lightgbm`)

These models were trained on engineered features and validated using cross-validation methods tailored for time-series data.

---

## 🧠 Context

Forecasting is a key problem in many industries. In retail, predicting demand helps prevent:

- Overstocking (leading to waste)
- Understocking (leading to lost sales and customer dissatisfaction)

This forecasting challenge involves many complexities, such as:

- Multiple store and item combinations
- Seasonal demand
- Ongoing promotions
- Introduction of new products and stores

By applying machine learning, we aim to automate and improve upon traditional, intuition-based forecasting methods.

---

## 📊 Evaluation Metric

The competition uses **Root Mean Squared Logarithmic Error (RMSLE)** as the evaluation metric:

\[
\text{RMSLE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} \left( \log(p_i + 1) - \log(a_i + 1) \right)^2}
\]

Where:
- \( n \) = number of predictions
- \( p_i \) = predicted sales
- \( a_i \) = actual sales

RMSLE penalizes under-predictions more than over-predictions, which is suitable for this scenario.

---

