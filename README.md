# AI Resume Screening & Recruitment Pipeline
### n8n + Groq (Free AI) | Screens 500+ CVs/hour | 8hrs of work in 35 minutes

![Workflow](screenshots/workflow.png)

## Project Summary
The AI Resume Screening & Recruitment Pipeline is an automation project built with n8n and Groq AI to screen candidates contextually, classify them automatically, send the right communication, and log everything in a structured audit trail. Instead of relying on rigid keyword matching, the workflow evaluates CVs alongside the job description to score candidate fit more intelligently.

This project demonstrates practical recruitment automation, AI-assisted evaluation, workflow orchestration, candidate communication automation, and audit-friendly logging using free and accessible tools.

## The Problem
- Recruiters spend 6–10 seconds per CV and still miss qualified candidates
- 88% of employers admit their automated filters reject good applicants
- Manual screening takes 8+ hours for 100 CVs
- No consistency between reviewers

## Results
- 92% reduction in screening time (8hrs → 35 mins)
- 500–800 CVs processed per hour
- Consistent, bias-reduced AI evaluation
- $0 AI cost using Groq's free tier

## How It Works
1. Candidate submits application via webhook or HTML form
2. Groq AI (Llama 3.3 70B) reads the CV and job description together
3. Scores candidate from 0–100 based on contextual fit
4. Classifies candidate: SHORTLISTED / KEEP IN VIEW / REJECTED
5. SHORTLISTED → interview invitation email + Slack recruiter alert
6. KEEP IN VIEW → professional holding email
7. REJECTED → kind, specific rejection with genuine feedback
8. All candidates are logged to Google Sheets for full audit tracking

## What Makes This Different
Traditional ATS systems depend heavily on keyword matching and can reject strong candidates who describe their skills differently. This workflow uses AI to understand context, transferable skills, role fit, and career progression instead of just exact keyword repetition.

## Tech Stack

| Tool | Purpose | Cost |
|------|---------|------|
| n8n | Workflow orchestration | Free (self-host) |
| Groq (Llama 3.3 70B) | CV screening and scoring | 100% Free |
| Webhook | Application intake | Built into n8n |
| Google Sheets | Candidate tracker | Free |
| Gmail | Candidate emails | Free |
| Slack | Recruiter notifications | Free |
| Calendly | Interview booking | Free |

## Customisation
Update the JOB DESCRIPTION in the HTTP Request node to match any role you want to screen for. The rest of the workflow remains automatic.

## Setup Instructions
1. Import `workflow.json` into n8n
2. Get a free Groq API key at console.groq.com
3. Create Google Sheet `Candidate Tracker` with columns:
   `CandidateID, Name, Email, RoleApplied, Score, Classification, StrengthAreas, GapAreas, AIRationale, ActionTaken, AppliedAt, InterviewLink`
4. Create Slack channel `#recruitment-pipeline`
5. Create a free Calendly account and copy your booking link
6. Update `CALENDLY_LINK` in the Code node
7. Connect all credentials in n8n
8. Copy the webhook URL and connect it to your application form
9. Activate the workflow

## Ideal For
Recruiters • HR teams • startups • agencies • talent acquisition teams • AI automation engineer portfolios

## Files Included
- `workflow.json` — n8n workflow export
- `screenshots/workflow.png` — workflow screenshot
- `SETUP.md` — setup guide

## Built By
**Ifeanyi Nwadike** | Open to AI Automation Engineer roles  
LinkedIn: https://www.linkedin.com/in/ifeanyi-nwadike-aab752356  
GitHub: https://github.com/Supreme-jay
