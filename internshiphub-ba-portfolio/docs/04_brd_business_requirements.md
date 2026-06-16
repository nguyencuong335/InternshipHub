# 04. Business Requirements Document

## 1. Purpose

This document defines the business requirements for the InternshipHub system.

The purpose of this BRD is to describe what the business needs, why the system is needed, who will benefit from the system, and what business rules the solution must follow.

## 2. Business Problem

The current internship recruitment process is fragmented across email, spreadsheets, chat tools, and manual notes. This makes it difficult for HR to track candidate status, schedule interviews, collect feedback, and provide timely updates to candidates.

As the number of applicants increases, the process becomes harder to manage, less transparent, and more error-prone.

## 3. Business Objectives

| Objective ID | Business Objective | Success Measure |
|---|---|---|
| BO-01 | Centralize internship application management in one system. | HR can manage all candidates from one dashboard. |
| BO-02 | Reduce manual tracking work for HR. | HR uses fewer spreadsheets and manual notes. |
| BO-03 | Improve candidate status transparency. | Candidate can view their current application status. |
| BO-04 | Standardize interview feedback. | Interviewers use one structured feedback form. |
| BO-05 | Improve hiring decision visibility. | Hiring manager can view candidate pipeline and feedback. |
| BO-06 | Improve recruitment process traceability. | Status history and important actions are stored in the system. |

## 4. Business Requirements

| Requirement ID | Business Requirement | Priority | Owner |
|---|---|---|---|
| BR-01 | The system shall allow candidates to submit internship applications online. | Must | HR Recruiter |
| BR-02 | The system shall allow candidates to upload their CV and personal information. | Must | HR Recruiter |
| BR-03 | The system shall allow HR to view and manage all submitted applications. | Must | HR Recruiter |
| BR-04 | The system shall allow HR to update candidate recruitment status. | Must | HR Recruiter |
| BR-05 | The system shall allow HR to schedule interviews and assign interviewers. | Must | HR Recruiter |
| BR-06 | The system shall allow interviewers to view assigned candidates. | Must | Interviewer |
| BR-07 | The system shall allow interviewers to submit structured interview feedback. | Must | Interviewer |
| BR-08 | The system shall allow hiring managers to view recruitment pipeline and candidate feedback. | Should | Hiring Manager |
| BR-09 | The system shall notify candidates when their application status changes. | Should | HR Recruiter |
| BR-10 | The system shall store status history for tracking and audit purposes. | Must | HR Recruiter |
| BR-11 | The system shall support role-based access control for different user types. | Must | System Admin |

## 5. Business Rules

| Rule ID | Business Rule |
|---|---|
| RULE-01 | A candidate cannot submit an application without required personal information and CV. |
| RULE-02 | A candidate can only view their own application status. |
| RULE-03 | Only HR Recruiter can update candidate recruitment status. |
| RULE-04 | Only HR Recruiter can schedule interviews and assign interviewers. |
| RULE-05 | Interviewer can only view candidates assigned to them. |
| RULE-06 | Interviewer feedback is required before a final hiring decision is made. |
| RULE-07 | Every candidate status change must be recorded with old status, new status, updated by, and updated time. |
| RULE-08 | Hiring Manager can view candidate pipeline but cannot directly edit candidate profile information. |
| RULE-09 | Rejected candidates cannot be moved directly to Offered without HR manager approval. |

## 6. Assumptions

| Assumption ID | Assumption |
|---|---|
| A-01 | Candidates will apply through the InternshipHub system. |
| A-02 | HR Recruiter is responsible for managing candidate status. |
| A-03 | Interviewers will submit feedback through the system after interviews. |
| A-04 | Hiring Manager will use dashboard information to support hiring decisions. |
| A-05 | Email will be used as the main notification channel. |

## 7. Constraints

| Constraint ID | Constraint |
|---|---|
| C-01 | The first version of the system should focus on core recruitment workflow only. |
| C-02 | The system should not include AI-based CV screening in the first version. |
| C-03 | The system should not include payroll or employee onboarding features. |
| C-04 | Candidate personal data must be protected by role-based access control. |
| C-05 | CV upload should support common document formats such as PDF and DOCX. |

## 8. Success Metrics

| Metric ID | Success Metric | Target |
|---|---|---|
| M-01 | Manual spreadsheet tracking effort | Reduce by 50% |
| M-02 | Candidate status inquiry messages | Reduce by 40% |
| M-03 | Interview feedback completion rate | At least 95% |
| M-04 | Average time from application submission to screening | Reduce by 30% |
| M-05 | Candidate status update accuracy | At least 95% |

## 9. Scope

### In Scope

- Candidate application submission
- Candidate profile and CV upload
- HR candidate screening
- Candidate status management
- Interview scheduling
- Interviewer feedback submission
- Hiring manager pipeline overview
- Candidate status notification
- Status history tracking
- Role-based access control

### Out of Scope

- AI-based CV screening
- Online coding test
- Payroll management
- Employee onboarding
- Integration with external HRM systems
- Full production-level implementation

## 10. BA Notes

This BRD focuses on business-level needs, not technical implementation details.

The most important business requirements are candidate application submission, HR status management, interview scheduling, structured feedback, and candidate status tracking.

The next step is to convert these business requirements into more detailed software requirements in the SRS document.