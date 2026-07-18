# ⚽ AI-Powered Football Academy Registration Agent (n8n Automation)

An intelligent, production-ready AI Automation workflow built with **n8n** that completely automates the student registration and payment tracking process for a sports academy. It parses messy, natural language inputs in Moroccan Darija, cleans the data, calculates dynamic subscription intervals, and updates Google Sheets instantly.

---

## 🚀 Features

* **Advanced LLM Parsing:** Leverages a custom-prompted AI Agent (Groq/OpenAI) to extract structured details (`first_name`, `last_name`, `amount`, `date`) from raw chat messages, handling flexible sentence structures perfectly.
* **Smart Data Processing (JavaScript):** Features an integrated Code Node to sanitize JSON string outputs from the AI layer and enforce reliable object parsing.
* **Automated Expiry Calculations:** Automatically computes the dynamic subscription expiration date (`expiry_date`) exactly one month from the time of registration.
* **Google Sheets Sync:** Appends a clean, structured data row to the academy spreadsheet automatically with zero manual entry.

---

## 🛠️ Architecture & Tech Stack

The workflow follows a strict, streamlined linear data highway:
`Chat/Webhook Trigger` ➡️ `AI Agent (LLM Layer)` ➡️ `JavaScript Code Node` ➡️ `Google Sheets API (Append Row)`

* **Automation Engine:** n8n
* **AI Model Stack:** Groq Chat Model / Simple Memory
* **Language/Logic:** JavaScript (ECMAScript)
* **Data Store:** Google Sheets API

---

## 📂 How to Use This Workflow

1. Download the `football-academy-automation.json` file from this repository.
2. In your n8n workspace, create a new workflow, click on the top right menu, and select **Import from File** to upload the JSON.
3. Configure your Google Sheets Node credentials using OAuth2.
4. Set up your Google Sheet with the following first-row headers: 
   `الاسم` | `الكنية` | `المبلغ` | `التاريخ` | `تاريخ انتهاء الاشتراك`
5. Save, activate the workflow, and start testing!
