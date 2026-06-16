# 06. User Stories and Product Backlog

## 1. Purpose

This document converts the software requirements from the SRS into user stories and organizes them into a product backlog.

The product backlog helps the team understand what should be built, who needs each feature, why the feature is valuable, and how important each item is for the first release of InternshipHub.

## 2. Backlog Scope

This backlog covers the core recruitment workflow of InternshipHub:

- Candidate application submission
- Candidate status tracking
- HR candidate management
- Interview scheduling
- Interview feedback
- Hiring manager decision support
- Admin and access control

## 3. User Story Format

All user stories follow this format:

```text
As a [user role], I want [goal], so that [business value].
```

Example:

```text
As a candidate, I want to view my application status, so that I can know my recruitment progress.
```

## 4. Priority Method

This backlog uses the MoSCoW priority method.

| Priority | Meaning |
|---|---|
| Must | Required for the first usable version |
| Should | Important, but can be released after core features |
| Could | Nice to have if time and resources allow |
| Won't | Not included in this version |

## 5. Epic List

| Epic ID | Epic Name | Description |
|---|---|---|
| EP-01 | Candidate Application | Candidate registration, login, profile, CV upload, and application submission |
| EP-02 | Candidate Status Tracking | Candidate views application status and receives updates |
| EP-03 | HR Candidate Management | HR views, searches, filters, screens, and updates candidates |
| EP-04 | Interview Scheduling | HR schedules interviews and assigns interviewers |
| EP-05 | Interview Feedback | Interviewer views assigned candidates and submits structured feedback |
| EP-06 | Hiring Decision | Hiring manager reviews pipeline, feedback, and final decisions |
| EP-07 | Admin and Access Control | Admin manages users, roles, programs, and permissions |

## 6. Product Backlog

### EP-01: Candidate Application

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-01 | As a candidate, I want to register an account using email and password, so that I can access the InternshipHub system. | Must | FR-01 | Draft |
| US-02 | As a candidate, I want to log in and log out, so that I can securely use my account. | Must | FR-02 | Draft |
| US-03 | As a candidate, I want to create and update my personal profile, so that HR can review my information. | Must | FR-03 | Draft |
| US-04 | As a candidate, I want to upload my CV, so that HR can evaluate my application. | Must | FR-04, FR-05 | Draft |
| US-05 | As a candidate, I want to apply for an available internship program, so that I can be considered for the position. | Must | FR-06 | Draft |
| US-06 | As a candidate, I want to view my submitted application, so that I can check the information I provided. | Must | FR-07 | Draft |

### EP-02: Candidate Status Tracking

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-07 | As a candidate, I want to view my current application status, so that I can know my recruitment progress. | Must | FR-08 | Draft |
| US-08 | As a candidate, I want to receive a notification when my application status changes, so that I do not need to contact HR manually. | Should | FR-09 | Draft |
| US-09 | As a candidate, I want to view interview information when my interview is scheduled, so that I can prepare on time. | Should | FR-17, FR-18 | Draft |

### EP-03: HR Candidate Management

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-10 | As an HR recruiter, I want to view all submitted applications, so that I can manage candidates in one place. | Must | FR-10 | Draft |
| US-11 | As an HR recruiter, I want to search candidates by name, email, or internship program, so that I can find candidates quickly. | Must | FR-11 | Draft |
| US-12 | As an HR recruiter, I want to filter candidates by status, program, and applied date, so that I can manage the recruitment pipeline efficiently. | Must | FR-12 | Draft |
| US-13 | As an HR recruiter, I want to view candidate profile and CV, so that I can screen candidates properly. | Must | FR-13 | Draft |
| US-14 | As an HR recruiter, I want to update candidate recruitment status, so that the candidate pipeline stays accurate. | Must | FR-14 | Draft |
| US-15 | As an HR recruiter, I want the system to validate status transitions, so that invalid recruitment status changes are prevented. | Must | FR-15 | Draft |
| US-16 | As an HR recruiter, I want every status change to be recorded, so that the recruitment process can be tracked and audited. | Must | FR-16 | Draft |
| US-17 | As an HR recruiter, I want to send offer or rejection results, so that candidates receive official recruitment outcomes. | Should | FR-19 | Draft |

### EP-04: Interview Scheduling

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-18 | As an HR recruiter, I want to schedule interviews, so that selected candidates can move to the interview stage. | Must | FR-17 | Draft |
| US-19 | As an HR recruiter, I want to assign interviewers to candidates, so that each interview has a responsible evaluator. | Must | FR-18 | Draft |
| US-20 | As an HR recruiter, I want interview details to be visible to assigned interviewers, so that interviewers can prepare before the interview. | Must | FR-18, FR-20 | Draft |

### EP-05: Interview Feedback

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-21 | As an interviewer, I want to view my assigned interviews, so that I know which candidates I need to interview. | Must | FR-20 | Draft |
| US-22 | As an interviewer, I want to view assigned candidate profile and CV, so that I can prepare for the interview. | Must | FR-21 | Draft |
| US-23 | As an interviewer, I want to submit structured interview feedback, so that HR and hiring manager can make better decisions. | Must | FR-22 | Draft |
| US-24 | As an interviewer, I want to provide rating, comments, and recommendation, so that feedback is clear and useful. | Must | FR-23 | Draft |
| US-25 | As an interviewer, I want to recommend Pass, Fail, or Hold, so that the next recruitment action is easier to decide. | Must | FR-24 | Draft |
| US-26 | As an interviewer, I want to access only candidates assigned to me, so that candidate information remains secure. | Must | FR-25 | Draft |

### EP-06: Hiring Decision

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-27 | As a hiring manager, I want to view the recruitment pipeline, so that I can monitor hiring progress. | Should | FR-26 | Draft |
| US-28 | As a hiring manager, I want to view candidate feedback, so that I can understand interviewer evaluation. | Should | FR-27 | Draft |
| US-29 | As a hiring manager, I want to compare candidates by status, rating, and feedback, so that I can make better hiring decisions. | Could | FR-28 | Draft |
| US-30 | As a hiring manager, I want to approve final hiring decisions, so that offers are controlled before being sent. | Should | FR-29 | Draft |

### EP-07: Admin and Access Control

| Story ID | User Story | Priority | Related FR | Status |
|---|---|---|---|---|
| US-31 | As a system admin, I want to create, update, and deactivate user accounts, so that system access can be managed. | Must | FR-30 | Draft |
| US-32 | As a system admin, I want to assign user roles, so that each user has correct permissions. | Must | FR-31 | Draft |
| US-33 | As a system admin, I want to create and update internship programs, so that HR can manage different recruitment campaigns. | Should | FR-32 | Draft |
| US-34 | As a system admin, I want to view system activity logs, so that important actions can be audited. | Should | FR-33 | Draft |

## 7. MVP Backlog

The MVP should include only the most important features needed for the first usable version.

| MVP Area | Included User Stories | Reason |
|---|---|---|
| Candidate application | US-01, US-02, US-03, US-04, US-05, US-06 | Candidate must be able to create and submit an application. |
| Candidate status tracking | US-07 | Candidate must be able to see application progress. |
| HR candidate management | US-10, US-11, US-12, US-13, US-14, US-15, US-16 | HR must be able to manage the recruitment pipeline. |
| Interview scheduling | US-18, US-19, US-20 | HR must be able to schedule interviews and assign interviewers. |
| Interview feedback | US-21, US-22, US-23, US-24, US-25, US-26 | Interviewer must be able to evaluate candidates. |
| Basic access control | US-31, US-32 | The system must protect candidate information. |

## 8. Release Plan

| Release | Goal | User Stories |
|---|---|---|
| Release 1 | MVP recruitment workflow | US-01 to US-07, US-10 to US-16, US-18 to US-26, US-31, US-32 |
| Release 2 | Candidate notification and result communication | US-08, US-09, US-17 |
| Release 3 | Hiring manager dashboard and decision support | US-27, US-28, US-29, US-30 |
| Release 4 | Admin configuration and audit improvement | US-33, US-34 |

## 9. Dependency Notes

| Dependency ID | Dependency |
|---|---|
| DEP-01 | Candidate must create an account before submitting an application. |
| DEP-02 | Candidate must upload a valid CV before application submission. |
| DEP-03 | HR must screen a candidate before scheduling an interview. |
| DEP-04 | HR must assign an interviewer before interview feedback can be submitted. |
| DEP-05 | Interview feedback should be submitted before the final hiring decision. |
| DEP-06 | User roles must be configured before access control can work correctly. |

## 10. Definition of Ready

A user story is ready for development when:

| Criteria | Description |
|---|---|
| Clear user role | The story identifies who needs the feature. |
| Clear goal | The story explains what the user wants to do. |
| Clear value | The story explains why the feature is useful. |
| Related requirement | The story is linked to at least one functional requirement. |
| Acceptance criteria | The story has clear acceptance criteria. |
| No major open question | Important ambiguity has been clarified. |

## 11. Definition of Done

A user story is done when:

| Criteria | Description |
|---|---|
| Feature implemented | The expected behavior is built. |
| Acceptance criteria passed | All acceptance criteria are satisfied. |
| Validation handled | Required validation rules are implemented. |
| Permission checked | Access control works correctly. |
| Tested by QA | Test scenarios are passed. |
| Reviewed by stakeholder | BA, Product Owner, or business user confirms the result. |

## 12. BA Notes

User stories help the BA communicate requirements in a user-centered way. They make it easier for the team to understand who needs the feature, what the user wants to do, and why the feature matters.

In this project, the highest priority user stories are related to candidate application, HR candidate management, interview scheduling, structured feedback, and access control.

The next step is to write acceptance criteria for selected user stories so that each story becomes clear and testable.
