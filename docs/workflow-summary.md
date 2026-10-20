
# Workflow Summary

## Purpose

Automate repeatable parts of on-page SEO analysis and recommendation drafting from a keyword-mapping spreadsheet.

## High-Level Stages

1. **Input preparation:** Read page URLs and mapped target keywords from Google Sheets and reshape rows into page records.
2. **Page retrieval:** Fetch the live page HTML.
3. **HTML inspection:** Extract the existing title tag, meta description, H1 elements, and supporting page context.
4. **AI-assisted review:** Send page context to the Claude API for structured analysis and suggested on-page improvements.
5. **Response processing:** Parse model responses and assemble result fields for the output sheet.
6. **Reporting:** Update Google Sheets, create a Google Docs page report, and organize it in Google Drive.

## Important Boundaries

- This describes the observed workflow design, not a claim that every run has been validated end to end.
- The workflow may require maintenance as n8n nodes, APIs, authentication methods, and spreadsheet schemas change.
- This public repository excludes production workflow JSON and detailed prompt content.
- An importable workflow should be prepared separately, with sensitive values removed, before public release.
