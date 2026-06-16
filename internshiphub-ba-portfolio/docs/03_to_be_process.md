# 03. TO-BE Process Analysis

## 1. Purpose

This document describes the future internship recruitment process after implementing the InternshipHub system.

The goal of TO-BE analysis is to design a better workflow that solves the pain points found in the AS-IS process.

## 2. Future Process Summary

In the future process, InternshipHub will be used as a centralized system for managing internship applications, candidate status, interview scheduling, interviewer feedback, and hiring decisions.

Instead of using many separate tools such as email, spreadsheets, and chat applications, HR can manage the recruitment pipeline in one system.

## 3. TO-BE Process Steps

| Step | Actor | Future Activity | System Support |
|---|---|---|---|
| 1 | Candidate | Creates account and submits application | Application form |
| 2 | Candidate | Uploads CV and personal information | Profile and CV upload |
| 3 | System | Validates required information | Form validation |
| 4 | HR Recruiter | Views new applications | Candidate dashboard |
| 5 | HR Recruiter | Screens candidate profile | Candidate detail page |
| 6 | HR Recruiter | Updates candidate status | Status management |
| 7 | System | Sends status notification to candidate | Email notification |
| 8 | HR Recruiter | Schedules interview and assigns interviewer | Interview scheduling |
| 9 | Interviewer | Views assigned interview and candidate profile | Interviewer dashboard |
| 10 | Interviewer | Submits structured feedback | Feedback form |
| 11 | Hiring Manager | Reviews candidate pipeline and feedback | Pipeline dashboard |
| 12 | Hiring Manager | Makes or approves final decision | Decision management |
| 13 | HR Recruiter | Sends offer or rejection result | Result notification |
| 14 | System | Stores status history and activity log | Audit log |

## 4. Main Improvements from AS-IS to TO-BE

| AS-IS Problem | TO-BE Improvement |
|---|---|
| Candidate data is stored in many places. | Candidate data is centralized in one system. |
| HR updates candidate status manually in spreadsheets. | HR updates status directly in the system. |
| Candidate does not know the current status. | Candidate can view application status. |
| Interview scheduling is done through chat or email. | HR can schedule interviews in the system. |
| Feedback is sent in different formats. | Interviewer submits structured feedback form. |
| Hiring manager lacks pipeline visibility. | Hiring manager can view dashboard and candidate pipeline. |
| No clear status history. | System stores status history and activity log. |

## 5. Future Candidate Status Flow

The candidate status flow should be:

```text
Draft → Submitted → Screening → Interview Scheduled → Interview Completed → Offered / Rejected / Hold