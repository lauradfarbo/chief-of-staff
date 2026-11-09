# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool you have connected in that category. The plugin describes work in terms of categories, not products, so it runs on any stack. During onboarding, Claude checks which categories you have and records your choices in `preferences.md`.

Nothing here is required. If a category is missing, the briefing says so in that section and carries on.

## Categories

| Category | Placeholder | Examples |
|---|---|---|
| Email | `~~email` | Gmail, Outlook |
| Calendar | `~~calendar` | Google Calendar, Outlook Calendar |
| Chat | `~~chat` | Slack, Microsoft Teams, Discord |
| Task tracker | `~~task tracker` | Asana, Linear, Jira, Todoist, Notion |
| CRM | `~~crm` | HubSpot, Salesforce, Pipedrive |
| Meeting notes | `~~meeting notes` | Granola, Fireflies, Otter, built-in meeting notes |
| Docs and notes | `~~docs` | Google Docs, Notion, Confluence |
| Files | `~~files` | Google Drive, OneDrive, Dropbox, a local folder |
