---
name: salesforce-admin
description: "Handle Salesforce configuration changes, metadata deployments, and data operations safely. Defaults to Sandbox first."
---

# Salesforce Admin Power

## Overview
Manage Salesforce metadata (flows, fields, validation rules) and data (queries, updates) using the Salesforce CLI. 

## Checklist
1. **Identify Object & Metadata** — Which object? Which rule/flow?
2. **Setup Environment** — Ensure `sf org list` shows the correct Sandbox.
3. **Backup Mode** — Retrieve current metadata or query current data to CSV before changing.
4. **Draft & Test (Sandbox)** — Deploy to Sandbox first.
5. **Validation Gate** — Run SOQL to verify the change in Sandbox.
6. **Production Deploy** — ONLY after explicit user approval.

## Salesforce CLI Commands
- `sf project retrieve start --metadata [Type]:[Name] --target-org sandbox`
- `sf project deploy start --metadata [Type]:[Name] --target-org sandbox`
- `sf data query --query "SELECT Id FROM Lead LIMIT 1" --target-org sandbox`

## Error Handling
If a deployment fails, read the component failures carefully. Check for:
- Missing dependencies
- API version mismatches
- Field level security (FLS) issues
