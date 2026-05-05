# 📊 Financial Risk & Performance Analysis in Consumer Lending

## 📌 Project Overview
This project focuses on analyzing consumer lending data to evaluate **loan performance, risk factors, and profitability** in the FinTech industry. 

The goal is to simulate how financial institutions use **data analytics, SQL, Excel, Power BI, and automation** to make better lending decisions and manage risk.

---

## 🎯 Objectives
- Analyze loan portfolio performance
- Identify high-risk borrower segments
- Improve decision-making using data insights
- Build dashboards for business stakeholders
- Automate risk reporting using GenAI

---

## 🛠️ Tools & Technologies
- **SQL (PostgreSQL / Colab)** – Data cleaning & ETL  
- **Excel** – Exploratory Data Analysis (EDA)  
- **Power BI** – Interactive Dashboard  
- **n8n** – Workflow Automation  
- **GenAI APIs** – Automated insights & explanations  

---

## 🗂️ Dataset Description
The dataset includes:
- Borrower demographics (income, employment)
- Loan details (amount, term, purpose)
- Financial metrics (interest rate, DTI)
- Loan performance (good/bad loan, recoveries)

---

## 🔄 ETL Process (SQL)

### Extract
- Imported CSV dataset into SQL
- Validated schema and data types

### Transform
- Handled missing values (median imputation)
- Standardized categorical variables
- Created new features:
  - `profitability = total_pymnt - loan_amount`
  - `risk_flag` (1 = bad loan)

### Load
- Created cleaned dataset: `loans_cleaned`
- Exported for Excel & Power BI

---

## 📊 Excel Analysis (EDA)

Key insights:
- Loan amounts are concentrated in mid-income groups
- Higher **DTI → higher default probability**
- Longer loan terms → higher default rates
- Certain regions show higher loan demand

---

## 📈 Power BI Dashboard

### Key Features:
- 📌 Loan Summary Metrics (Total Loans, Avg Interest, Default Rate)
- 📌 Risk Heatmap (Grade vs Employment Length)
- 📌 Trend Analysis (Year-wise Loan Growth)
- 📌 Profitability Analysis
- 📌 Interactive Filters (Region, Income, Grade)

---

## 🤖 Automation (n8n + GenAI)

### 🔹 1. Loan Risk Summary Automation
- Weekly trigger
- Generates:
  - Risk exposure summary
  - Default trends
  - Regional risk insights

### 🔹 2. Loan Explanation System
- Input: Loan ID / User Query
- Output:
  - Why loan is risky
  - Key influencing factors
  - Human-readable explanation

---

## 🧠 Key Business Insights

- High-risk loans (Grades D–F) contribute disproportionately to defaults  
- Borrowers with **high DTI & low income** are most risky  
- **Short employment length** correlates with higher defaults  
- Region-based risk patterns suggest need for **localized credit policies**  

---

## 🚀 Recommendations

- Implement stricter approval for high DTI borrowers  
- Introduce dynamic interest pricing based on risk  
- Focus on low-risk segments for growth  
- Use automation for real-time risk monitoring  

---

## 📌 Future Improvements

- Add Machine Learning model for default prediction  
- Deploy dashboard on cloud  
- Real-time streaming data integration  

---

