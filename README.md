# 📈 Stock Price Prediction using Machine Learning

This project analyzes and predicts the stock prices of selected companies using various machine learning models such as **Linear Regression** and **Random Forest Regressor**.

---

## 📌 Objective

To build predictive models using historical stock data to forecast the **next day's closing price**.

---

## 🗃️ Dataset

The data is fetched from [Yahoo Finance](https://finance.yahoo.com/) using the `yfinance` Python library. It includes daily stock prices for:

- Apple Inc. (`AAPL`)
- Alphabet Inc. (`GOOGL`)
- Microsoft Corp. (`MSFT`)
- Amazon.com Inc. (`AMZN`)
- Tesla Inc. (`TSLA`)
- NVIDIA Corp. (`NVDA`)
- JPMorgan Chase & Co. (`JPM`)
- Netflix Inc. (`NFLX`)
- PayPal Holdings Inc. (`PYPL`)
- BioMarin Pharmaceutical Inc. (`BMRN`)

---

## ⚙️ Workflow

### 1. 📥 Data Collection

- Used `yfinance` to download 3 years of daily data.
- Stored relevant columns: `Open`, `High`, `Low`, `Close`, `Volume`.
- Combined data for all tickers and labeled with a `Ticker` column.

### 2. 🧼 Exploratory Data Analysis (EDA)

- Checked for missing values.
- Plotted **closing prices** over time for each stock.

### 3. 📊 Feature Engineering

- Added a new column `Next_Close` which is the `Close` price of the **next trading day** (target variable).

### 4. 🧠 Models Used

#### ✅ Linear Regression

- Applied separately to each stock.
- Features used: `Open`, `High`, `Low`, `Volume`, `Close`
- Target: `Next_Close`
- Evaluated using **Mean Squared Error (MSE)** and **R² score**

#### ✅ Random Forest Regressor

- Used `RandomForestRegressor` from `sklearn.ensemble`.
- Applied per stock similarly.
- Compared performance with Linear Regression.

### 5. 📈 Results

- Plotted **actual vs predicted** closing prices for both models.
- Combined performance metrics into a comparison table for all stocks.

---

## 📦 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `yfinance`
- `sklearn`

---

## 🚀 Future Work

- Add LSTM (deep learning) models for time series predictions.
- Hyperparameter tuning with `GridSearchCV` or `RandomizedSearchCV`.
- Include technical indicators as additional features.

---



