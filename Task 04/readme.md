# Task 4: Optimizing Customer Churn Prediction (Advanced Classification)

## 📌 The Why  
A simple Logistic Regression model (from Task 3) gave us a starting point, but GlobalMart needs **higher accuracy and better insights** to reduce churn effectively.  
This task focuses on using **advanced models and evaluation techniques** to improve predictive power.  

---

## 📖 Description  
We enhance the churn prediction model by introducing **powerful algorithms** and **comprehensive evaluation metrics**.  
Instead of relying only on Logistic Regression, we use models like **Random Forest** and **XGBoost**.  
This allows us to capture more complex relationships in the data and make better business decisions.  

---

## 🛠️ Step-by-Step Guide  

1. **Feature Scaling**  
   - Apply scaling (e.g., `StandardScaler`) to numerical features.  
   - Ensures all features contribute fairly to the model.  

2. **Model Training**  
   - Train advanced models such as **Random Forest** and **XGBoost**.  
   - These models handle complex data patterns better than Logistic Regression.  

3. **Advanced Evaluation**  
   - Go beyond accuracy and evaluate using:  
     - **Precision** → Out of predicted churn customers, how many actually churned?  
     - **Recall** → Out of actual churn customers, how many did we capture?  
     - **F1 Score** → Balance between Precision and Recall.  

4. **Comparison**  
   - Compare performance of advanced models against Logistic Regression (Task 3).  
   - Discuss which performs better and why.  
   - Provide a **clear recommendation** on the best model for deployment.  

---

## 📊 Suggested Dataset  
- Use the **same churn dataset** from Task 3 for consistency.  

---

## 🎯 Expected Outcome  
- A **Jupyter Notebook** with:  
  - Scaling process.  
  - Training results of advanced models.  
  - Precision, Recall, F1 Score comparisons.  
  - Clear explanation of which model is best for GlobalMart and why.  

- Final Deliverable: A strong recommendation backed by advanced metrics, showing whether the Logistic Regression baseline or the new advanced model should be deployed.  
