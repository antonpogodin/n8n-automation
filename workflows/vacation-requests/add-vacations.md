# Add Vacations

**File:** `add-vacations.json`

An AI-powered vacation request processing system that automatically handles vacation requests sent via email.

## Features

### Multi-language Support

Processes vacation requests in multiple languages (English, Spanish, Russian, Hebrew)

### Intelligent Parsing

Uses AI to extract vacation details from email threads:
- Vacation type (Paid/Unpaid/Sick)
- Start and end dates
- Duration calculations

### Working Days Calculation

- Calculates working days excluding weekends and holidays
- Supports country-specific weekend rules (e.g., Friday-Saturday for Israel)
- Monthly breakdown of working days
- Integrates with Calendarific API for national holidays

### Calendar Integration

Checks employee calendar information

### Glass Factory Integration

Automatically adds vacations to Glass Factory system

### Google Sheets Logging

Maintains a detailed log of all vacation requests

### Automatic Replies

Sends friendly, personalized replies in the same language as the request

## Workflow Components

- **Gmail Trigger**: Monitors for vacation-related emails (checks every minute)
- **AI Agent**: Processes vacation requests with security protocols
- **Calendarific Tool**: Retrieves national holidays
- **Calculate Working Days Tool**: Custom code tool for accurate working day calculations
- **Glass Factory Integration**: Adds/updates vacations via sub-workflow
- **Google Sheets**: Logs all vacation requests with detailed metadata

## Email Filtering

The workflow monitors emails with subjects containing:
- Vacation-related terms (vacation, отпуск, отгул, etc.)
- Sick leave terms (sick, больничный, etc.)
- Excludes already processed emails (label:processed, label:archived)

## Security Features

- **Security Protocol**: Protects against prompt injection attacks
- **Input Validation**: Validates vacation requests before processing
- **Thread Context**: Retrieves full email thread for context

## Requirements

- Gmail OAuth2 credentials
- OpenAI API credentials (GPT-5.2 model)
- Google Sheets OAuth2 credentials
- Calendarific API key
- Glass Factory API access
- Google Sheets for vacation request logging
- Employee calendar spreadsheet

## Configuration

Before using this workflow, you'll need to:

1. **Set up credentials** in n8n for:
   - Gmail (OAuth2)
   - OpenAI API
   - Google Sheets (OAuth2)
   - Calendarific API
   - Glass Factory API

2. **Create required resources**:
   - Google Sheets for vacation request logging
   - Employee calendar spreadsheet
   - Gmail labels (processed, archived)

3. **Update workflow-specific settings**:
   - Email addresses
   - Google Sheet document IDs
   - Calendarific API key
   - Workflow ID for "Add Vacation to GF" sub-workflow

## Notes

- This workflow references the "Add Vacation to GF" sub-workflow by ID
- Gmail label IDs are account-specific and will need to be updated
- The workflow contains sensitive information that should be sanitized before sharing publicly

