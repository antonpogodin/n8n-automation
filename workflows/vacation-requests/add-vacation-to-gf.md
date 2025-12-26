# Add Vacation to GF

**File:** `add-vacation-to-gf.json`

A sub-workflow that handles the integration with Glass Factory API for vacation management.

## Features

### Authentication

Handles Glass Factory API authentication

### Member Lookup

Finds employee by email address

### Vacation Management

- Creates new vacations
- Updates existing vacations (delete and recreate)
- Retrieves vacation details

## Workflow Components

- **Execute Workflow Trigger**: Receives parameters from parent workflow
- **Authenticate**: Logs into Glass Factory API
- **Get Members**: Retrieves employee list
- **Find Member by Email**: Locates specific employee
- **Get Vacations**: Retrieves existing vacations
- **Find Vacation by ID**: Checks if vacation already exists
- **Delete Vacation**: Removes existing vacation (for updates)
- **Create Vacation**: Adds new vacation to Glass Factory

## Input Parameters

- `member_email`: Employee email address
- `start_date`: Vacation start date (YYYY-MM-DD)
- `end_date`: Vacation end date (YYYY-MM-DD)
- `vacation_type`: Type of vacation (Paid/Unpaid/Sick)
- `vacation_id`: Optional existing vacation ID for updates

## Requirements

- Glass Factory API credentials
- Glass Factory account with API access

## Configuration

Before using this workflow, you'll need to:

1. **Set up credentials** in n8n for:
   - Glass Factory API

2. **Update workflow-specific settings**:
   - Glass Factory API endpoint URLs
   - Authentication credentials

## Usage

This workflow is typically called by the "Add Vacations" workflow, but can also be used standalone or called from other workflows.

## Notes

- This workflow is designed to be called as a sub-workflow
- The workflow contains sensitive information (API credentials) that should be sanitized before sharing publicly

