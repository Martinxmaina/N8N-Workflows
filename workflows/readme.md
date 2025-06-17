# 🧠 Investment Criteria Intelligence Tool

An automation-first system that helps startups find the most aligned VC/PE firms by intelligently extracting, filtering, and reporting detailed investment criteria — all built using **n8n** and modern low-code tools.

---

## 🚀 Features

- **Automated Data Extraction**  
  - Pulls firm-specific data: industry focus, deal size, region, stage preferences, exclusions, etc.  
  - Extracts data from websites, pitch decks, and other public/private sources

- **Smart Filtering Engine**  
  - Matches startups with relevant investors based on their profile  
  - Handles multi-condition logic for accurate pairing (e.g., industry + region + check size)

- **AI-Powered Report Generation**  
  - Uses OpenAI to create summary insights and investment profiles  
  - Exports to well-structured PDF documents

- **Real-Time Notifications**  
  - Alerts via **Telegram**, **Email**, and now **Slack**  
  - Summarized investor-match reports delivered directly to stakeholders

- **Hidden Data Mining**  
  - Employs **Google Dorking** to discover deep investment details not easily accessible  
  - Expands dataset with firm LinkedIn pages, hidden PDF decks, and team bios

- **Fully Modular & Low-Code**  
  - Built 100% in **n8n**, with integrations across:
    - Supabase
    - Airtable
    - Redis
    - Telegram
    - Slack
    - OpenAI
    - PDF Generator

---

## 📹 Demo

[Screenshort of the workflow](<Screenshot 2025-06-17 at 05.01.06.png>)
---

## 🧩 Architecture Overview

![n8n workflow](<Screenshot 2025-06-17 at 04.30.46.png>)


| **Tool**         | **Purpose**                     |
| ---------------- | ------------------------------- |
| `n8n`            | Core automation engine          |
| `Supabase`       | Relational data storage         |
| `MongoDB`        | NoSQL for flexible data capture |
| `Airtable`       | Light CMS/CRM                   |
| `Redis`          | Caching and queues              |
| `OpenAI`         | Investment insights generation  |
| `PDF Generator`  | Report creation                 |
| `Telegram/Slack` | Notifications                   |
| `Google Dorking` | Deep data discovery             |

## 🔧 Setup Instructions

2. Configure Environment Variables
You'll need API keys for:

OpenAI

Slack

Telegram

Supabase / MongoDB

PDF Generator

### Import the Workflow
Open your n8n instance

Import the workflow JSON located in /workflows/investor-matching.json

### Set up Triggers
Use one of the following triggers to initiate the workflow:

HTTP Webhook

Scheduled Cron

Airtable/Database event

## Run It!
Input a startup profile and let the system do the rest — from matching to report generation and notification delivery.

🧪 Example Use Case
You’re a fintech founder looking to raise $1M in Africa.
Simply input your company profile — the system will:


Deliver everything to your inbox and Slack — fully automated


```bash
git clone https://github.com/martinxmaina/