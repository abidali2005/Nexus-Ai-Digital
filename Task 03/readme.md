# 📊 Customer Churn Prediction

## 📌 Project Overview
This project focuses on predicting **customer churn** — i.e., whether a customer will leave (churn) or stay (retain).  
Churn prediction is crucial for businesses because retaining existing customers is often more cost-effective than acquiring new ones.

---

## 📝 Steps We Followed

### 1. Understanding the Data
- The dataset contained **customer-level information** such as demographics, account details, and usage behavior.  
- The target variable was **Churn** (Yes/No), which we converted into binary labels (1 = churn, 0 = not churn).  

---

### 2. Data Preprocessing
- **Handling missing values** → Replaced or dropped missing data.  
- **Encoding categorical variables** → Converted text columns (e.g., Gender, Contract Type) into numerical format using techniques like one-hot encoding.  
- **Feature scaling** → Normalized numerical features (like MonthlyCharges, Tenure) to improve model performance.  

---

### 3. Exploratory Data Analysis (EDA)
- Analyzed distributions of features (e.g., age, charges, contract type).  
- Visualized **churn rates across different groups** (e.g., short-term vs long-term customers).  
- Identified patterns:
  - Customers with **month-to-month contracts** churn more.  
  - Customers with **higher monthly charges** are at higher risk.  
  - Customers with **longer tenure** are less likely to churn.  

---

### 4. Model Selection
We treated this as a **binary classification problem**.  
We experimented with multiple algorithms:
- **Logistic Regression**  
- **Random Forest**  
- **XGBoost**  
- **Support Vector Machines (SVM)**  

The goal was to find the model that gave the **best accuracy, precision, recall, and F1-score**.  

---

### 5. Model Training & Evaluation
- Split the dataset into **training and testing sets** (e.g., 80% train, 20% test).  
- Trained models on training data and evaluated on test data.  
- Key metrics:
  - **Accuracy** → Overall correctness.  
  - **Precision** → How many predicted churns were actual churns.  
  - **Recall (Sensitivity)** → How many actual churns we correctly predicted.  
  - **F1-score** → Balance between precision and recall.  
  - **ROC-AUC** → Overall ability of the model to separate churn vs non-churn.  

---

### 6. Feature Importance
- Identified the **most important features** influencing churn.  
- Examples:
  - **Tenure** (shorter tenure = higher churn risk).  
  - **Contract Type** (month-to-month contracts churn more).  
  - **Monthly Charges** (higher charges often lead to churn).  

---

### 7. Final Model & Predictions
- Selected the best-performing model (e.g., **XGBoost or Random Forest**).  
- Used the model to predict **probabilities of churn** for each customer.  
- Business can now:
  - Identify **high-risk customers**.  
  - Take preventive actions like **discounts, offers, loyalty programs**.  

---

## 📌 Key Learnings
- **Churn prediction is classification**, not regression.  
- Preprocessing (encoding + scaling) is critical for good model performance.  
- **Feature importance** helps businesses understand *why* customers leave.  
- **Evaluation metrics** beyond accuracy (especially recall & ROC-AUC) are important because missing churners can be very costly.  

---

## ✅ Final Outcome
- Built a machine learning model that predicts whether a customer will churn.  
- Business can now take **data-driven actions** to reduce churn and increase retention.  
