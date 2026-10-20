
# Setup and Security Checklist

## Purpose

This checklist outlines the preparation required to deploy a comparable n8n-based on-page SEO automation workflow.

This public repository documents the project architecture. It does not include the production workflow export or guarantee a one-click deployment.

## Prerequisites

- An n8n instance with permission to create and execute workflows
- A Google Sheets document containing page URLs and target keyword data
- Google account access for the required Sheets, Docs, and Drive operations
- An Anthropic API account and suitable API access for Claude
- A review of the workflow's node versions, inputs, outputs, and error paths

## Configuration

Before running a deployment:

1. Create your own input spreadsheet and verify its column names and data types.
2. Configure Google authentication using n8n's credential management.
3. Configure Anthropic API authentication using a securely stored credential.
4. Update references to spreadsheets, documents, folders, and other resources to point to resources you control.
5. Check the HTTP request settings, response formats, timeouts, and failure handling.
6. Test with a small number of non-sensitive URLs before processing a full site.

## Security Checklist

- Never commit API keys, OAuth tokens, passwords, or authorization headers.
- Do not publish private spreadsheet IDs, document IDs, client information, or internal URLs.
- Store credentials in n8n's credential manager rather than hard-coding secrets in nodes.
- Grant integrations only the permissions they need.
- Review exported workflow JSON for sensitive values before sharing.
- Use only websites and data you are authorized to access.
- Avoid placing confidential page content or customer data in public logs or reports.

## Validation Before Deployment

- Confirm that page URLs are valid and accessible.
- Handle redirects, unsuccessful HTTP responses, and pages with incomplete HTML.
- Verify that extracted titles, meta descriptions, and headings match the actual pages.
- Check that AI-generated recommendations are supported by the supplied page content.
- Review proposed changes manually before applying them to a live website.
- Verify that spreadsheet updates and report creation target the intended resources.

## Limitations

Actual setup requirements and runtime behavior depend on the deployed workflow, node versions, credentials, API availability, and input spreadsheet structure.

AI-generated recommendations can be inaccurate or unsuitable for a particular page. Human review remains necessary before implementation.
