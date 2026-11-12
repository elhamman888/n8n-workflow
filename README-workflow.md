# n8n Workflow Template

This workspace now includes a ready-to-import workflow template:

- `workflow-template.json`

## Import into n8n

1. Open your n8n editor.
2. Click the menu to import a workflow.
3. Select `workflow-template.json`.
4. Save and activate the workflow.

## What this workflow does

- listens for a POST webhook at `demo-webhook`
- reads the incoming payload
- prepares a response object
- returns JSON to the caller

## Example request

```bash
curl -X POST "https://your-n8n-instance.example.com/webhook/demo-webhook" \
  -H "Content-Type: application/json" \
  -d '{"name":"Alice"}'
```

## Example response

```json
{
  "message": "Alice",
  "status": "success",
  "timestamp": "2026-11-12T00:00:00.000Z",
  "received": {
    "name": "Alice"
  }
}
```

If you want, I can customize this workflow for email, Slack, Google Sheets, Airtable, CRM, or a database.
