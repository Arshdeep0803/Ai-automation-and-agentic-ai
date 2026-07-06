# Day 6 – Building an AI-Powered Travel Planner Agent in n8n

**Date:** 27 June

---

# Overview

On Day 6 of my **AI Automation and Agentic AI** training, I built an **AI-powered Travel Planner Agent** using **n8n** and the **Google Gemini Chat Model**. The aim of this project was to understand how AI agents can process user requests received through a webhook, structure the incoming data, and generate personalized travel itineraries based on user preferences.

This project introduced me to building AI-powered API services that can be integrated with websites, mobile applications, or chatbots to provide intelligent travel recommendations.

---

# Objective

The objectives of today's project were:

* Build a Travel Planner AI Agent in n8n.
* Learn how Webhooks receive data from external applications.
* Transform incoming user data using the Edit Fields node.
* Connect Google Gemini as the Large Language Model (LLM).
* Generate customized travel itineraries based on user inputs.
* Understand how AI workflows can function as API endpoints.

---

# Workflow Architecture

```text
User/Application
        │
        ▼
   Webhook (POST)
        │
        ▼
   Edit Fields
        │
        ▼
     AI Agent
        │
        ▼
Google Gemini Chat Model
        │
        ▼
 Personalized Travel Plan
```

---

# Workflow Components

## 1. Webhook Node

The workflow begins with a **Webhook** node configured to accept **HTTP POST** requests.

### Purpose

* Acts as the entry point of the workflow.
* Receives travel-related information from users.
* Allows external applications to communicate with the AI workflow.

Typical information received includes:

* Destination
* Number of travel days
* Budget
* Number of travelers
* Preferred activities
* Travel interests

Once the data is received, the webhook automatically triggers the workflow.

---

## 2. Edit Fields Node

After receiving the request, the **Edit Fields** node processes and organizes the incoming data.

### Purpose

* Rename fields.
* Remove unnecessary information.
* Format the request.
* Prepare structured input for the AI Agent.

Instead of sending multiple separate fields to the AI, this node creates a clean and readable prompt.

### Example

Input Data

* Destination: Manali
* Days: 5
* Budget: ₹20,000
* Travelers: 2

Formatted Prompt

> Create a 5-day travel itinerary for two people visiting Manali with a budget of ₹20,000. Include sightseeing places, transportation suggestions, hotels, food recommendations, and daily activities.

This improves the quality of the AI-generated response.

---

## 3. AI Agent

The AI Agent is responsible for processing the user's request.

### Responsibilities

* Accept structured input.
* Understand the travel requirements.
* Send the request to the connected language model.
* Generate the final travel plan.

The AI Agent serves as the central controller of the workflow.

---

## 4. Google Gemini Chat Model

The AI Agent uses the **Google Gemini Chat Model** as its language model.

### Responsibilities

* Understand natural language.
* Analyze user preferences.
* Generate detailed travel recommendations.
* Create personalized itineraries.

The model can recommend:

* Tourist attractions
* Hotels
* Restaurants
* Transportation
* Daily schedules
* Budget allocation
* Travel tips

---

# Workflow Execution

The workflow follows these steps:

1. A user sends travel details through an application or API.
2. The **Webhook** receives the request.
3. The **Edit Fields** node organizes the input into a structured prompt.
4. The prompt is sent to the **AI Agent**.
5. The AI Agent forwards the request to the **Google Gemini Chat Model**.
6. Gemini generates a customized travel itinerary.
7. The AI Agent returns the response to the user.

---

# Example Scenario

### User Request

Destination: Goa

Duration: 4 Days

Budget: ₹25,000

Travelers: 2

Interests:

* Beaches
* Water Sports
* Nightlife

### AI Response

The Travel Planner Agent generates:

* A complete 4-day itinerary.
* Recommended tourist attractions.
* Hotel suggestions within budget.
* Local food recommendations.
* Transportation guidance.
* Estimated daily expenses.
* Useful travel tips.

---

# Concepts Learned

During this project, I learned:

* Building AI Agents in n8n.
* Configuring Webhooks for API-based communication.
* Structuring incoming data using the Edit Fields node.
* Connecting Google Gemini as the language model.
* Prompt engineering for travel planning.
* Designing AI workflows that respond to external requests.
* Understanding how AI agents coordinate between user input and language models.

---

# Skills Practiced

* n8n Workflow Development
* AI Agent Configuration
* Google Gemini Integration
* Webhook Configuration
* API-Based Automation
* Prompt Engineering
* Data Transformation
* Workflow Design
* Agentic AI Fundamentals

---

# Challenges Faced

While building this workflow, I understood the importance of:

* Correctly mapping webhook data.
* Formatting user input before sending it to the AI model.
* Writing structured prompts for better AI-generated itineraries.
* Ensuring smooth communication between workflow nodes.

---

# Key Takeaways

* Webhooks enable AI workflows to receive requests from external applications.
* The Edit Fields node improves AI responses by organizing raw input into structured prompts.
* AI Agents coordinate the interaction between workflow components and the language model.
* Google Gemini can generate personalized travel itineraries based on user preferences.
* Combining AI with workflow automation allows the creation of practical applications such as travel assistants.

---

# Conclusion

On Day 6, I successfully built a **Travel Planner AI Agent** using **n8n**, a **Webhook**, the **Edit Fields** node, an **AI Agent**, and the **Google Gemini Chat Model**. This project helped me understand how AI agents can receive real-time user requests through APIs, process structured input, and generate personalized travel recommendations. It strengthened my understanding of workflow automation, prompt engineering, and the practical implementation of agentic AI for real-world use cases.
