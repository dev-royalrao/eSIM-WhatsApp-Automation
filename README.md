# 📱 eSIM WhatsApp Support Automation (Phase 1) – Powered by n8n

In an increasingly connected world, automating customer support is essential to deliver fast, reliable, and human-friendly service. This project presents an intelligent WhatsApp-based automation system built with **n8n**, designed to streamline **eSIM request handling** using AI-like logic, human approvals, and email integration.

---

## 🚀 Overview

This automation handles incoming eSIM support messages via WhatsApp and performs the following:

- ✅ Extracts **NSCE** and **MSISDN** using regex
- ✅ Sends the ticket for **dual human approval** (YES/NO flow)
- ✅ If approved, sends an email to **Orange support**
- ✅ Waits for Orange’s reply using Gmail message ID tracking
- ✅ Logs all actions and updates to **Google Sheets**
- ✅ Sends the final response back to the customer on WhatsApp

---

## 🛠️ Tools & Technologies

- **n8n** – Workflow Automation
- **WhatsApp Business API / UltraMsg / Gupshup** – Messaging Integration
- **Gmail API** – Email automation and reply tracking
- **Google Sheets API** – Ticket logging and updates
- **JavaScript (Code nodes)** – Custom logic and regex processing
- **Regex** – For dynamic extraction of NSCE and MSISDN

---

## 📂 Folder Structure

```
📁 esim-whatsapp-automation/
├── workflows/
│   └── esim_support_workflow.json
├── screenshots/
│   └── flow-diagram.png
├── README.md
```

---

## 🔄 Workflow Highlights

- 📥 **Trigger:** WhatsApp message received via webhook
- 🔍 **Extract:** Regex-based NSCE/MSISDN parsing
- 👤 **Approval 1:** Sent to human approver (YES/NO)
- 📧 **Email:** Draft sent to Orange support if approved
- 🕒 **Wait:** Response tracked using Gmail Message-ID
- 👤 **Approval 2:** Orange’s reply shared for final approval
- 📤 **Notify:** Final message sent to customer
- 📝 **Log:** All steps recorded in Google Sheets

---

## 🧠 Key Features

- Dynamic message ID tracking for accurate email response mapping  
- 12-hour timeout logic for approvals and escalations  
- Centralized Google Sheet logs for reporting and transparency  
- Reusable JS code for response validation and extraction  

---

## 📋 Prerequisites

- n8n (self-hosted or cloud)
- WhatsApp Business API credentials (UltraMsg / Gupshup / Twilio)
- Gmail account with OAuth2 credentials in n8n
- Google Sheets document with editable access
- Basic knowledge of n8n workflows and credentials setup

---

## 🧪 How to Use

1. Clone this repository  
2. Import `esim_support_workflow.json` into your n8n instance  
3. Configure your **Webhook**, **Gmail**, and **Google Sheets** credentials  
4. Set up your WhatsApp webhook provider  
5. Test the automation using sample eSIM request messages

---

## 📌 Example Input

```
Hello, my eSIM issue:
NSCE: ABC12345
MSISDN: 9876543210
```

---

## 👨‍💻 Author

**Royal Rao**  
🎓 M.Tech Data Engineering @ IIT Jodhpur  
📧 [royalrao.edu@gmail.com](mailto:royalrao.edu@gmail.com)  
🔗 [LinkedIn](https://linkedin.com/in/royal-rao-443298228)  
💻 [GitHub](https://github.com/dev-royalrao)

---

## 📄 License

MIT License – Feel free to fork, modify, and build upon it!
