# Setup Guide

## 1. Import the Workflow
Import `workflow.json` into your n8n instance.

## 2. Groq Setup
Get a free Groq API key from console.groq.com.

Recommended model:
- `llama-3.3-70b-versatile`

Used for:
- CV screening
- candidate scoring
- strength and gap analysis
- rationale generation
- candidate email content

## 3. Google Sheets Setup
Create a Google Sheet named **Candidate Tracker**.

Use these columns:
- CandidateID
- Name
- Email
- RoleApplied
- Score
- Classification
- StrengthAreas
- GapAreas
- AIRationale
- ActionTaken
- AppliedAt
- InterviewLink

## 4. Gmail Setup
Connect Gmail in n8n using OAuth2.

Used for:
- interview invitations
- keep-in-view emails
- rejection emails

## 5. Slack Setup
Connect Slack in n8n.

Used for:
- shortlisted candidate alerts
- recruiter notifications

Recommended channel:
- `recruitment-pipeline`

## 6. Calendly Setup
Create a free Calendly booking page and copy the interview link.

Update the Code node with:
- `CALENDLY_LINK`

## 7. Webhook / Form Setup
Copy the webhook URL from n8n and connect it to your candidate application form.

Typical form fields:
- name
- email
- role
- cv_text or uploaded CV path
- linkedin (optional)

## 8. Expected Flow
- application submitted
- candidate details sent to Groq
- candidate scored and classified
- candidate email sent based on result
- shortlisted candidate triggers recruiter Slack alert
- candidate log written to Google Sheets

## 9. Notes
This project is portfolio-ready and may require reconnecting credentials after import into another n8n environment.
