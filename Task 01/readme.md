# 🛒 Retail Sales EDA

## 📌 Project Overview
Before building predictive models, it’s important to **understand the data**.  
This project performs **Exploratory Data Analysis (EDA)** on a retail sales dataset to uncover initial patterns and generate business insights.  

We answer questions like:
- What are customers buying?
- When are they buying?
- Which products and countries drive the most sales?

---

## 🛠️ Steps Performed
1. **Load Data** – Using `pandas` to import the dataset.  
2. **Data Cleaning** –  
   - Handling missing values  
   - Removing duplicates  
   - Converting columns (e.g., `Date` → datetime)  
3. **Descriptive Statistics** – Mean, median, mode, standard deviation for `Sales` & `Quantity`.  
4. **Data Visualization** – Using `matplotlib` & `seaborn` to find trends.  
5. **Business Insights** – Key findings from the analysis.  

---

## 📊 Visualizations
- **Sales Trends Over Time** → Monthly & yearly sales (line chart)  
- **Top 10 Products by Sales** → Bar chart  
- **Top 10 Countries by Sales** → Bar chart (excluding UK if needed)  
- **Sales Distribution** → Histogram & Boxplot  
- **Sales by Day of Week/Hour** → Heatmap (buying behavior)  
- **Customer Sales Distribution** → Histogram (with log scale to handle skewness)  

---

## 💡 Key Business Insights
1. **Peak Sales Periods** – Most sales happen in **Q4 (Christmas season)**.  
2. **Best-Selling Products** – Small gift items & decorative pieces dominate.  
3. **Customer Behavior** – Majority of purchases occur on **weekdays, mostly mornings**.  
4. **Geographic Trends** – UK dominates, but **Germany & France** contribute significantly.  
5. **Revenue Distribution** – A few high-selling products/customers drive most of the revenue (**Pareto 80/20 rule**).  

---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

