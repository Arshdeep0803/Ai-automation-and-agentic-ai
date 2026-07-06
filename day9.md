# Day 9– Building AI Fitness Coach and AI Expense Tracker with n8n

**Date:** 29 June

## Overview

On Day 8 of my **AI Automation and Agentic AI** training, I developed two AI-powered applications using **n8n**, **Google Gemini Chat Model**, **Google Sheets**, **Webhooks**, **JavaScript**, and the **Switch** node. These projects demonstrated how AI can automate real-world tasks in the domains of **health & fitness** and **personal finance** by combining large language models with workflow automation and external data storage.

The first project was an **AI Fitness Coach**, which generates personalized workout and wellness recommendations based on user information. The second project was an **AI Expense Tracker**, which automatically understands, categorizes, and stores user expenses in different Google Sheets. Both projects helped me understand how AI agents can process user input, interact with external services, and automate complete workflows with minimal manual effort.

---

# Project 1 – AI Fitness Coach

The AI Fitness Coach was designed to provide personalized health and fitness guidance based on user details. The workflow begins with a **Webhook** that receives information such as age, height, weight, activity level, and fitness goals. The user's data is then stored in **Google Sheets** for record keeping. An **AI Agent**, connected to the **Google Gemini Chat Model**, analyzes the user's profile and generates customized workout plans, healthy lifestyle suggestions, nutrition tips, and motivational advice. Finally, the generated recommendations are returned to the user through the Webhook.

This project demonstrated how AI can deliver personalized recommendations while integrating workflow automation with external data storage.

---

# Project 2 – AI Expense Tracker

The AI Expense Tracker was developed to automate expense management using artificial intelligence. Users submit expense details through a **Webhook**, and the **AI Agent** forwards the request to the **Google Gemini Chat Model**. Gemini analyzes the expense description, identifies the appropriate expense category, and generates structured output. A **JavaScript Code** node processes the AI-generated data, after which a **Switch** node automatically routes the expense to the correct **Google Sheet** based on categories such as **Food**, **Shopping**, **Travel**, **Bills**, or **Others**. Each category is connected to an **Append Row** node that stores the expense in its respective spreadsheet. After successfully saving the record, the workflow returns a confirmation response to the user.

This project introduced me to AI-based expense categorization, workflow branching using the Switch node, and automated financial record management.

---

# Concepts Learned

During these projects, I learned:

* Building AI-powered applications using n8n.
* Integrating Google Gemini Chat Model with AI Agents.
* Using Webhooks for API-based communication.
* Reading and writing data in Google Sheets.
* Processing AI-generated output using JavaScript.
* Implementing conditional workflow routing with the Switch node.
* Creating personalized recommendation systems.
* Automating expense categorization using AI.
* Applying prompt engineering to improve AI-generated responses.
* Designing practical Agentic AI solutions for real-world use cases.

---

# Skills Practiced

* n8n Workflow Development
* AI Agent Configuration
* Google Gemini Integration
* Google Sheets Integration
* Webhook Automation
* JavaScript in n8n
* Switch Node Logic
* Prompt Engineering
* Health & Fitness Automation
* Expense Management Automation
* API Integration
* Workflow Design
* Agentic AI Development

---

# Key Takeaways

These two projects strengthened my understanding of how AI agents can automate different real-world scenarios by combining language models with workflow automation. The **AI Fitness Coach** demonstrated how AI can generate personalized health recommendations based on user profiles, while the **AI Expense Tracker** showed how natural language processing and conditional workflow routing can simplify financial management. Together, these projects enhanced my practical knowledge of **Agentic AI**, **Google Gemini integration**, **workflow automation**, **data processing**, and building intelligent applications using **n8n**.
