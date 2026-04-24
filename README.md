# 🚀 AI-Powered Loan Risk Automation (n8n + GenAI + Webhooks)

An end-to-end financial analytics automation project that combines **workflow automation** and **Generative AI** to:

- 📊 Automate loan portfolio risk reporting  
- 🤖 Generate AI-based loan explanations  
- 🌐 Provide real-time API responses using Webhooks  

Built using n8n, LLMs, and tested with Postman.

---

# 📌 Problem Statement

Loan risk analysis in financial institutions is:

- Manual and time-consuming  
- Difficult to interpret for non-technical stakeholders  
- Lacking real-time explainability  

This project solves these challenges by automating insights and enabling AI-driven explanations.

---

# 🧩 Solution Overview

The system includes two workflows:

- 🔹 Automated Loan Risk Summary  
- 🔹 AI Loan Decision Explanation API  

---

# 🔄 Workflow 1: Automated Loan Portfolio Risk Summary

## 🎯 Objective
Generate a **weekly AI-driven loan risk report** and send it via email.

---

## ⚙️ Workflow Steps

1. **Schedule Trigger**
   - Runs weekly using Cron  

2. **Data Fetch**
   - Reads loan data from Google Sheets  
   - Includes:
     - Total loans  
     - Bad loan %  
     - High-risk grades (D, E, F)  
     - Interest rates  
     - Region-wise defaults  

3. **Data Processing**
   - JavaScript node cleans and structures data  

4. **GenAI Analysis**
   - Converts raw data into insights  

   **Prompt Example:**
   ```
   Summarize loan portfolio risk:
   - Highlight high-risk segments
   - Identify trends
   - Explain in simple business terms
   ```

5. **Output**
   - Sends report via email  

---

## 🧠 Sample Output

> “18.4% of loans fall under high-risk grades (D–F).  
Higher defaults are linked to high DTI and low employment stability.  
The South region shows elevated risk levels.”

---

## 💼 Business Impact

- Reduces manual reporting  
- Enables proactive risk monitoring  
- Saves analyst time  

---

# 🔄 Workflow 2: AI-Based Loan Decision Explanation API

## 🎯 Objective
Provide **real-time AI explanations** for loan decisions using Webhooks.

---

## 🌐 Key Feature

- Acts as a **real-time AI backend service**
- Integrated with Postman for API testing  

---

## ⚙️ Workflow Steps

1. **Webhook Trigger**
   - Accepts POST requests  

   **Example Request:**
   ```json
   {
     "loan_id": "L001",
     "question": "Why is this loan risky?"
   }
   ```

2. **Fetch Loan Details**
   - Grade  
   - Interest Rate  
   - DTI  
   - Income  
   - Employment Length  
   - Loan Purpose  

3. **Data Processing**
   - Formats input using JavaScript  

4. **GenAI Reasoning**

   **Prompt Example:**
   ```
   Explain why this loan is risky:
   - Compare with a good loan
   - Highlight key risk factors
   - Keep explanation simple
   ```

5. **API Response**
   - Returns explanation via Webhook  

---

## 🧠 Sample API Response

```json
{
  "explanation": "This loan is high-risk due to high DTI and low income stability. Compared to good loans, this borrower has weaker repayment capacity."
}
```

---

## 💼 Business Impact

- Enables real-time decision explanation  
- Improves transparency  
- Reduces dependency on analysts  

---

# 🔌 API Testing

Tested using Postman:

1. Copy webhook URL from n8n  
2. Send POST request  
3. Receive AI-generated response  

---

# ⚙️ Tech Stack

- n8n (Workflow Automation)  
- LLM (Groq / OpenAI)  
- Google Sheets  
- Webhooks  
- Postman  

---

# 🔥 Key Highlights

- Built end-to-end automation system  
- Implemented real-time AI API  
- Combined data + automation + AI  

---


# 🚀 Future Improvements

- Dashboard integration (Power BI)  
- ML-based risk scoring  
- Production API deployment  

---

