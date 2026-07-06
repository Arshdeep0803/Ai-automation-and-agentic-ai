# Day 7 – Building an AI Study Tutor in n8n

**Date:** 28 June

---

# Overview

On Day 7 of my **AI Automation and Agentic AI** training, I developed an **AI Study Tutor** using **n8n**, **Google Gemini Chat Model**, and **Google Sheets**. The goal of this project was to build an intelligent tutoring system capable of answering students' questions, tracking previous interactions, and maintaining a record of conversations for future reference.

Unlike the previous projects, this workflow introduced conditional logic using the **If** node and JavaScript-based data processing, making the AI tutor more dynamic and capable of handling different scenarios based on the user's input.

---

# Objective

The objectives of today's project were:

* Build an AI-powered Study Tutor.
* Receive student questions through a Webhook.
* Check if the student's information or query already exists in Google Sheets.
* Apply conditional logic using the **If** node.
* Process data using JavaScript when required.
* Generate intelligent answers using Google Gemini.
* Store new conversations in Google Sheets.
* Return the AI-generated response through the Webhook.

---

# Workflow Architecture

```text
Student Question
        │
        ▼
      Webhook
        │
        ▼
 Get Row(s) in Google Sheets
        │
        ▼
        IF
   ┌───────────────┐
   │               │
True             False
 │                 │
 ▼                 ▼
Code          Edit Fields
(JavaScript)       │
   └─────────┬─────┘
             ▼
         AI Agent
             │
             ▼
 Google Gemini Chat Model
             │
             ▼
 Append Row in Google Sheets
             │
             ▼
   Respond to Webhook
```

---

# Workflow Components

## 1. Webhook

The workflow starts with a **Webhook** configured to receive **HTTP POST** requests.

### Purpose

* Accepts questions submitted by students.
* Acts as the entry point of the workflow.
* Sends the received data to the next node for processing.

Example inputs include:

* Subject
* Topic
* Question
* Student name
* Difficulty level

---

## 2. Get Row(s) in Google Sheets

The **Get Row(s)** node searches a Google Sheet for existing records.

### Purpose

* Read previously stored student data.
* Check if a similar question or record already exists.
* Retrieve relevant information before generating a response.

This helps avoid unnecessary duplication and provides context for the AI.

---

## 3. If Node

The **If** node introduces decision-making into the workflow.

### Purpose

* Evaluate whether matching data exists in Google Sheets.
* Direct the workflow to different paths based on the result.

#### True Path

If matching data is found:

* The workflow sends the data to the JavaScript Code node for further processing.

#### False Path

If no matching data exists:

* The workflow formats the incoming request using the Edit Fields node before sending it to the AI Agent.

This conditional branching makes the workflow more intelligent and efficient.

---

## 4. Code in JavaScript

The **Code** node processes the data programmatically.

### Purpose

* Manipulate or clean retrieved data.
* Format information before passing it to the AI Agent.
* Perform custom logic that cannot be achieved with standard nodes.

Using JavaScript allows greater flexibility and control over the workflow.

---

## 5. Edit Fields

When no existing record is found, the **Edit Fields** node prepares the student's question.

### Purpose

* Organize incoming data.
* Rename fields.
* Create a structured prompt for the AI model.

For example, a student's raw question can be transformed into a prompt such as:

> "Explain Newton's Second Law with a simple example suitable for a Class 11 student."

Well-structured prompts improve the quality of AI-generated responses.

---

## 6. AI Agent

The **AI Agent** serves as the central processing unit of the workflow.

### Responsibilities

* Receive processed input.
* Understand the student's request.
* Send the prompt to the language model.
* Generate an educational and accurate response.

The AI Agent coordinates communication between the workflow and the AI model.

---

## 7. Google Gemini Chat Model

The AI Agent is connected to the **Google Gemini Chat Model**, which acts as the Large Language Model (LLM).

### Responsibilities

* Understand natural language.
* Explain concepts clearly.
* Solve academic questions.
* Provide examples and step-by-step explanations.
* Adapt responses to the student's query.

This enables the Study Tutor to act like a virtual teacher.

---

## 8. Append Row in Google Sheets

After generating a response, the workflow stores the interaction in Google Sheets.

### Purpose

* Save the student's question.
* Store the AI-generated answer.
* Maintain a history of conversations.
* Build a searchable knowledge base for future use.

This allows future interactions to reference previously stored information.

---

## 9. Respond to Webhook

The final node sends the AI-generated response back to the user.

### Purpose

* Return the tutor's answer to the application or website that made the request.
* Complete the workflow execution.

---

# Workflow Execution

The workflow follows these steps:

1. A student submits a question through an application or API.
2. The **Webhook** receives the request.
3. Google Sheets is searched for existing records.
4. The **If** node checks whether matching data exists.
5. If data exists, it is processed using JavaScript.
6. If no data exists, the request is formatted using the Edit Fields node.
7. The processed prompt is sent to the **AI Agent**.
8. The AI Agent uses the **Google Gemini Chat Model** to generate a response.
9. The question and answer are saved to Google Sheets.
10. The final response is returned through the Webhook.

---

# Example Scenario

### Student Question

**Subject:** Physics

**Question:** Explain Newton's First Law of Motion with an example.

### AI Tutor Response

The AI Tutor provides:

* A simple definition of Newton's First Law.
* A real-life example (such as a passenger moving forward when a bus stops suddenly).
* A clear explanation of inertia.
* A student-friendly summary for better understanding.

---

# Concepts Learned

During this project, I learned:

* Building AI tutoring systems in n8n.
* Integrating Google Sheets for data retrieval and storage.
* Using conditional logic with the **If** node.
* Writing JavaScript code inside workflows for custom data processing.
* Structuring prompts for educational responses.
* Connecting AI Agents with Google Gemini.
* Managing complete request-response workflows using Webhooks.

---

# Skills Practiced

* n8n Workflow Development
* AI Agent Configuration
* Google Gemini Integration
* Webhook Automation
* Google Sheets Integration
* JavaScript in n8n
* Conditional Logic
* Prompt Engineering
* Data Processing
* Agentic AI Workflow Design

---

# Challenges Faced

While building the AI Study Tutor, I learned the importance of:

* Correctly mapping data between workflow nodes.
* Using the **If** node to handle different execution paths.
* Processing data with JavaScript before sending it to the AI.
* Structuring prompts to generate clear and educational responses.
* Storing conversation history in Google Sheets for future reference.

---

# Key Takeaways

* AI tutors can provide personalized and instant learning support.
* Conditional logic allows workflows to adapt based on available data.
* JavaScript nodes add flexibility for advanced data processing.
* Google Sheets can be used as both a data source and a storage system.
* Combining AI Agents, external storage, and automation creates intelligent educational applications.

---

# Conclusion

On Day 7, I successfully built an **AI Study Tutor** using **n8n**, **Google Gemini Chat Model**, **Google Sheets**, JavaScript, and conditional workflow logic. The tutor receives student questions through a webhook, checks for existing records, processes the data intelligently, generates accurate educational responses using AI, stores each interaction in Google Sheets, and returns the answer to the user. This project strengthened my understanding of AI-driven educational systems, workflow automation, data management, and the practical implementation of agentic AI.
