# Day 11 – AI Weather Report Automation using n8n

**Date:** 2 July

## Overview

On Day 11 of my **AI Automation and Agentic AI** training, I built an **AI Weather Report Automation** workflow using **n8n**, **OpenWeather API**, **OpenAI Chat Model**, **HTTP Request**, **Schedule Trigger**, **Edit Fields**, **AI Agent**, and **Gmail**. The goal of this project was to automate the process of collecting weather information, generating an AI-powered weather summary, and delivering it through email on a scheduled basis.

This project helped me understand how to integrate weather APIs with AI models and automate routine information delivery. Instead of manually checking weather forecasts every day, the workflow automatically retrieves the latest weather data, converts it into a simple and user-friendly summary using AI, and sends it to the user's email.

---

# Project – AI Weather Report Automation

The AI Weather Report Automation workflow was designed to fetch live weather data, generate an easy-to-understand weather summary, and automatically send it via email.

The workflow begins with a **Schedule Trigger**, which automatically executes the workflow at predefined intervals, such as every morning or at any scheduled time. This eliminates the need for manual execution and ensures regular weather updates.

After the workflow starts, an **HTTP Request** node sends a GET request to the **OpenWeather API** to retrieve the latest weather information for a specified location. The API returns details such as temperature, humidity, weather conditions, wind speed, and other meteorological data in JSON format.

The retrieved data is then passed to the **Edit Fields** node, where unnecessary information is removed and only the relevant weather details are selected. This node formats the data into a clean structure before sending it to the AI model.

Next, the formatted weather information is forwarded to the **AI Agent**, which is connected to the **OpenAI Chat Model**. The AI analyzes the weather data and generates a concise, natural-language weather report that is easy to understand. Instead of presenting raw numerical values, the AI summarizes the forecast with useful insights, making the report more readable.

Finally, the generated weather report is sent through the **Gmail** node. The workflow automatically creates an email containing the AI-generated weather summary and delivers it to the recipient, providing timely weather updates without requiring manual effort.

---

# Workflow Architecture

```text
Schedule Trigger
        │
        ▼
HTTP Request (OpenWeather API)
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
(Send Weather Report)
```

---

# Workflow Components

### 1. Schedule Trigger

* Automatically starts the workflow at predefined intervals.
* Enables daily or scheduled weather updates.
* Removes the need for manual execution.

### 2. HTTP Request (OpenWeather API)

* Retrieves live weather information.
* Connects n8n with the OpenWeather API.
* Fetches details such as temperature, humidity, weather conditions, and wind speed.

### 3. Edit Fields

* Cleans and formats the API response.
* Extracts only the required weather information.
* Prepares structured input for AI processing.

### 4. AI Agent

* Coordinates the workflow.
* Sends formatted weather data to the AI model.
* Receives the summarized weather report.

### 5. OpenAI Chat Model

* Analyzes weather information.
* Converts raw weather data into natural-language summaries.
* Generates user-friendly weather reports with key highlights.

### 6. Gmail

* Automatically sends the AI-generated weather report.
* Delivers weather updates directly to the user's inbox.
* Completes the workflow.

---

# Workflow Execution

The workflow performs the following steps:

1. The Schedule Trigger starts the workflow at the configured time.
2. The HTTP Request node fetches live weather data from the OpenWeather API.
3. The Edit Fields node formats and filters the retrieved data.
4. The AI Agent forwards the formatted weather information to the OpenAI Chat Model.
5. The OpenAI model generates an easy-to-read weather summary.
6. Gmail sends the summarized weather report to the recipient automatically.

---

# Example Scenario

**Location:** Chandigarh

**Weather Data Retrieved**

* Temperature: 32°C
* Humidity: 68%
* Weather: Partly Cloudy
* Wind Speed: 10 km/h

**AI-Generated Weather Summary**

> "Today's weather in Chandigarh is partly cloudy with a temperature of 32°C. Humidity levels are moderate at 68%, and light winds of around 10 km/h are expected. Overall, the weather will remain warm, making it advisable to stay hydrated if spending long periods outdoors."

---

# Concepts Learned

During this project, I learned:

* Building scheduled automation workflows in n8n.
* Integrating REST APIs using HTTP Request nodes.
* Fetching live weather information from the OpenWeather API.
* Processing JSON responses.
* Using AI to generate human-readable summaries from structured data.
* Automating email delivery using Gmail.
* Combining external APIs with AI-powered workflows.
* Designing intelligent information delivery systems.

---

# Skills Practiced

* n8n Workflow Development
* Schedule Trigger Configuration
* HTTP Request Integration
* REST API Integration
* OpenWeather API Integration
* OpenAI Chat Model Integration
* AI Agent Configuration
* Data Transformation
* Prompt Engineering
* Gmail Automation
* AI Content Summarization
* Workflow Automation

---

# Key Takeaways

This project demonstrated how AI and workflow automation can transform raw weather data into meaningful daily updates. By integrating the **OpenWeather API**, **OpenAI Chat Model**, **Gmail**, and **n8n**, I built an end-to-end automation workflow that automatically retrieves weather information, summarizes it using AI, and delivers it via email. The project strengthened my understanding of API integration, scheduled automation, AI-powered summarization, and intelligent notification systems, while reinforcing the practical application of **Agentic AI** in everyday use cases.
