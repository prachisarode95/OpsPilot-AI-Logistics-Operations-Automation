# OpsPilot AI — Incident Automation System

## Project Overview

OpsPilot AI is an AI-powered operations incident automation system designed to streamline operational issue intake, intelligent incident classification, escalation management, and executive dashboard monitoring for logistics and operations teams.

The system combines workflow automation, AI classification, conditional escalation logic, and dynamic Airtable dashboards to simulate a real-world AI Operations (AIOps) environment.

---

# Problem Statement

Operations and logistics teams often rely on manual processes for:

* incident intake
* severity assessment
* escalation management
* operational tracking
* dashboard updates

This creates:

* delayed response times
* inconsistent prioritization
* lack of centralized visibility
* operational inefficiencies

OpsPilot AI addresses these challenges through intelligent workflow automation.

---

# Solution Architecture

The system architecture consists of:

1. Tally Forms for operational incident intake
2. n8n for workflow orchestration
3. OpenRouter AI for intelligent classification
4. JavaScript-based operational logic
5. Gmail escalation notifications
6. Airtable executive dashboard for incident tracking

---

# Workflow Pipeline

## Workflow Sequence

1. User submits operational incident via Tally form
2. Webhook captures submission in n8n
3. OpenRouter AI classifies:

   * incident severity
   * operational impact
   * escalation requirements
4. JavaScript logic applies operational rules
5. High/Critical incidents trigger escalation emails
6. Airtable dynamically updates the executive dashboard

---

# AI Classification Logic

The AI classification engine evaluates:

* incident description
* operational keywords
* failure indicators
* routing issues
* system disruption patterns

The system dynamically assigns:

* AI Priority
* Incident Type
* Operational Impact
* Escalation Status

---

# Escalation Logic

## Escalation Conditions

High and Critical incidents:

* trigger Gmail escalation alerts
* update Airtable with escalated status
* notify operational stakeholders

Medium and Low incidents:

* are logged for review
* remain under operational monitoring

---

# Tech Stack

| Component           | Technology    |
| ------------------- | ------------- |
| Workflow Automation | n8n           |
| AI Processing       | OpenRouter AI |
| Database Dashboard  | Airtable      |
| Form Intake         | Tally Forms   |
| Email Notifications | Gmail         |
| Logic Engine        | JavaScript    |
| API Integration     | REST APIs     |

---

# Dashboard Screenshots

## Executive Dashboard

![Dashboard Overview](https://github.com/user-attachments/assets/256e082d-ed39-49c2-9734-f8bccfe01c41)

## Airtable Incident Record

![Airtable Record](https://github.com/user-attachments/assets/658b1a03-310b-4dd8-bf47-3f665d4b4b07)

---

# Workflow Screenshots

## n8n Workflow Overview

![Workflow Overview](https://github.com/user-attachments/assets/d4f85876-2ace-4bd4-baab-2d252df71bc9)

## Tally Intake Form

![Tally Form](https://github.com/user-attachments/assets/1ecd38a3-d86c-4548-bf0d-2bd851bfc556)

## Gmail Escalation Alert

![Escalation Email](https://github.com/user-attachments/assets/f4b70942-52f0-4a23-b3d8-94f7c1e97b66)

---

# Future Improvements

Potential future enhancements include:

* geospatial incident mapping
* AI trend analytics
* SLA monitoring
* predictive incident detection
* role-based dashboards
* automated ticket assignment
* real-time operational analytics
* integration with enterprise ERP systems

---

# Setup Instructions

## Clone Repository

```bash
git clone https://github.com/prachisarode95/OpsPilot-AI-Logistics-Operations-Automation.git
```

## Configure Workflow

1. Import n8n workflow JSON
2. Configure OpenRouter API key
3. Connect Airtable credentials
4. Configure Gmail integration
5. Update webhook URLs
6. Connect Tally webhook

---

# Resume / Portfolio Impact

This project demonstrates practical skills in:

* AI workflow automation
* operations intelligence systems
* workflow orchestration
* API integrations
* Airtable automation
* AI-powered operational decision systems
* incident escalation workflows
* no-code/low-code enterprise automation

The project simulates a real-world AI operations platform suitable for logistics, operational intelligence, and automation engineering environments.
