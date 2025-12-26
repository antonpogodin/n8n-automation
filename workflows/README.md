# n8n Workflows

This repository contains n8n workflow automation templates organized by category.

## Directory Structure

```
workflows/
├── email-management/     # Email processing and management workflows
│   ├── inbox-ninja.json
│   └── inbox-ninja.md
└── vacation-requests/    # Vacation request processing workflows
    ├── add-vacations.json
    ├── add-vacations.md
    ├── add-vacation-to-gf.json
    └── add-vacation-to-gf.md
```

## Workflows

### Email Management

- **[InboxNinja](email-management/inbox-ninja.md)** - Intelligent email classification, receipt processing, and newsletter management

### Vacation Requests

- **[Add Vacations](vacation-requests/add-vacations.md)** - AI-powered vacation request processing from email
- **[Add Vacation to GF](vacation-requests/add-vacation-to-gf.md)** - Glass Factory API integration for vacation management

## Quick Start

### Importing Workflows

1. Open your n8n instance
2. Click "Import from File" or use the import functionality
3. Select the desired workflow JSON file
4. Configure credentials for all required services
5. Update any hardcoded values (email addresses, document IDs, etc.)
6. Test the workflow before activating

### General Requirements

Most workflows require credentials for:
- Gmail (OAuth2)
- OpenAI API
- Google Sheets (OAuth2)
- Google Drive (OAuth2)
- Various other APIs (see individual workflow documentation)

## Documentation

Each workflow has its own detailed documentation file:
- See the `.md` files in each workflow directory for specific setup instructions, features, and requirements

## License

See the [LICENSE](../LICENSE) file in the repository root.
