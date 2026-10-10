# NEXORA Intelligent Recruitment

**AI-powered recruitment management built on ServiceNow**

NEXORA is a ServiceNow application designed to organize job openings,
candidate applications, AI-assisted screening, interview scheduling,
feedback, hiring recommendations, notifications, and recruitment
analytics.

> **Repository note:** This repository contains a ServiceNow
> source-control export, not a standalone application that can be
> launched with `npm start` or `python app.py`. A compatible ServiceNow
> instance and appropriate configuration are required.

## Problem Statement

Recruitment involves repetitive work across job descriptions, candidate
records, application screening, interview coordination, feedback
collection, and hiring decisions. When these tasks are managed
separately, recruiters can lose time coordinating the process and may
struggle to track candidate progress consistently.

NEXORA brings these activities together in one ServiceNow application
and uses AI-assisted screening and feedback summaries to support
recruiter decisions.

## Solution Overview

NEXORA combines structured recruitment records, ServiceNow workflow
automation, configured AI skills, notifications, and a dashboard. It
aims to reduce manual coordination and provide a consistent candidate
pipeline. AI recommendations are decision-support information;
recruiters remain responsible for final hiring decisions.

## Key Features

-   **Job opening management:** Store role, department, location,
    employment type, skills, experience, education, deadline, and
    position count.
-   **AI-assisted job descriptions:** Store generated job-description
    content with a job opening.
-   **Candidate and application tracking:** Link candidates to jobs and
    track application status.
-   **AI candidate screening:** Populate fit score, strengths, skill
    gaps, screening status, and recommendation when the configured skill
    and flow succeed.
-   **Hiring recommendations:** Record AI-assisted recommendations and
    recruiter decisions.
-   **Interview management:** Track interview date, status, type, mode,
    interviewer, duration, and meeting details.
-   **Interview reminders:** Send reminders when the flow and email
    configuration allow.
-   **Interview feedback:** Capture technical, communication, and
    problem-solving ratings and comments.
-   **AI feedback consolidation:** Summarize feedback into scores,
    strengths, weaknesses, and a recommendation when configured
    correctly.
-   **Decision notifications:** Notify relevant people when a final
    decision is recorded, subject to email configuration.
-   **Recruitment dashboard:** Show high-level metrics and charts for
    candidates, openings, applications, fit scores, interviews, and
    outcomes.

Feature availability depends on the exported configuration, permissions,
ServiceNow release, and successful setup of AI skills and flows.

## End-to-End Workflow

1.  Create a job opening and enter its requirements.
2.  Register or select a candidate.
3.  Create an application linked to the candidate and job.
4.  Run AI-assisted screening.
5.  Review the fit score, strengths, skill gaps, and recommendation.
6.  Have a recruiter shortlist, hold, or reject the application.
7.  Schedule an interview.
8.  Send interview reminders if configured.
9.  Collect interview feedback.
10. Consolidate feedback using the configured AI workflow.
11. Have a recruiter review the evidence and record the final decision.
12. Send configured notifications and review dashboard metrics.

``` text
Job Opening
    |
Candidate + Application
    |
AI-assisted Screening
    |
Recruiter Review
    |
Shortlist / Hold / Reject
    |
Interview Scheduling + Reminder
    |
Interview Feedback
    |
AI Feedback Consolidation
    |
Human-reviewed Hiring Decision
    |
Notification + Dashboard
```

## Technology Stack

  -----------------------------------------------------------------------
  Area                                Technology
  ----------------------------------- -----------------------------------
  Application platform                ServiceNow

  Development environment             ServiceNow Studio / custom
                                      application

  Data                                ServiceNow custom tables and
                                      reference fields

  Workflow automation                 ServiceNow Flow Designer

  AI-assisted evaluation              Configured ServiceNow AI skills and
                                      skill execution actions

  Analytics                           ServiceNow Platform Analytics /
                                      dashboard

  Version control                     GitHub connected through ServiceNow
                                      Source Control

  Export format                       ServiceNow application metadata and
                                      XML update files
  -----------------------------------------------------------------------

Confirm the specific AI provider and dependencies in the instance
configuration. Credentials and secrets must not be stored in this
repository.

## Application Data Model

The core custom tables are:

-   **Candidate** --- Candidate profile details.
-   **Job Opening** --- Job requirements and opening information.
-   **Application** --- Candidate/job relationship, status, and
    screening results.
-   **Hiring Recommendation** --- Recommendation and final-decision
    information.
-   **Interview** --- Interview schedule, status, interviewer, and
    meeting details.
-   **Interview Feedback** --- Interview ratings and comments.

Review the exported metadata to confirm exact fields, references, choice
values, and dependencies.

## Automation and AI

Configured workflows cover candidate screening, hiring recommendations,
interview creation and reminders, feedback consolidation, and decision
notifications. AI results can vary with input quality, prompt design,
provider behavior, and configuration. If fields are blank or unexpected,
review flow execution details and AI skill outputs.

**Human review is required.** Do not use an AI fit score or
recommendation as the sole basis for hiring or rejection. Check outputs
for inaccuracies, inconsistent criteria, and potential bias.

## Dashboard and Reporting

The dashboard is intended to report total candidates, active job
openings, total applications, average fit score, interviews scheduled,
selected and rejected candidates, candidate pipeline, applications by
status, and hiring recommendations. Figures depend on the current
records and report definitions; validate them before presenting them as
production metrics.

## Setup and Access

This repository contains a **ServiceNow source-control export**, not a
conventional standalone software package.

1.  Use an authorized ServiceNow instance and confirm the required
    development/import permissions.
2.  Select the intended repository branch. The initial export was
    committed to `sn_instances/ltm-hck-2876-0039`.
3.  Download the branch as a ZIP and keep a separate backup.
4.  Review the application metadata, dictionary, update records, skill
    configurations, and source-control properties.
5.  Follow the supported import or source-control procedure for your
    ServiceNow release and application scope. Test in a non-production
    instance first.
6.  Reconfigure and validate AI providers, credential records, email
    settings, roles, access controls, and other dependencies in the
    target instance. Secrets should not be expected to restore from
    GitHub.
7.  Test the tables, forms, flows, AI skills, notifications, and
    dashboard before relying on the application.

Restoration steps vary by ServiceNow release and configuration. Do not
use **Pull from repository** on a working instance unless you understand
the impact and have a separate backup.

## Testing Checklist

-   [ ] Create a job opening and verify its status and requirements.
-   [ ] Link a candidate to an application.
-   [ ] Confirm screening completes and populates the expected fields.
-   [ ] Review screening results and record a recruiter decision.
-   [ ] Create and update an interview.
-   [ ] Verify interview reminders with the configured email setup.
-   [ ] Submit feedback and confirm it links to the correct interview.
-   [ ] Verify feedback consolidation populates expected fields.
-   [ ] Test final-decision notifications.
-   [ ] Compare dashboard counts and charts with test records.
-   [ ] Verify access controls for candidate information.
-   [ ] Ensure a human reviews AI outputs before a final decision.

## Limitations

-   GitHub stores tracked exported application files; it is **not a
    complete backup of the live ServiceNow instance**.
-   Runtime records, users, credentials, secrets, instance properties,
    and external service settings may not be included.
-   A successful push does not guarantee that the application can be
    restored without additional setup.
-   AI output quality depends on the input, prompts, provider, and
    configuration.
-   Reminders and notifications depend on email and notification
    configuration.
-   Dashboard accuracy depends on data quality and report definitions.
-   This README does not certify the export as production-ready.
-   The default `main` branch may differ from the ServiceNow
    source-control branch. Use the branch containing the intended
    export.

## Security and Privacy

-   Never commit GitHub tokens, passwords, API keys, secrets, or real
    candidate data.
-   Revoke and replace any token that has been exposed.
-   Limit repository and ServiceNow access to authorized people.
-   Handle candidate data according to applicable privacy and retention
    policies.
-   Prefer synthetic candidate data for demonstrations.
-   Review access controls and AI-provider data handling before using
    real candidate information.

## Future Enhancements

-   Add candidate-facing and recruiter-focused user experiences.
-   Improve structured AI outputs and validation.
-   Add clearer explanations and audit trails for recommendations.
-   Add configurable interview availability and scheduling rules.
-   Strengthen dashboard filters and report validation.
-   Add automated tests for flows and edge cases.
-   Document and test a release-specific restoration procedure.

## Project Summary

NEXORA Intelligent Recruitment demonstrates how ServiceNow records,
workflow automation, AI-assisted screening and feedback, notifications,
and analytics can be combined to manage an end-to-end recruitment
process while keeping recruiters responsible for final hiring decisions.
