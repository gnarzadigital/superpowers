---
name: data-enrichment
description: "Orchestrate data enrichment pipelines using Clay, Orbital, and Salesforce. Focuses on SDR and Marketing targets."
---

# Data Enrichment Power

## Overview
Turn sparse leads into high-intent targets by combining Clay's waterfall enrichment with Orbital's custom scraping and Salesforce connectivity.

## Checklist
1. **Define Source** — Salesforce Lead/Contact, CSV, or Domain list?
2. **Map Columns** — What data do we have vs. what do we need?
3. **Waterfall Logic** — 
   - [Step 1] Primary provider (e.g. Apollo via Clay)
   - [Step 2] Secondary/Fallback (e.g. Hunter/Prospeo)
   - [Step 3] Custom Scrape (Orbital)
4. **Validation** — Check fill rate on a sample of 10-50 records.
5. **Sync** — Push back to Salesforce or export to CSV.

## Principles
- **Accuracy over Speed:** Always verify a sample.
- **Cost Efficiency:** Use cheaper providers for the first hit, expensive ones only if null.
- **Audit Trail:** Keep a copy of the "Before" and "After" data.
