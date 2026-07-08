# AI Automation Workflows

A collection of n8n automation workflows built during my AI Automation 
Internship, exploring event-driven automation, CRM-style data handling, 
and AI-assisted decision logic.

## What's in here

Each folder under `/workflows` is a self-contained automation with its 
own README, exported workflow JSON, and sample data so it can be reviewed 
or re-imported into n8n independently.

| Workflow | What it does |
|---|---|
| [lead-intake-alert](workflows/lead-intake-alert) | Captures form submissions via webhook and sends a conditional email alert based on lead budget |
| [lead-intake-dedupe](workflows/lead-intake-dedupe) | Extends the intake flow with CRM-style deduplication — checks Airtable by email before deciding to update or create a record |

## Tools used across these workflows
n8n, Tally Forms, Airtable, Gmail API

## Note on data
All sample data in this repo is fake/generated for demonstration purposes. 
No real client or company data from my internship is included here.

## More coming soon
This repo will grow as the internship progresses — future additions include 
AI agent workflows, a RAG-based FAQ bot, and Telegram bot integrations.
