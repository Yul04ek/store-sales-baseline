# 🧠 Store Sales Forecasting (Kaggle)

Minimalist baseline solution for the [Store Sales Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) competition on Kaggle.

## 🔍 Problem

Predict daily sales for multiple product families across different stores in Ecuador.  
The data includes calendar, promotion flags, and location information.

## 📦 Solution Summary

- ⏱️ Model: LightGBM Regressor  
- 🔁 Target: `log1p(sales)`  
- 🧩 Features:
  - `month`, `dayofweek`, `is_holiday`, `is_weekend`
  - `onpromotion`, `store_nbr`, `family`, `city`, `state`
- 🧹 Clean categorical encoding (`astype('category')`)
- ❌ No lag/rolling features for clarity and stability

## 📈 Results

- 🔄 CV (RMSLE): ~1.21  
- 🏁 Public LB: **0.8395 RMSLE**

## 🚀 How to Run

```bash
pip install lightgbm pandas scikit-learn
# store-sales-baseline
 LightGBM baseline for Kaggle time series forecasting
