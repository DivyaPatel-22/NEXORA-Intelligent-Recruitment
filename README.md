# 🚀 NEXORA — Intelligent Recruitment Engine

### *Transforming Recruitment with AI, Automation & Human Intelligence*

NEXORA is an AI-powered recruitment management application built on **ServiceNow** that streamlines the end-to-end hiring process. From creating job openings and screening candidates to scheduling interviews, analyzing feedback, and supporting final hiring decisions, NEXORA brings recruitment activities together in one intelligent workflow.

**Screen smarter. Hire faster. Make informed decisions.**

---

## 💡 Problem Statement

Traditional recruitment involves repetitive manual tasks, time-consuming resume screening, interview coordination challenges, and fragmented candidate information. These challenges can delay hiring and make it difficult for recruiters to consistently evaluate candidates.

## ✨ Our Solution

NEXORA combines ServiceNow's workflow automation with AI-assisted candidate evaluation and recruitment analytics to create a structured, transparent, and efficient hiring process.

The platform helps recruiters reduce repetitive coordination, identify relevant candidate strengths and skill gaps, consolidate interview feedback, and make informed decisions with human oversight.

## 🌟 Key Features

- **📋 Smart Job Management** — Create and manage job openings with skills, qualifications, experience, location, and employment details.
- **🧠 AI-Powered Candidate Screening** — Generate candidate fit scores, strengths, skill gaps, and screening recommendations using configured AI skills.
- **🔄 Automated Recruitment Workflow** — Track applications through screening, shortlisting, interviews, and final decisions.
- **📅 Intelligent Interview Management** — Create interview records, manage schedules and statuses, and send configured interview reminders.
- **💬 AI Interview Feedback Analysis** — Consolidate interviewer feedback into summaries, strengths, weaknesses, scores, and recommendations.
- **🎯 Hiring Recommendation Management** — Support recruiter review and final decision recording.
- **📩 Automated Notifications** — Notify relevant participants when configured recruitment events occur.
- **📊 Recruitment Analytics Dashboard** — Monitor candidate pipelines, job openings, application statuses, interviews, and hiring outcomes.

## 🔄 End-to-End Workflow

```text
Job Opening Creation
        ↓
Candidate Registration & Application
        ↓
AI-Powered Candidate Screening
        ↓
Fit Score • Strengths • Skill Gaps
        ↓
Recruiter Review & Shortlisting
        ↓
Interview Scheduling & Reminders
        ↓
Interview Feedback Collection
        ↓
AI Feedback Consolidation
        ↓
Human-Reviewed Hiring Decision
        ↓
Notifications & Analytics Dashboard
```

Each stage connects to the next through recruitment records and configured ServiceNow workflows, helping recruiters maintain visibility across the hiring lifecycle.

## 🏗️ Application Architecture

NEXORA is organized around five functional layers:

1. **Presentation Layer** — ServiceNow application forms, records, and recruitment dashboard.
2. **Workflow Automation Layer** — Flow Designer workflows for screening, interviews, feedback, and notifications.
3. **AI Intelligence Layer** — Configured AI skills for candidate screening and feedback consolidation.
4. **Data Layer** — Custom tables for candidates, job openings, applications, interviews, feedback, and hiring recommendations.
5. **Analytics Layer** — Dashboard metrics and reports for recruitment progress and outcomes.

## 🛠️ Technology Stack

| Component                 | Technology                                              |
| ------------------------- | ------------------------------------------------------- |
| Application Platform      | ServiceNow                                              |
| Development Environment   | ServiceNow Studio                                       |
| Workflow Automation       | ServiceNow Flow Designer                                |
| AI Capabilities           | Configured ServiceNow AI Skills                         |
| Data Management           | ServiceNow Custom Tables & Reference Fields             |
| Analytics & Visualization | ServiceNow Platform Analytics                           |
| Version Control           | GitHub                                                  |
| Application Export        | ServiceNow Source Control metadata and XML update files |

*AI providers, credentials, and external integrations depend on the instance configuration.*

## 🗃️ Core Data Model

NEXORA uses six core custom tables to organize recruitment information:

| Table                 | Purpose                                                          |
| --------------------- | ---------------------------------------------------------------- |
| Candidate             | Maintains candidate information                                  |
| Job Opening           | Stores job requirements and opening details                      |
| Application           | Connects candidates to job openings and stores screening results |
| Hiring Recommendation | Records recommendations and hiring decisions                     |
| Interview             | Manages interview schedules and status                           |
| Interview Feedback    | Stores interviewer ratings, comments, and assessments            |

These records provide the foundation for the application's workflow automation and reporting.

## 📈 Recruitment Dashboard

The dashboard provides a consolidated view of recruitment activity, including:

- Total candidates
- Active job openings
- Total applications
- Average candidate fit score
- Scheduled interviews
- Selected and rejected candidates
- Candidate pipeline visualization
- Applications by status
- Hiring recommendation distribution

Dashboard metrics depend on the available records and report configuration.

## ⚙️ Setup & Access

**NEXORA is a ServiceNow application, not a standalone application that can be launched directly using Node.js or Python.**

To inspect or restore the project:

1. Obtain access to a compatible ServiceNow instance with the necessary application development permissions.
2. Clone or download this repository's ServiceNow source-control branch.
3. Review the exported application metadata, dictionary files, and update records.
4. Follow the supported source-control or application import procedure for your ServiceNow release.
5. Configure required AI skills, credential records, email settings, access controls, and other dependencies in the target instance.
6. Test all tables, workflows, AI actions, notifications, and dashboard reports before use.

**Important:** The repository contains tracked ServiceNow application exports. It is not guaranteed to contain every live record, credential, secret, or environment-specific setting required for a complete restoration.

## 🧪 Validation Checklist

- [ ] Job openings can be created and managed.
- [ ] Candidate applications link to the correct records.
- [ ] AI screening produces the expected results.
- [ ] Recruiters can review and update application decisions.
- [ ] Interview creation and reminder workflows operate correctly.
- [ ] Interview feedback is linked to the correct interview.
- [ ] AI feedback consolidation populates expected fields.
- [ ] Hiring decision notifications work with the configured email setup.
- [ ] Dashboard figures match the underlying test records.
- [ <img width="1254" height="1254" alt="ChatGPT Image Aug 26, 2026, 12_18_09 PM" src="https://github.com/user-attachments/assets/f7fda2a5-d44f-44cf-aee6-59bc5f92b715" />
] Access controls protect candidate information.

## 🔐 Responsible AI & Security

NEXORA is designed to **assist recruiters, not replace human judgment**.

- AI scores and recommendations should be reviewed before making hiring decisions.
- Candidate information should be handled according to applicable privacy and retention requirements.
- Never commit API keys, passwords, personal access tokens, or confidential candidate data to GitHub.
- Verify access controls and AI-provider data handling before using real candidate information.

## 🚀 Future Enhancements

- Dedicated recruiter and candidate user experiences.
- More structured and explainable AI screening results.
- Enhanced interview availability and scheduling.
- Improved recruitment analytics and configurable reports.
- Automated workflow testing and stronger error handling.
- Documented, tested application restoration procedures.

## 🎯 Project Impact

NEXORA demonstrates how **AI-assisted evaluation, workflow automation, structured data, and analytics** can work together to modernize recruitment.

By connecting screening, interviews, feedback, and decisions into a unified process, NEXORA aims to reduce manual coordination and give recruiters better visibility throughout the candidate journey.

---

### 🌐 NEXORA Intelligent Recruitment Engine

**Screen. Evaluate. Interview. Decide.**

*Built to make recruitment more connected, consistent, and intelligent.*
