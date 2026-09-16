# 🤖 AI Lead Qualification & Automated Follow-Up System

An AI-powered automation workflow built with **n8n** that captures lead information, analyzes and qualifies leads using an AI Agent, stores the results in Google Sheets, and automatically sends a personalized follow-up email.

## ✨ What This Workflow Does

The workflow automates the lead qualification process from start to finish:

**Lead Intake Form → AI Lead Qualification → Structured Data → Google Sheets → Personalized Email**

### Key Features

* 📝 Collects lead information through an n8n form
* 🤖 Uses an AI Agent to analyze each lead
* 🔥 Classifies leads as **Hot, Warm, or Cold**
* 📊 Generates a concise lead summary and qualification reason
* 📋 Stores lead information and AI-generated results in Google Sheets
* 📧 Automatically sends a personalized follow-up email
* 🛡️ Includes basic workflow error handling

## 🔄 Workflow

### 1. Lead Intake Form

Collects:

* Name
* Email
* Business/Company
* Business requirement
* Budget
* Additional details

### 2. AI Lead Qualification Agent

The AI Agent analyzes the submitted information and determines:

* Lead status
* Qualification reason
* Lead summary
* Suggested follow-up

The agent is instructed to use only the information provided and avoid inventing missing details.

### 3. Lead Data Parser

Converts the AI Agent's response into a structured format containing:

```text
lead_status
reason
lead_summary
suggested_follow_up
```

### 4. Save Qualified Lead

The structured lead information is appended to **Google Sheets** for tracking and follow-up management.

### 5. Send Personalized Follow-Up

A personalized email is automatically sent to the lead using **Gmail**.

## 🧰 Tech Stack

* **n8n** — Workflow automation
* **OpenAI GPT-5 mini** — AI lead qualification
* **Google Sheets** — Lead storage
* **Gmail** — Automated email follow-up
* **n8n Structured Output Parser** — Structured AI responses

## 🎯 Example Use Case

A business receives a new inquiry from a potential client.

Instead of manually reviewing the inquiry, a team can use this workflow to automatically:

1. Capture the inquiry
2. Analyze the lead
3. Determine the lead status
4. Store the information
5. Send a relevant follow-up

This reduces repetitive manual work and creates a consistent lead qualification process.

## 📌 Example

**Lead Input**

```text
Business: Maira's Boutique
Need: AI chatbot for customer support
Budget: $800
Timeline: One month
Requirement: Human handoff
```

**AI Qualification**

```text
Lead Status: Hot
Reason: Clear requirement, stated budget, defined timeline, and
human-handoff requirement indicate strong intent.
```

The workflow then saves the result to Google Sheets and sends a personalized follow-up email automatically.

## 🛠️ Error Handling

Basic error handling is configured on the AI Agent, Google Sheets, and Gmail nodes using n8n's error-handling settings.

## 🚀 Project Goal

This project demonstrates how AI agents can be combined with workflow automation to create a practical business process that can operate with minimal manual intervention.

---

### 👩‍💻 Built by Mawa Ahtsham

AI Automation & AI Agent Orchestration learner

**Focus:** AI Agents • n8n • Workflow Automation • LLMs • Business Process Automation
