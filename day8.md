# Day 8 – Building Multiple AI Automation Projects with n8n

**Date:** 29 June

---

# Overview

On Day 8 of my **AI Automation and Agentic AI** training, I built three practical AI-powered applications using **n8n**, **Google Gemini Chat Model**, **Google Sheets**, **Webhooks**, and **Simple Memory**. The projects focused on solving real-world business problems by integrating AI with workflow automation.

The three applications developed were:

1. **AI Customer Support Agent**
2. **AI Inventory Assistant**
3. **AI Fitness Coach**

These projects helped me understand how AI agents can receive user requests, access external data sources, maintain conversation context, generate intelligent responses, and automate complete workflows.

---

# Project 1 – AI Customer Support Agent

## Objective

The objective of this project was to build an intelligent customer support system capable of:

* Receiving customer queries through a Webhook.
* Retrieving previous customer interactions from Google Sheets.
* Processing conversation history using JavaScript.
* Generating context-aware responses using Google Gemini.
* Storing new conversations in Google Sheets.
* Returning responses through an API.

---

## Workflow Architecture

```text
Customer Query
      │
      ▼
Webhook
      │
      ▼
Get Row(s) in Google Sheets
      │
      ▼
JavaScript Code
      │
      ▼
AI Agent
      │
      ▼
Google Gemini Chat Model
      │
 ┌────┴───────────┐
 ▼                ▼
Append Row     Respond to Webhook
Google Sheets
```

---

## Workflow Components

### Webhook

* Receives customer requests.
* Starts the workflow.
* Accepts HTTP POST requests from websites or applications.

### Google Sheets (Get Rows)

* Searches previous customer conversations.
* Retrieves relevant customer history.
* Provides context to the AI Agent.

### JavaScript Code Node

* Formats conversation history.
* Cleans retrieved data.
* Combines previous and current customer queries.

### AI Agent

* Understands customer issues.
* Coordinates communication between all nodes.
* Sends prompts to the language model.

### Google Gemini Chat Model

* Generates intelligent customer support responses.
* Understands natural language.
* Produces professional and context-aware replies.

### Google Sheets (Append Row)

* Saves customer queries.
* Stores AI-generated responses.
* Maintains conversation history.

### Respond to Webhook

* Returns the AI response to the customer.

---

## Example

Customer:

> "My order hasn't been shipped yet."

AI Response:

> "Thank you for contacting support. Your order is currently being processed. Shipping updates are usually sent within 2–3 business days."

---

## Skills Learned

* Customer Support Automation
* Google Sheets Integration
* AI Agent Design
* JavaScript Data Processing
* API Automation
* Prompt Engineering

---

# Project 2 – AI Inventory Assistant

## Objective

The purpose of this project was to create an AI assistant capable of answering inventory-related questions using live data stored in Google Sheets.

---

## Workflow Architecture

```text
User Message
      │
      ▼
When Chat Message Received
      │
      ▼
AI Agent
├───────────────┐
│               │
▼               ▼
Google Gemini   Simple Memory
Chat Model
│
▼
Google Sheets
(Get Rows)
│
▼
Inventory Response
```

---

## Workflow Components

### When Chat Message Received

* Starts the workflow.
* Receives inventory-related questions.

### AI Agent

* Understands user requests.
* Decides when inventory data is required.
* Coordinates the workflow.

### Google Gemini Chat Model

* Generates natural language responses.
* Explains inventory information clearly.

### Simple Memory

* Stores previous conversations.
* Maintains chat context.
* Supports follow-up questions.

### Google Sheets

* Reads live inventory data.
* Retrieves stock information.
* Provides product availability.

---

## Example

User:

> "How many laptops are available?"

AI:

> "There are currently 25 laptops available in inventory."

---

## Skills Learned

* Conversational AI
* Memory Integration
* Google Sheets Tool Calling
* Inventory Management Automation
* AI Workflow Design

---

# Project 3 – AI Fitness Coach

## Objective

The objective of this project was to develop an AI-powered Fitness Coach that provides personalized workout and wellness recommendations based on user information.

---

## Workflow Architecture

```text
User Fitness Details
        │
        ▼
Webhook
        │
        ▼
Append Row in Google Sheets
        │
        ▼
AI Agent
        │
        ▼
Google Gemini Chat Model
        │
        ▼
Respond to Webhook
```

---

## Workflow Components

### Webhook

* Receives user fitness information.
* Starts the workflow.

### Google Sheets

* Stores user details.
* Maintains fitness records.
* Creates a user database.

### AI Agent

* Processes fitness goals.
* Sends prompts to Gemini.
* Generates personalized recommendations.

### Google Gemini Chat Model

* Creates workout plans.
* Suggests healthy habits.
* Generates diet and exercise recommendations.

### Respond to Webhook

* Returns personalized fitness advice.

---

## Example

User Information

* Age: 24
* Weight: 72 kg
* Goal: Weight Loss

AI Response

* Weekly workout plan
* Daily calorie recommendations
* Beginner-friendly exercises
* Healthy diet suggestions
* Motivation tips

---

## Skills Learned

* Health & Fitness Automation
* AI Personalization
* Google Sheets Integration
* Webhook APIs
* AI Agent Development

---

# Concepts Learned During Day 8

Throughout these projects, I learned:

* Building AI Agents in n8n.
* Integrating Google Gemini Chat Model with workflows.
* Using Webhooks to receive API requests.
* Reading and writing data using Google Sheets.
* Using Simple Memory for conversational context.
* Processing workflow data using JavaScript.
* Designing intelligent AI workflows.
* Creating real-world AI automation solutions.
* Implementing Agentic AI concepts for different business use cases.
* Prompt engineering for generating accurate AI responses.

---

# Challenges Faced

During these projects, I learned the importance of:

* Correctly mapping data between workflow nodes.
* Structuring prompts for high-quality AI responses.
* Managing conversation history using Google Sheets and Simple Memory.
* Designing workflows that integrate AI with external tools.
* Ensuring smooth communication between Webhooks, AI Agents, and Google Sheets.

---

# Skills Practiced

* n8n Workflow Development
* AI Agent Configuration
* Google Gemini Integration
* Google Sheets Integration
* Webhook Automation
* JavaScript in n8n
* Simple Memory
* Prompt Engineering
* Customer Support Automation
* Inventory Management
* Fitness Recommendation Systems
* API Development
* Workflow Design
* Agentic AI

---

# Key Takeaways

* AI Agents can automate real-world business processes by combining language models with external tools.
* Google Sheets is an effective lightweight database for storing and retrieving application data.
* Webhooks enable AI workflows to integrate with websites, mobile applications, and APIs.
* Simple Memory improves conversations by preserving context between interactions.
* Google Gemini can generate personalized, context-aware responses across different domains such as customer support, inventory management, and fitness coaching.
* Workflow automation with n8n allows AI systems to interact seamlessly with users and external data sources, making them practical for business and productivity applications.

---

# Conclusion

Day 8 was one of the most comprehensive sessions of my **AI Automation and Agentic AI** training. I successfully developed three AI-powered applications: an **AI Customer Support Agent**, an **AI Inventory Assistant**, and an **AI Fitness Coach**. These projects combined **Google Gemini Chat Model**, **Google Sheets**, **Simple Memory**, **JavaScript**, and **Webhooks** to create intelligent, automated workflows capable of handling customer queries, retrieving live inventory information, and generating personalized fitness recommendations. Through these hands-on implementations, I gained practical experience in building **Agentic AI systems**, integrating AI with external tools, designing API-driven workflows, and developing scalable automation solutions for real-world scenarios.
