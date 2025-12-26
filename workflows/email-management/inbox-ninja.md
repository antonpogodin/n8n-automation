# InboxNinja

**File:** `inbox-ninja.json`

An intelligent email management system that automatically classifies, organizes, and processes incoming emails using AI. Originally created by Yonatan Levin (https://www.linkedin.com/in/levinyonatan/).

## Features

### Email Classification

Uses AI to automatically classify emails into categories:
- Promotions
- Newsletters
- Personal
- Business/Customers
- Receipts
- Social
- Other

### Receipt Processing

- Automatically extracts receipt information from emails
- Uploads receipt attachments to Google Drive
- Analyzes receipts using AI to flag unusual expenses
- Stores receipt data in Google Sheets for tracking

### Newsletter Management

- Collects newsletters in Google Sheets
- Weekly digest generation (runs Saturday at 8:30 AM)
- AI-powered newsletter summarization and enrichment
- Sends beautifully formatted weekly mega-newsletter

### Email Organization

- Automatically applies Gmail labels based on classification
- Marks emails as read after processing
- Filters emails newer than 3 hours and not archived

## Workflow Components

- **Gmail Trigger**: Polls for new emails every 10 minutes
- **Email Classifier**: AI-powered text classification using OpenAI
- **Receipts AI Agent**: Intelligent receipt processing with structured output
- **Mega Newsletter AI Agent**: Weekly newsletter digest generation
- **Google Sheets Integration**: Stores newsletters and receipts
- **Google Drive Integration**: Stores receipt attachments

## Requirements

- Gmail OAuth2 credentials
- OpenAI API credentials
- Google Sheets OAuth2 credentials
- Google Drive OAuth2 credentials
- Anthropic API credentials (for newsletter enrichment)
- Google Sheets for newsletters and receipts tracking
- Google Drive folder for receipt storage

## Configuration

Before using this workflow, you'll need to:

1. **Set up credentials** in n8n for:
   - Gmail (OAuth2)
   - OpenAI API
   - Google Sheets (OAuth2)
   - Google Drive (OAuth2)
   - Anthropic API

2. **Create required resources**:
   - Google Sheets for newsletters and receipts
   - Google Drive folder for receipt attachments
   - Gmail labels (custom labels will need to be created and their IDs updated)

3. **Update workflow-specific settings**:
   - Email addresses
   - Google Sheet document IDs
   - Google Drive folder IDs
   - Gmail label IDs
   - API keys

## Notes

- Gmail label IDs are account-specific and will need to be updated
- Google Sheet and Drive IDs are specific to your Google account
- The workflow contains sensitive information that should be sanitized before sharing publicly

