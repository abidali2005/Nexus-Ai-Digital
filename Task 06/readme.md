# 📊 Sales Forecasting with SARIMA

## 📌 Project Overview
This project focuses on building a **time series forecasting model** to predict sales using the **SARIMA (Seasonal AutoRegressive Integrated Moving Average with eXogenous regressors)** model.  
We worked step by step, from exploring the dataset to building the model and interpreting the results.

---

## 📝 Steps We Followed

### 1. Understanding the Data
- The dataset contained **daily sales data**.
- Since sales are recorded daily, the data may show **weekly seasonality** (patterns repeating every 7 days).
- Before applying forecasting models, we needed to **analyze trends, seasonality, and stationarity** in the data.

---

### 2. Stationarity and Differencing
- **Stationarity** means the average and variance of the data remain constant over time.
- Many forecasting models like ARIMA/SARIMA require the data to be stationary.
- We used **differencing (`d`)** to remove trends and make the data stationary.
- Seasonal differencing (`D`) was also applied if patterns repeated periodically.

---

### 3. Model Selection
We aimed to use **SARIMA**, which has two sets of parameters:

#### 🔹 Non-Seasonal Part: (p, d, q)
- **p (AR term)** → Number of past values used to predict the current value.  
- **d (Differencing)** → Times the series is differenced to make it stationary.  
- **q (MA term)** → Number of past forecast errors used to predict the current value.  

#### 🔹 Seasonal Part: (P, D, Q, m)
- **P (Seasonal AR term)** → Past seasonal values used for forecasting.  
- **D (Seasonal differencing)** → Seasonal differencing to remove seasonal trends.  
- **Q (Seasonal MA term)** → Past seasonal errors used for forecasting.  
- **m** → The length of the seasonality cycle (e.g., 7 for weekly seasonality in daily data).  

---

### 4. Initial Model Search
- At first, we attempted **Auto ARIMA**, which automatically finds the best parameters.  
- However, due to errors, we manually tuned the model.  

---

### 5. Fitting the SARIMA Model
- We applied **SARIMA** with parameters `(p, d, q)` and `(P, D, Q, m)`.  
- This model allowed us to capture:
  - Short-term dependencies (p, q).  
  - Long-term seasonal effects (P, Q).  
  - Stationarity adjustments (d, D).  

---

### 6. Interpreting the Results
- The model summary provided **coefficients** for AR and MA terms.  
- It also showed **AIC/BIC values**, which help compare model quality (lower values indicate better models).  
- Residual diagnostics were checked to ensure the model fit well.  

---

### 7. Forecasting
- Once fitted, the SARIMA model was used to **forecast future sales**.  
- The forecasts captured both:
  - **Trends** (long-term movement).  
  - **Seasonality** (weekly repeating patterns).  

---

## 📌 Key Learnings
- **ARIMA vs SARIMA** → ARIMA handles trends, while SARIMA extends it by also handling seasonality.  
- **Order `(p,d,q)`** handles non-seasonal effects.  
- **Seasonal order `(P,D,Q,m)`** captures repeating seasonal patterns.  
- Proper tuning of parameters is crucial for accurate forecasts.  
- Understanding the business context (e.g., weekly seasonality in sales) is as important as statistical methods.  

---

## ✅ Final Outcome
- We successfully applied **SARIMA** to daily sales data.  
- The model can now be used to forecast future sales, helping in **business planning and decision-making**.  
