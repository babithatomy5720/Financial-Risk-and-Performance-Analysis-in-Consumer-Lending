🚀 AI-Powered Loan Risk Automation System

An end-to-end financial analytics automation project that uses workflow automation + Generative AI to:

📊 Automatically generate loan risk summaries
🤖 Explain loan decisions using AI
🌐 Provide real-time responses via API (Webhook)

Built using n8n
, LLMs, and API testing via Postman
.

📌 Problem Statement

In financial institutions:

Loan risk reporting is manual and repetitive
Explaining why a loan is risky takes analyst effort
No real-time system exists for decision explanations

👉 This project solves these problems using automation + AI reasoning.

🧩 Solution Overview

This system consists of two intelligent workflows:

🔹 1. Automated Loan Portfolio Risk Summary
🎯 Objective

Generate a weekly AI-based loan risk report and send it via email.

🔄 Workflow Steps
⏰ Step 1: Schedule Trigger
Runs automatically on a weekly basis
📊 Step 2: Fetch Loan Data
Reads data from Google Sheets
Includes:
Total loans
Bad loan percentage
High-risk grades (D, E, F)
Interest rates
Region-wise defaults
⚙️ Step 3: Data Processing
JavaScript node formats and aggregates the data
🤖 Step 4: GenAI Analysis
LLM converts raw metrics into business insights

Prompt Logic:

Summarize loan portfolio risk:
- Highlight high-risk segments
- Identify trends
- Explain in simple business language
📤 Step 5: Output
Sends report via email (Gmail node)
🧠 Sample Output

“18.4% of loans fall under high-risk categories (D–F).
Higher defaults are observed among borrowers with high DTI and low employment stability.
The South region shows elevated risk levels.”

💼 Business Value
Automates reporting
Saves analyst time
Enables proactive risk monitoring
🔹 2. AI-Based Loan Decision Explanation API
🎯 Objective

Provide real-time AI explanations for loan decisions using a Webhook.

🌐 Key Feature

👉 Acts like a mini backend AI service
👉 Integrated with Postman for testing

🔄 Workflow Steps
🧑‍💻 Step 1: Webhook Trigger
Accepts POST request

Example Request:

{
  "loan_id": "L001",
  "question": "Why is this loan risky?"
}
📊 Step 2: Fetch Loan Details
Retrieves:
Grade
Interest rate
DTI
Income category
Employment length
Loan purpose
⚙️ Step 3: Data Formatting
JavaScript node structures the input
🤖 Step 4: GenAI Reasoning

Prompt Example:

Explain why this loan is risky:
- Compare with a good loan profile
- Highlight key risk factors
- Keep explanation simple
📤 Step 5: API Response
Returns AI-generated explanation via Webhook
🧠 Sample Response
{
  "explanation": "This loan is high-risk due to a high DTI (38%) and low income stability. Compared to good loans, this borrower has weaker repayment capacity."
}
💼 Business Value
Real-time explainability
Improves transparency
Reduces dependency on analysts
🔌 API Testing

API endpoints were tested using Postman
.

Steps:
Copy webhook URL from n8n
Send POST request via Postman
Receive AI-generated response instantly

⚙️ Tech Stack
n8n
 – Workflow automation
LLM (Groq / OpenAI) – AI reasoning
Google Sheets – Data source
Webhooks – API layer
Postman
 – API testing
🔥 Key Highlights
Built end-to-end automation system
Developed real-time AI API using Webhooks
Combined:
Data analytics
Automation
AI insights

🚀 Future Enhancements
Integration with dashboards (Power BI)
Add ML-based risk scoring
Deploy as production API
