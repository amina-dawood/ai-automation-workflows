# Lead Intake Alert Workflow

Captures lead submissions in real time and automatically alerts the sales 
team by email when a lead meets a budget threshold — instead of someone 
having to manually check a spreadsheet.

## How it works

Tally Form -> Webhook -> Edit Fields -> IF (Budget > 1000) -> Gmail alert

1. A lead fills out an intake form (name, email, phone, company, service 
   needed, budget, timeline, message, consent).
2. The submission hits an n8n webhook as a nested JSON payload.
3. An Edit Fields node cleans and flattens the payload into simple, 
   usable fields.
4. An IF node checks whether the submitted budget is above 1000.
5. If true, a Gmail node sends a formatted alert email with the lead's details.

## Why this matters
Manually checking a form-response sheet for high-value leads doesn't scale 
past a handful of submissions. This automates the triage step so no 
qualifying lead sits unnoticed.

## Files
- `workflow.json` — importable n8n workflow export
- `sample-leads.csv` — fake sample data used for testing

## Tech
n8n, Tally Forms, Gmail API
