# AI Lead Qualification & Follow-up Agent

An AI-powered lead qualification and follow-up automation workflow built with **n8n, Groq LLM, Webhooks, and Google Sheets**.

The system takes incoming lead information, analyzes the lead using an LLM, assigns a lead score and priority, identifies buying intent, recommends the next action, generates a personalized follow-up message, and stores the result in a Google Sheets CRM.

> **Current version:** AI-powered automation workflow
> **Future direction:** Autonomous AI Lead Qualification Agent

## Problem

Businesses receive leads from different sources, but manually reviewing, prioritizing, and following up with every lead can take time.

This project automates the initial lead qualification process so that businesses can quickly identify high-priority leads and decide what action to take next.

## Solution

The workflow automatically:

* Receives lead information through a webhook
* Analyzes the lead using an AI/LLM
* Assigns a lead score from 0–100
* Classifies the lead as **HOT, WARM, or COLD**
* Identifies buying intent
* Explains why the lead received its score
* Recommends the next sales action
* Generates a follow-up message
* Stores the lead and AI results in Google Sheets

## Workflow

The workflow automates the lead qualification process from lead intake to CRM storage.
Lead Data
   ↓
Webhook
   ↓
AI Lead Qualification
   ↓
Structured Output
   ↓
Lead Score + Priority + Buying Intent
   ↓
Recommended Action + Follow-up Message
   ↓
Google Sheets CRM

### Actual n8n Workflow

[AI Lead Qualification n8n Workflow](workflow.png)
## Tech Stack

* **n8n** — workflow automation
* **Groq** — LLM inference
* **GPT-OSS-20B** — language model
* **Webhooks** — lead intake
* **Google Sheets** — CRM/storage
* **Structured Output Parser** — consistent AI responses

## CRM Fields

The workflow stores the following information:

| Field              | Description                   |
| ------------------ | ----------------------------- |
| Name               | Lead name                     |
| Company            | Lead's company                |
| Email              | Lead email                    |
| Requirement        | What the lead needs           |
| Budget             | Lead's stated budget          |
| Timeline           | Expected timeline             |
| Lead Score         | AI-generated score from 0–100 |
| Priority           | HOT / WARM / COLD             |
| Buying Intent      | AI assessment                 |
| Reason             | Explanation for qualification |
| Recommended Action | Suggested next sales step     |
| Follow-up Message  | AI-generated follow-up        |

## Example

### Input

```text
Name: Rahul Sharma
Company: ABC Interiors
Requirement: AI chatbot for website
Budget: 100000
Timeline: 2 weeks
```

### AI Output

```text
Lead Score: 90
Priority: HOT
Buying Intent: High

Reason:
High budget and urgent timeline with a clear requirement for an AI chatbot.

Recommended Action:
Schedule a demo and discuss integration details.
```

The workflow also generates a personalized follow-up message for the lead.

## Why I Built This

I built this project to understand how AI can be applied to real business operations rather than only generating text.

The project focuses on:

* Lead qualification
* Sales operations
* CRM automation
* Customer engagement
* AI-assisted decision making
* Workflow automation

## Key Learning

Through this project, I learned how to connect an LLM with an automation workflow, enforce structured AI outputs, process incoming data through webhooks, and automatically store AI-generated business insights in a CRM-style spreadsheet.

## Future Improvements

The project can be extended from an AI-powered workflow into a more autonomous **AI Lead Qualification Agent**.

Planned improvements include:

* Transforming the workflow into an AI agent that can decide the next action based on lead context
* Connecting the agent to email for automated follow-ups
* Adding automatic follow-up reminders
* Connecting to a real CRM such as HubSpot
* Allowing the agent to update lead status automatically
* Adding lead-source tracking
* Adding analytics and reporting
* Connecting the system to website forms and other lead sources

### Future Agent Architecture

```text
Lead
 ↓
AI Agent
 ↓
Understand Lead
 ↓
Decide Priority
 ↓
Choose Next Action
 ↓
Take Action
 ├── Update CRM
 ├── Send Follow-up
 └── Schedule Reminder
```

The current project focuses on building the **core AI qualification and automation workflow**, which can later serve as the foundation for a more autonomous AI agent.

## Project Status

**MVP Completed**

The current version successfully performs:

* Lead intake
* AI lead qualification
* Lead scoring
* Priority classification
* Buying-intent analysis
* Recommended sales action
* Follow-up message generation
* Structured AI output
* Google Sheets CRM storage

## Security

No API keys, credentials, service-account files, or private customer information are included in this repository.
