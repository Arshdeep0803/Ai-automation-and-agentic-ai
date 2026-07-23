# 🤖 AI Support Triage Agent using n8n

## 📌 Project Overview

The **AI Support Triage Agent** is an AI-powered workflow developed using **n8n** to automate the initial handling of customer support requests. The workflow receives customer messages through a Webhook, analyzes them using an AI Agent, determines the support category and urgency, and intelligently routes the request for either an automated response or human review.

This project demonstrates how AI and workflow automation can improve customer support by reducing response time, automating repetitive tasks, and ensuring that urgent requests are reviewed by a human.

---

## 🎯 Project Objectives

- Automate customer support request processing.
- Classify customer messages using AI.
- Identify the urgency level of each request.
- Generate automatic responses for routine support cases.
- Escalate important or sensitive requests to a human reviewer.
- Improve customer support efficiency through workflow automation.

---

## ✨ Features

- ✅ Webhook Trigger to receive customer requests
- ✅ AI-powered message classification
- ✅ Support Category Detection
  - Technical
  - Billing
  - General
- ✅ Urgency Detection
  - Low
  - Medium
  - High
- ✅ Automatic AI-generated replies for routine requests
- ✅ Human-in-the-loop escalation for urgent cases
- ✅ Gmail integration for notifications
- ✅ Professional HTML email templates
- ✅ Conditional routing using IF Node
- ✅ Structured JSON output from AI Agent

---

## ⚙️ Workflow Architecture

```text
Customer Support Form
        │
        ▼
Webhook Trigger
        │
        ▼
AI Agent
(Classify Message)
        │
        ▼
Category + Urgency + Reply + Reason
        │
        ▼
IF Node
 ┌───────────────┐
 │               │
 ▼               ▼
Low Urgency   Medium/High Urgency
 │               │
 ▼               ▼
Automatic     Human Review
Email Reply   Email Notification
(Gmail)       (Gmail)
```

---

## 🛠 Technologies Used

- n8n
- AI Agent
- Google Gemini
- Gmail Node
- Webhook
- IF Node
- HTML
- JSON

---

## 🧪 Sample Input

**Customer Name**

Arashpreet Kaur

**Customer Email**

arashchahal788@gmail.com

**Customer Message**

```
Hello, I forgot my password. Can you tell me how to reset it?
```

---

## 🤖 AI Analysis

| Field | Result |
|--------|--------|
| Category | Account Support |
| Urgency | Medium |
| AI Reason | Customer cannot access their account and requires password reset instructions. |

---

## 📧 Workflow Output

### Automatic Reply

For low-priority requests, the workflow sends an AI-generated response directly to the customer.

### Human Review

For medium or high-priority requests, the workflow sends an HTML-formatted email containing:

- Customer Name
- Customer Email
- Original Message
- Support Category
- Urgency Level
- AI Reason

This allows a support agent to review the request before responding.

---

## 📚 Learning Outcomes

Through this project, I learned how to:

- Build AI-powered workflows in n8n.
- Process Webhook requests.
- Integrate AI models with automation.
- Generate structured JSON responses.
- Implement workflow branching using IF Nodes.
- Create professional HTML email templates.
- Integrate Gmail with n8n.
- Design Human-in-the-Loop automation workflows.
- Test and validate different workflow execution paths.

---

## 📸 Project Screenshots

The repository contains screenshots of:

- Customer Support Form
- Webhook Configuration
- AI Agent Setup
- AI Prompt
- IF Node Logic
- Gmail Configuration
- Automatic Email Response
- Human Review Email
- Workflow Execution
- Final Workflow
---

## 🚀 Future Improvements

- Add Slack or Microsoft Teams notifications.
- Store support requests in Google Sheets or a database.
- Integrate a ticketing system.
- Add sentiment analysis for customer messages.
- Build a support dashboard for tracking requests.
