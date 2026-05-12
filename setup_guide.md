# OpsPilot AI — Logistics Operations Automation System — Setup Guide

## Overview

OpsPilot AI is an AI-powered logistics operations incident automation system designed to simulate real-world AIOps workflows.

The system automates:

- Incident intake
- AI-based incident classification
- Operational impact analysis
- Escalation management
- Email alerting
- Executive dashboard updates

---

# System Architecture

The workflow integrates:

- Tally Forms
- n8n
- OpenRouter AI
- JavaScript Logic Engine
- Gmail
- Airtable

---

# Prerequisites

Before setup, ensure you have:

## Required Accounts

| Service | Purpose |
|---|---|
| n8n | Workflow automation |
| Airtable | Executive dashboard database |
| Tally Forms | Incident intake form |
| OpenRouter AI | AI classification |
| Gmail | Escalation notifications |

---

# Folder Structure

```text
OpsPilot-AI-Logistics-Operations-Automation/
│
├── README.md
├── setup_guide.md
├── assets/
│   ├── architecture_flow.png
│   ├── executive_dashboard.png
│   ├── workflow_overview.png
│   ├── gmail_alert.png
│   └── tally_form.png
│
├── workflow/
│   └── opspilot_n8n_workflow.json
│
└── presentation/
    └── OpsPilot_AI_Hackathon_Deck.pptx
```

---

# Step 1 — Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/OpsPilot-AI-Logistics-Operations-Automation.git
```

---

# Step 2 — Configure Airtable

## Create Airtable Base

Create a table named:

```text
Incident_Management
```

## Recommended Fields

| Field Name | Type |
|---|---|
| Ticket ID | Auto Number |
| Timestamp | Created Time |
| Incident Title | Single Line Text |
| Department | Single Select |
| Incident Type | Single Select |
| AI Priority | Single Select |
| Operational Impact | Single Select |
| Escalation Required | Single Select |
| Incident Status | Single Select |
| Reporter Name | Single Line Text |
| Reporter Email | Email |
| AI Summary | Long Text |
| Incident Description | Long Text |

---

# Step 3 — Configure Tally Form

Create an incident intake form using:

- Incident Title
- Department
- Incident Description
- Reporter Name
- Reporter Email

Enable:

```text
Webhook Integration
```

---

# Step 4 — Configure OpenRouter AI

## Create OpenRouter API Key

Generate API key from:

```text
https://openrouter.ai/
```

Use the API key in the n8n HTTP Request node.

---

# Step 5 — Import n8n Workflow

## Import Workflow JSON

In n8n:

1. Open n8n editor
2. Click:
   ```text
   Import from File
   ```
3. Select:
   ```text
   opspilot_n8n_workflow.json
   ```

---

# Step 6 — Configure Webhook

Copy the n8n webhook URL.

Add the webhook inside:

```text
Tally → Integrations → Webhooks
```

---

# Step 7 — Configure Gmail Node

Authenticate Gmail inside n8n.

Used for:

- High priority alerts
- Critical escalation notifications

---

# Step 8 — Configure Airtable Credentials

Inside n8n Airtable nodes:

- Add Airtable Personal Access Token
- Select Base ID
- Select Incident_Management table

---

# Step 9 — Activate Workflow

Inside n8n:

```text
Activate Workflow
```

The automation system is now live.

---

# Workflow Logic

## AI Classification

The AI engine evaluates:

- incident severity
- operational keywords
- system failure indicators
- logistics disruption patterns

The workflow dynamically assigns:

- AI Priority
- Operational Impact
- Incident Type
- Escalation Status

---

# Escalation Rules

## High/Critical Incidents

Triggers:

- Gmail escalation alerts
- Escalated status updates
- Executive dashboard logging

## Medium/Low Incidents

Triggers:

- Incident logging
- Monitoring workflow
- Under review status

---

# Example Workflow Sequence

```text
Tally Form
   ↓
n8n Webhook
   ↓
OpenRouter AI Classification
   ↓
JavaScript Logic Rules
   ↓
Conditional Escalation
   ↓
Gmail Alert (if required)
   ↓
Airtable Dashboard Update
```

---

# Recommended Demo Flow

For demonstrations:

1. Submit incident information via Tally form
2. Show webhook execution in n8n
3. Show AI classification output
4. Show escalation email
5. Show Airtable dashboard update

---

# Author

## Prachi Sarode

Student at Be10X AI Inner Circle Accelerator Program

---
