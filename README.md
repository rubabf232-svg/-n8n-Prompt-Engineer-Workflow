# -n8n-Prompt-Engineer-Workflow
n8n Prompt Engineer Workflow using Google Gemini for Complaint Management and Automated AI Responses.# n8n Prompt Engineer Workflow 🚀

A structured, automated AI workflow built in **n8n** that acts as a domain-specific **Prompt Engineer**. It takes raw user inputs from a chat interface, transforms them into high-quality engineered prompts for **Complaint Management**, and generates professional responses using **Google Gemini**.

---


---

## 🛠️ Workflow Architecture & Tech Stack

- **Automation Platform:** n8n (Cloud/Self-hosted)
- **AI Model:** Google Gemini Chat Model
- **Trigger:** n8n Chat Trigger Node
- **Core Logic:** Basic LLM Chain (Prompt Engineering Node)

### Workflow Steps:
1. **Chat Trigger Node (`When chat message received`):** Captures raw text input directly from the user chat window.
2. **Basic LLM Chain (`Prompt Engineer Node`):** Processes raw feedback and restructures it according to Complaint Management guidelines (defining root cause, severity, empathetic tone, and actionable steps).
3. **Google Gemini Chat Model:** Connects as the underlying LLM to generate the final structured resolution response.

---

## 🎯 Domain Prompt (Complaint Management)

The workflow utilizes the following System Prompt inside the Basic LLM Chain:

```text
System: You are an expert Prompt Engineer specializing in Complaint Management. 
Your task is to take a user's raw complaint or negative feedback and rewrite it into a structured, clear, and high-priority prompt for an AI agent handling complaints.

Ensure the engineered prompt includes:
1. Issue Breakdown: Identify the exact complaint, root cause, and severity level.
2. Tone Requirements: Apologetic, serious, objective, and conflict-de-escalating.
3. Action Plan: Clear instructions to offer immediate remedies, compensation/refund policy options, or escalation steps.
4. Output Format: Professional response with numbered resolution steps.
🚀 How to Run / Import
Clone or download this repository.

Open your n8n canvas.

Import the workflow.json file into n8n.

Add your Google Gemini API Key in the credentials setup for Google Gemini Chat Model.

Execute the workflow and test via the built-in Chat window!

✅ Execution Status
Status: Tested & Fully Functional

Execution Log: All nodes execute with zero errors (1 Item output successfully generated).
