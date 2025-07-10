# 🪙 Bitcoin Price Prediction with Machine Learning

Predict the future price of Bitcoin for the next 30 days using **Support Vector Regression (SVR)**. This project demonstrates time series forecasting with historical price data and applies machine learning to capture market trends.

## 📌 Project Overview

In this project, we:

* Load historical Bitcoin price data
* Preprocess and shift the data to build a supervised learning model
* Train an SVR model to forecast future prices
* Predict Bitcoin prices for the next 30 days

## 🔍 Technologies Used

* Python 3
* NumPy
* Pandas
* Scikit-learn
* Matplotlib (optional for visualization)

## 📂 Dataset

The dataset used is a CSV file containing historical Bitcoin prices with date and closing price.


---

## ⚙️ How It Works

### 1. Data Preparation

* Load the dataset using `pandas`
* Drop the `Date` column (we focus only on price)
* Create a target column `Prediction` by shifting the price by 30 days

### 2. Feature & Label Creation

* `X` (features): All current prices except the last 30 rows
* `y` (labels): Future prices (30 days ahead), excluding the last 30 entries

### 3. Model Training

* Use `SVR(kernel='rbf')` from `scikit-learn`
* Train on the `X` and `y` datasets

### 4. Prediction

* Create a test set `X_forecast` (last 30 values)
* Predict the next 30 days of prices using the trained model


---

## 📌 Notes

* This is a basic regression project; it does not take into account external market signals or technical indicators.
* SVR works well for small datasets but may not capture large-scale volatility accurately.
* For production-level predictions, consider using LSTM, ARIMA, or hybrid models.

