# HubSpot Slack Pipeline Analysis Workflow

This repository contains an n8n workflow for analyzing HubSpot CRM pipeline data through Slack commands.

## Overview

The workflow connects Slack, n8n, HubSpot CRM, Google Gemini, and QuickChart to generate real-time CRM pipeline insights. It allows users to ask pipeline-related questions from Slack and receive structured analysis automatically.

## Key Features

Monthly pipeline summary
Month-over-month comparison
Win rate analysis
Open deals analysis
Owner breakdown
Stage funnel analysis
Top deals analysis
Lost deals analysis
Deal velocity analysis
Pipeline comparison chart generation

## Workflow Logic

1. Slack sends a user request to the n8n webhook
2. The Intent Router identifies the type of CRM question
3. Parse Intent converts the model response into structured JSON
4. The workflow checks whether the user requested a comparison
5. HubSpot deal data is fetched for the selected period
6. Smart Compute calculates key CRM metrics
7. Chart Builder creates a chart for comparison requests
8. LLM Analyst generates a short CRM insight
9. The result is sent back to Slack

## File Structure

```text
hubspot-slack-pipeline-analysis/
│
├── README.md
├── .gitignore
└── hubspot-data-analysis.json
```

## Tools Used

n8n
HubSpot CRM
Slack
Google Gemini
QuickChart
GitHub

## Supported Questions

```text
show pipeline
compare this month with last month
show win rate
show open deals
show owner breakdown
show stage funnel
show top deals
show lost deals
show deal velocity
```

## Setup Requirements

To run this workflow, configure the required credentials directly inside n8n.

Required services:

n8n instance
HubSpot account
Slack workspace
Google Gemini API access

## Security Note

Do not upload real API keys, access tokens, credential files, webhook URLs, or private IDs to a public repository. Keep production credentials inside n8n only.

## Status

This workflow is ready for private GitHub storage and can be customized further for CRM reporting, sales performance tracking, and automated pipeline analysis.
