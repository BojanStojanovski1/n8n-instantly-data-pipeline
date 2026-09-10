# Automated Instantly Data Pipeline

A GTM workflow I built in n8n to automate account sourcing through the Instantly SuperSearch API and transfer the resulting data into Google Sheets for further lead scoring via GPT for Sheets.

## What it does

The workflow:

- Triggers an Instantly SuperSearch
- Waits for Instantly to complete enrichment
- Checks the enrichment status automatically
- Handles retries and timeout scenarios
- Detects searches that return no accounts
- Retrieves the completed data
- Splits the results into individual rows
- Transfers the structured data into Google Sheets

## Why I built it

Instantly SuperSearch runs asynchronously, so the results aren't immediately available after a search is triggered.

Instead of manually triggering searches, waiting, exporting data and moving it into Sheets, this workflow handles the process automatically in just seconds for hundreds of leads.

## Built with

n8n · Instantly API · Google Sheets API

## Next iteration

Extend the workflow from:

**Data sourcing → enrichment → ICP qualification → email verification → campaign activation**
