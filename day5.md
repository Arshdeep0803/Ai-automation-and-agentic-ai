# Day 5 – Building My First AI Agent with Google Gemini, Memory, and Google Sheets in n8n

**Date:** 26 June

---

# Overview

On Day 5 of my AI Automation and Agentic AI training, I built my first complete AI Agent workflow in **n8n**. The objective was to understand how an AI agent differs from a simple chatbot by enabling it to use a language model, remember previous conversations, and interact with external tools to fetch real-time information.

This was an important milestone because it introduced the concept of **Agentic AI**, where an AI model can make decisions about when to use tools instead of relying only on its built-in knowledge.

---

# Objective

The main goal of today's session was to:

* Build an AI Agent using n8n.
* Integrate Google Gemini as the Large Language Model (LLM).
* Add conversational memory.
* Connect Google Sheets as an external tool.
* Understand how AI agents interact with tools to answer user queries.

---

# Workflow Built

The workflow starts whenever a user sends a chat message.

```
When Chat Message Received
          │
          ▼
      AI Agent
     ├───────────────┐
     │               │
     ▼               ▼
Google Gemini     Simple Memory
Chat Model
     │
     ▼
Google Sheets Tool
(Get Inventory)
     │
     ▼
Response to User
```

---

# Components Used

## 1. When Chat Message Received

This is the trigger node of the workflow.

### Purpose

* Starts the workflow.
* Receives user input.
* Sends the message to the AI Agent.

Without this node, the workflow would never begin.

---

## 2. AI Agent Node

The AI Agent is the brain of the workflow.

Unlike a normal AI model, the AI Agent can:

* Understand the user's request.
* Decide whether memory is needed.
* Decide whether an external tool should be used.
* Generate a final response.

This makes the workflow more intelligent and dynamic.

---

## 3. Google Gemini Chat Model

The AI Agent requires an LLM (Large Language Model) to think and generate responses.

Today I connected:

* Google Gemini Chat Model

### Responsibilities

* Understand natural language.
* Interpret user questions.
* Generate human-like responses.
* Work together with memory and tools.

Without connecting an LLM, the AI Agent cannot process any user request.

---

## 4. Simple Memory

One limitation of basic chatbots is that they forget previous messages.

To solve this, I connected **Simple Memory**.

### Purpose

* Store previous conversations.
* Maintain context.
* Make conversations more natural.

### Example

User:

> My name is Arshdeep.

Later:

> What is my name?

Without memory:

> I don't know.

With memory:

> Your name is Arshdeep.

This demonstrates how memory improves the user experience.

---

## 5. Google Sheets Tool (Get Inventory)

The AI Agent was connected to a Google Sheet that stores inventory data.

Instead of answering from memory, the AI Agent can retrieve live data from the spreadsheet.

### Purpose

* Read inventory records.
* Fetch product information.
* Answer inventory-related questions.

### Example

User:

> How many laptops are available?

The AI Agent can:

1. Detect that inventory data is required.
2. Use the Google Sheets tool.
3. Read the inventory.
4. Return the correct quantity.

This is an example of an AI agent using an external tool.

---

# Understanding Agentic AI

Today I learned the concept of **Agentic AI**.

Traditional AI models only generate responses from their training data.

Agentic AI can:

* Think about the user's request.
* Decide which tool is needed.
* Use memory when necessary.
* Fetch external information.
* Generate an informed response.

This makes AI systems more useful for real-world business applications.

---

# Difference Between AI Model and AI Agent

| AI Model                     | AI Agent                     |
| ---------------------------- | ---------------------------- |
| Generates text               | Can perform actions          |
| Uses only training knowledge | Uses tools and external data |
| No decision-making           | Chooses which tool to use    |
| Usually stateless            | Can remember conversations   |
| Limited capabilities         | More intelligent and dynamic |

---

# Key Concepts Learned

During today's session, I learned:

* Introduction to Agentic AI.
* Building AI Agents in n8n.
* Connecting Google Gemini as the language model.
* Understanding how LLMs work inside an AI Agent.
* Adding conversational memory.
* Integrating Google Sheets as an external tool.
* Reading live data from spreadsheets.
* Understanding tool calling.
* Creating modular AI workflows.

---

# Practical Outcome

By the end of today's training, I successfully created an AI Agent capable of:

* Receiving user messages.
* Understanding natural language.
* Maintaining conversation history.
* Accessing inventory stored in Google Sheets.
* Returning intelligent responses based on live data.
* Combining AI reasoning with external tools.

---

# Challenges Faced

During the implementation, I understood the importance of correctly connecting each component to the AI Agent.

I also learned that:

* The AI Agent cannot function without a connected language model.
* Memory is optional but improves conversations significantly.
* External tools must be properly configured for the AI Agent to access live information.

---

# Skills Gained

* n8n Workflow Development
* AI Agent Configuration
* Google Gemini Integration
* Conversational AI
* Agentic AI Fundamentals
* Memory Management
* Google Sheets Integration
* Tool Calling
* Workflow Automation
* AI Workflow Design

---

# Key Takeaways

* AI Agents are more powerful than traditional chatbots because they can reason and use external tools.
* Memory enables context-aware conversations, making interactions more natural.
* Integrating Google Sheets allows AI to answer questions using real-time data instead of relying only on its training knowledge.
* n8n provides a simple visual interface for building intelligent, modular AI workflows with minimal coding.

---

## Conclusion

Day 5 marked my introduction to building intelligent AI agents in n8n. I learned how to combine **Google Gemini**, **Simple Memory**, and **Google Sheets** to create an AI system capable of understanding user requests, remembering previous interactions, and retrieving live inventory data. This session laid a strong foundation for developing more advanced AI automation workflows and real-world agentic AI applications in the coming days.
