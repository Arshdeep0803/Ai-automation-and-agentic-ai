# Day 10 – AI News Digest Automation using n8n

**Date:** 1 July

## Overview

On Day 10 of my **AI Automation and Agentic AI** training, I built an **AI News Digest Automation** workflow using **n8n**, **NewsAPI**, **OpenAI Chat Model**, **HTTP Request**, **Edit Fields**, **Schedule Trigger**, and **Gmail**. The objective of this project was to automate the process of collecting the latest news, summarizing it using AI, and delivering a well-structured news digest via email.

This project introduced me to integrating external APIs with AI models and creating scheduled automation workflows. Instead of manually browsing multiple news websites, the workflow automatically fetches the latest headlines, processes them using an AI model, and sends a concise summary to the recipient's inbox. It demonstrated how AI can transform raw information into meaningful insights while eliminating repetitive manual tasks.

---

# Project – AI News Digest Automation

The AI News Digest workflow was designed to collect the latest news articles, generate AI-powered summaries, and automatically email the summarized news at scheduled intervals.

The workflow begins with a **Schedule Trigger**, which automatically executes the workflow at predefined times without requiring any manual intervention. This makes the automation capable of delivering daily or periodic news updates.

After the workflow starts, an **HTTP Request** node sends a GET request to the **NewsAPI** to retrieve the latest news articles based on selected topics or categories. The API returns news headlines, descriptions, article links, and other related information in JSON format.

The retrieved data is then passed to the **Edit Fields** node, where unnecessary information is removed and only the relevant fields—such as the news title, description, and source—are prepared for AI processing. This step ensures that the AI model receives clean and structured input.

The formatted news data is then forwarded to the **AI Agent**, which is connected to the **OpenAI Chat Model**. The AI analyzes multiple news articles, identifies the key information, removes redundant content, and generates a concise and easy-to-read news summary. Instead of forwarding lengthy articles, the AI creates a digest highlighting the most important events and developments.

Finally, the summarized news is sent to users through the **Gmail** node. The workflow automatically generates an email containing the AI-created news digest and delivers it to the specified recipient, providing an efficient way to stay informed without manually searching for news.

---

# Workflow Architecture

```text
Schedule Trigger
        │
        ▼
HTTP Request (NewsAPI)
        │
        ▼
Edit Fields
        │
        ▼
AI Agent
        │
        ▼
OpenAI Chat Model
        │
        ▼
Gmail
(Send AI News Digest)
```

---

# Workflow Components

### 1. Schedule Trigger

* Automatically starts the workflow at predefined intervals.
* Eliminates the need for manual execution.
* Enables daily or scheduled news delivery.

### 2. HTTP Request (NewsAPI)

* Fetches the latest news articles.
* Retrieves headlines, descriptions, sources, and article links.
* Connects n8n with an external news service.

### 3. Edit Fields

* Cleans and formats the API response.
* Selects only the required news information.
* Prepares structured input for the AI model.

### 4. AI Agent

* Coordinates the workflow.
* Sends formatted news data to the language model.
* Receives AI-generated summaries.

### 5. OpenAI Chat Model

* Analyzes multiple news articles.
* Generates concise summaries.
* Highlights the most important information.
* Produces a reader-friendly news digest.

### 6. Gmail

* Sends the AI-generated news digest automatically.
* Delivers summarized news directly to the user's inbox.
* Completes the end-to-end automation workflow.

---

# Concepts Learned

During this project, I learned:

* Building scheduled automation workflows in n8n.
* Integrating external REST APIs using HTTP Request nodes.
* Fetching real-time news data from NewsAPI.
* Processing and formatting JSON responses.
* Using AI to summarize multiple news articles.
* Automating email delivery using Gmail.
* Designing AI-powered information aggregation systems.
* Combining workflow automation with large language models.

---

# Skills Practiced

* n8n Workflow Development
* Schedule Trigger Configuration
* HTTP Request Integration
* REST API Integration
* NewsAPI Integration
* OpenAI Chat Model Integration
* AI Agent Configuration
* Data Transformation
* Prompt Engineering
* Gmail Automation
* AI Content Summarization
* Workflow Automation

---

# Key Takeaways

This project demonstrated how AI and workflow automation can simplify information consumption by automatically collecting, summarizing, and delivering news updates. By integrating **NewsAPI**, the **OpenAI Chat Model**, **Gmail**, and **n8n**, I learned how to build an end-to-end automation pipeline that transforms large volumes of news into concise, personalized email digests. The project strengthened my understanding of API integration, scheduled workflows, AI-powered summarization, and automated communication, showcasing a practical real-world application of **Agentic AI**.
