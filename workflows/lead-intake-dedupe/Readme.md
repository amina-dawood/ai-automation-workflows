# Lead Intake Deduplication Workflow

Prevents duplicate CRM records when the same lead submits a form more 
than once, by checking for an existing match before deciding whether to 
create or update a record.

## How it works

Tally Form -> Webhook -> Edit Fields -> Search Airtable (by email) 
-> IF -> Update existing record / Create new record

1. Incoming submission is cleaned the same way as the alert workflow.
2. Before writing anything, the workflow searches Airtable for a record 
   matching the submitted email.
3. If a match is found, the existing record is updated with the latest 
   submitted values.
4. If no match is found, a new record is created.

## Why email, not name
Two different people can share a name, which would incorrectly merge 
their records. Email reliably identifies one specific person, so it's 
used as the unique key for the search-before-write check.

## Files
- `workflow.json` — importable n8n workflow export
- `sample-leads.csv` — fake sample data used for testing

## Tech
n8n, Tally Forms, Airtable
