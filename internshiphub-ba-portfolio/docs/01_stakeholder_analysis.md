# 01. Stakeholder Analysis

## 1. Purpose

This document identifies the key stakeholders of the InternshipHub system and explains their roles, needs, influence, and involvement in the project.

Stakeholder analysis helps the Business Analyst understand who will use the system, who will make decisions, who will provide requirements, and who will be affected by the final solution.

## 2. Stakeholder List

| Stakeholder | Description | Main Needs | Influence | Interest |
|---|---|---|---|---|
| Candidate | A student or fresh graduate who applies for an internship program. | Submit application, upload CV, track application status, receive updates. | Low | High |
| HR Recruiter | The person who manages the recruitment process. | Screen candidates, update status, schedule interviews, send results. | High | High |
| Interviewer | A technical or business team member who interviews candidates. | View candidate profile, review CV, submit interview feedback. | Medium | Medium |
| Hiring Manager | The person who makes or approves the final hiring decision. | View recruitment pipeline, compare candidates, approve decisions. | High | High |
| System Admin | The person who manages system users, roles, and configurations. | Manage accounts, permissions, internship programs, and activity logs. | Medium | Medium |
| Developer | The person who builds the system based on requirements. | Receive clear functional requirements and business rules. | Medium | High |
| QA Engineer | The person who tests the system quality. | Receive testable acceptance criteria and test scenarios. | Medium | High |

## 3. Stakeholder Goals

| Stakeholder | Goal |
|---|---|
| Candidate | Complete the application process easily and know the current status. |
| HR Recruiter | Manage candidates efficiently and reduce manual tracking work. |
| Interviewer | Evaluate candidates using a clear and structured feedback form. |
| Hiring Manager | Make faster and better hiring decisions based on pipeline data. |
| System Admin | Ensure the system is secure and users have correct permissions. |
| Developer | Build the correct features with fewer requirement changes. |
| QA Engineer | Test the system based on clear business rules and expected results. |

## 4. Stakeholder Pain Points

| Stakeholder | Current Pain Point |
|---|---|
| Candidate | Does not know whether the application is received, reviewed, rejected, or moved to the next round. |
| HR Recruiter | Needs to track candidates manually using spreadsheets, email, and chat tools. |
| Interviewer | May receive candidate information late or in an unstructured format. |
| Hiring Manager | Cannot easily see the full recruitment pipeline and candidate comparison. |
| System Admin | Needs to control access to sensitive candidate information. |
| Developer | May receive unclear requirements if the business process is not documented well. |
| QA Engineer | May find it hard to test if acceptance criteria are missing or vague. |

## 5. RACI Matrix

RACI is used to clarify responsibility in a project.

- R = Responsible: Person who does the work.
- A = Accountable: Person who owns the final decision.
- C = Consulted: Person who gives input.
- I = Informed: Person who needs to be updated.

| Activity | Candidate | HR Recruiter | Interviewer | Hiring Manager | Admin | Developer | QA Engineer |
|---|---|---|---|---|---|---|---|
| Submit application | R | I | I | I | I | I | I |
| Screen CV | I | R/A | I | C | I | I | I |
| Update candidate status | I | R/A | I | C | I | I | I |
| Schedule interview | I | R/A | C | I | I | I | I |
| Conduct interview | I | C | R/A | I | I | I | I |
| Submit feedback | I | I | R/A | C | I | I | I |
| Make final decision | I | C | C | R/A | I | I | I |
| Manage users and roles | I | C | I | I | R/A | I | I |
| Build system features | I | C | C | C | C | R/A | C |
| Test system features | I | C | C | C | C | C | R/A |

## 6. Stakeholder Communication Plan

| Stakeholder | Communication Method | Frequency | Main Topics |
|---|---|---|---|
| HR Recruiter | Interview / Workshop | Weekly during discovery | Recruitment process, pain points, business rules |
| Interviewer | Short interview | Once per feedback feature | Interview flow, evaluation form, feedback criteria |
| Hiring Manager | Review meeting | At milestone | Pipeline dashboard, decision process, reports |
| Candidate | Survey / Prototype review | Once during validation | Application flow, status tracking, notification |
| Developer | Requirement walkthrough | Each sprint | Functional requirements, business rules, edge cases |
| QA Engineer | Test review | Each sprint | Acceptance criteria, test scenarios, expected results |
| Admin | Interview | Once during discovery | Roles, permissions, system configuration |

## 7. BA Notes

The most important stakeholder in this project is the HR Recruiter because HR manages the main recruitment workflow. However, the Candidate experience is also important because one of the business goals is to make the recruitment process more transparent.

The BA should work closely with HR to understand the current process, then validate the future process with interviewers and hiring managers.