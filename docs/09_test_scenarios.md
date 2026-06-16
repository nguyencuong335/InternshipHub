# 09. Test Scenarios

## 1. Purpose

This document defines test scenarios for the InternshipHub system.

The purpose of test scenarios is to help the BA, QA Engineer, Developer, and stakeholder verify that the system behavior matches the user stories, acceptance criteria, business rules, and software requirements.

## 2. Test Scenario Scope

This document covers the main test scenarios for:

- Candidate registration and login
- Candidate profile and CV upload
- Internship application submission
- Application status tracking
- HR candidate management
- Candidate status update
- Interview scheduling
- Interview feedback
- Hiring manager dashboard
- Admin user and role management
- Permission and access control

## 3. Test Scenario Format

| Field | Description |
|---|---|
| Test ID | Unique test scenario ID |
| Module | Functional area being tested |
| Scenario | What should be tested |
| Related User Story | User story connected to the scenario |
| Related Requirement | Functional requirement connected to the scenario |
| Test Type | Positive, Negative, Permission, Validation, or Business Rule |
| Expected Result | Expected system behavior |

## 4. Test Scenarios

---

## 4.1 Candidate Registration and Login

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-001 | Candidate Registration | Candidate registers with valid required information. | US-01 | FR-01 | Positive | Candidate account is created successfully. |
| TC-002 | Candidate Registration | Candidate registers with an email that already exists. | US-01 | FR-01 | Negative | System shows an error message that the email is already registered. |
| TC-003 | Candidate Registration | Candidate leaves required fields empty during registration. | US-01 | FR-01 | Validation | System shows validation messages for missing fields. |
| TC-004 | Login | Candidate logs in with correct email and password. | US-02 | FR-02 | Positive | Candidate is logged in and redirected to candidate dashboard. |
| TC-005 | Login | User logs in with incorrect email or password. | US-02 | FR-02 | Negative | System shows invalid login message. |
| TC-006 | Logout | Logged-in user clicks logout. | US-02 | FR-02 | Positive | User is logged out and redirected to login page. |
| TC-007 | Login | Deactivated user tries to log in. | US-02 | FR-02, FR-30 | Permission | System prevents login. |

---

## 4.2 Candidate Profile and CV Upload

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-008 | Candidate Profile | Candidate saves profile with valid required information. | US-03 | FR-03 | Positive | Profile is saved successfully. |
| TC-009 | Candidate Profile | Candidate leaves required profile fields empty. | US-03 | FR-03 | Validation | System shows validation messages. |
| TC-010 | Candidate Profile | Candidate updates existing profile with valid data. | US-03 | FR-03 | Positive | Updated profile information is saved. |
| TC-011 | CV Upload | Candidate uploads a valid PDF CV under 5MB. | US-04 | FR-04, FR-05 | Positive | CV is uploaded successfully. |
| TC-012 | CV Upload | Candidate uploads a valid DOCX CV under 5MB. | US-04 | FR-04, FR-05 | Positive | CV is uploaded successfully. |
| TC-013 | CV Upload | Candidate uploads unsupported file type. | US-04 | FR-05 | Negative | System rejects file and shows allowed file types. |
| TC-014 | CV Upload | Candidate uploads a CV file larger than 5MB. | US-04 | FR-05 | Validation | System rejects file and shows file size limit. |
| TC-015 | CV Upload | Candidate replaces existing CV before application submission. | US-04 | FR-04 | Positive | Old CV is replaced by the new CV. |

---

## 4.3 Internship Application Submission

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-016 | Application Submission | Candidate submits application with complete profile and valid CV. | US-05 | FR-06 | Positive | Application is created with Submitted status. |
| TC-017 | Application Submission | Candidate submits application without CV. | US-05 | FR-06 | Validation | System prevents submission and shows CV required message. |
| TC-018 | Application Submission | Candidate submits application without selecting internship program. | US-05 | FR-06 | Validation | System prevents submission and shows program required message. |
| TC-019 | Application Submission | Candidate applies to the same program more than once. | US-05 | FR-06 | Business Rule | System prevents duplicate application. |
| TC-020 | Application Submission | Candidate applies to a closed internship program. | US-05 | FR-06 | Business Rule | System prevents submission and shows program closed message. |
| TC-021 | Submitted Application | Candidate views own submitted application. | US-06 | FR-07 | Positive | Candidate can see submitted application information. |
| TC-022 | Submitted Application | Candidate tries to view another candidate's submitted application. | US-06 | FR-07, NFR-04 | Permission | System denies access. |

---

## 4.4 Candidate Status Tracking

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-023 | Application Status | Candidate views current application status. | US-07 | FR-08 | Positive | Current application status is displayed. |
| TC-024 | Application Status | Candidate views program name and submitted date. | US-07 | FR-08 | Positive | Program name and submitted date are displayed. |
| TC-025 | Application Status | Candidate tries to view another candidate's status. | US-07 | FR-08, NFR-04 | Permission | System denies access. |
| TC-026 | Application Status | Candidate views interview information after interview is scheduled. | US-09 | FR-17, FR-18 | Positive | Interview date, time, and meeting information are displayed. |
| TC-027 | Notification | Candidate receives notification after HR updates status. | US-08 | FR-09 | Positive | Candidate receives status update notification. |
| TC-028 | Notification | Status notification fails to send. | US-08 | FR-09 | Negative | System records notification failure. |

---

## 4.5 HR Candidate Management

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-029 | Candidate Management | HR views all submitted applications. | US-10 | FR-10 | Positive | Candidate list is displayed. |
| TC-030 | Candidate Management | HR views candidate list columns. | US-10 | FR-10 | Positive | Candidate name, email, program, status, and applied date are displayed. |
| TC-031 | Candidate Management | Unauthorized user tries to access candidate management page. | US-10 | FR-10, NFR-03 | Permission | System denies access. |
| TC-032 | Candidate Search | HR searches candidates by name. | US-11 | FR-11 | Positive | Matching candidates are displayed. |
| TC-033 | Candidate Search | HR searches candidates by email. | US-11 | FR-11 | Positive | Matching candidates are displayed. |
| TC-034 | Candidate Search | HR searches with no matching result. | US-11 | FR-11 | Negative | System shows empty result message. |
| TC-035 | Candidate Filter | HR filters candidates by status. | US-12 | FR-12 | Positive | Only candidates with selected status are displayed. |
| TC-036 | Candidate Filter | HR filters candidates by internship program. | US-12 | FR-12 | Positive | Only candidates in selected program are displayed. |
| TC-037 | Candidate Filter | HR combines status, program, and date filters. | US-12 | FR-12 | Positive | Candidates matching all filters are displayed. |
| TC-038 | Candidate Detail | HR views candidate profile and CV. | US-13 | FR-13 | Positive | Candidate profile and CV are displayed. |
| TC-039 | Candidate Detail | Unauthorized user tries to view candidate detail. | US-13 | FR-13, NFR-03 | Permission | System denies access. |

---

## 4.6 Candidate Status Update

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-040 | Status Update | HR updates candidate status from Submitted to Screening. | US-14 | FR-14, FR-15 | Positive | New status is saved successfully. |
| TC-041 | Status Update | HR updates status using valid transition. | US-15 | FR-15 | Positive | System accepts the transition. |
| TC-042 | Status Update | HR updates status using invalid transition. | US-15 | FR-15 | Business Rule | System prevents update and shows error message. |
| TC-043 | Status Update | HR tries to move candidate from Draft directly to Offered. | US-15 | FR-15 | Business Rule | System rejects the transition. |
| TC-044 | Status Update | HR updates a rejected candidate without required approval. | US-15 | FR-15 | Business Rule | System prevents update. |
| TC-045 | Status History | HR updates candidate status successfully. | US-16 | FR-16 | Positive | Old status, new status, updated by, and updated time are recorded. |
| TC-046 | Status History | HR views status history on candidate detail page. | US-16 | FR-16 | Positive | Status history is displayed. |
| TC-047 | Status History | Status update fails. | US-16 | FR-16 | Negative | Incorrect status history record is not created. |
| TC-048 | Status Update | Candidate views status after HR update. | US-14 | FR-14, FR-08 | Positive | Candidate sees latest status. |

---

## 4.7 Interview Scheduling

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-049 | Interview Scheduling | HR schedules interview with valid candidate, interviewer, date, time, and meeting information. | US-18 | FR-17 | Positive | Interview schedule is created successfully. |
| TC-050 | Interview Scheduling | HR schedules interview without selecting interviewer. | US-18 | FR-17 | Validation | System prevents scheduling and shows required field message. |
| TC-051 | Interview Scheduling | HR schedules interview for candidate not in Screening status. | US-18 | FR-17, FR-15 | Business Rule | System prevents scheduling and shows invalid status message. |
| TC-052 | Interview Scheduling | Interview is scheduled successfully. | US-18 | FR-17 | Positive | Candidate status changes to Interview Scheduled. |
| TC-053 | Interview Assignment | HR assigns interviewer to candidate. | US-19 | FR-18 | Positive | Interviewer can view assigned interview. |
| TC-054 | Interview Assignment | HR changes assigned interviewer. | US-19 | FR-18 | Positive | Old interviewer loses access and new interviewer gains access. |
| TC-055 | Interview Assignment | Non-HR user tries to assign interviewer. | US-19 | FR-18, NFR-03 | Permission | System denies access. |
| TC-056 | Interview Details | Assigned interviewer views interview details. | US-20 | FR-20 | Positive | Interview details are displayed. |

---

## 4.8 Interviewer Dashboard and Feedback

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-057 | Interviewer Dashboard | Interviewer views assigned interviews. | US-21 | FR-20 | Positive | Only assigned interviews are displayed. |
| TC-058 | Interviewer Dashboard | Interviewer views interview detail. | US-21 | FR-20 | Positive | Candidate name, program, date, time, and meeting information are displayed. |
| TC-059 | Interviewer Dashboard | Interviewer tries to view interview assigned to another interviewer. | US-21 | FR-20, NFR-05 | Permission | System denies access. |
| TC-060 | Candidate Profile | Assigned interviewer views candidate profile and CV. | US-22 | FR-21 | Positive | Candidate profile and CV are displayed. |
| TC-061 | Candidate Profile | Unassigned interviewer tries to view candidate profile and CV. | US-22 | FR-21, NFR-05 | Permission | System denies access. |
| TC-062 | Feedback Form | Assigned interviewer submits complete structured feedback. | US-23 | FR-22, FR-23 | Positive | Feedback is saved successfully. |
| TC-063 | Feedback Form | Interviewer submits feedback without required rating. | US-23 | FR-23 | Validation | System prevents submission and shows validation message. |
| TC-064 | Feedback Form | Interviewer submits feedback without recommendation. | US-25 | FR-24 | Validation | System prevents submission and shows recommendation required message. |
| TC-065 | Feedback Form | Unassigned interviewer tries to submit feedback. | US-23 | FR-22, NFR-05 | Permission | System denies access. |
| TC-066 | Feedback Visibility | HR views feedback after successful submission. | US-23 | FR-22 | Positive | Submitted feedback is visible to HR. |
| TC-067 | Recommendation | Interviewer selects Pass recommendation. | US-25 | FR-24 | Positive | Pass recommendation is saved. |
| TC-068 | Recommendation | Interviewer selects Fail recommendation. | US-25 | FR-24 | Positive | Fail recommendation is saved. |
| TC-069 | Recommendation | Interviewer selects Hold recommendation. | US-25 | FR-24 | Positive | Hold recommendation is saved. |

---

## 4.9 Hiring Manager Dashboard and Decision

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-070 | Pipeline Dashboard | Hiring manager views candidate count by status. | US-27 | FR-26 | Positive | Number of candidates by status is displayed. |
| TC-071 | Pipeline Dashboard | Hiring manager views candidates grouped by internship program. | US-27 | FR-26 | Positive | Candidates are grouped by program. |
| TC-072 | Pipeline Dashboard | Unauthorized user accesses pipeline dashboard. | US-27 | FR-26, NFR-03 | Permission | System denies access. |
| TC-073 | Candidate Feedback | Hiring manager views submitted interview feedback. | US-28 | FR-27 | Positive | Candidate feedback is displayed. |
| TC-074 | Candidate Feedback | Hiring manager opens candidate detail with no submitted feedback. | US-28 | FR-27 | Negative | System shows feedback is not available yet. |
| TC-075 | Candidate Comparison | Hiring manager compares at least two candidates. | US-29 | FR-28 | Positive | Candidate comparison is displayed side by side. |
| TC-076 | Candidate Comparison | Hiring manager compares fewer than two candidates. | US-29 | FR-28 | Validation | System asks user to select at least two candidates. |
| TC-077 | Final Decision | Hiring manager approves final offer decision. | US-30 | FR-29 | Positive | Approval is recorded successfully. |
| TC-078 | Final Decision | Non-hiring-manager tries to approve final decision. | US-30 | FR-29, NFR-03 | Permission | System denies access. |

---

## 4.10 Admin and Access Control

| Test ID | Module | Scenario | Related User Story | Related Requirement | Test Type | Expected Result |
|---|---|---|---|---|---|---|
| TC-079 | User Management | Admin creates a new user account with valid information. | US-31 | FR-30 | Positive | User account is created successfully. |
| TC-080 | User Management | Admin updates user information. | US-31 | FR-30 | Positive | Updated user information is saved. |
| TC-081 | User Management | Admin deactivates user account. | US-31 | FR-30 | Positive | User can no longer log in. |
| TC-082 | User Management | Non-admin user tries to manage user accounts. | US-31 | FR-30, NFR-03 | Permission | System denies access. |
| TC-083 | Role Management | Admin assigns a role to a user. | US-32 | FR-31 | Positive | User receives permissions of assigned role. |
| TC-084 | Role Management | Admin changes a user's role. | US-32 | FR-31 | Positive | User permissions are updated based on new role. |
| TC-085 | Role Management | Non-admin user tries to assign roles. | US-32 | FR-31, NFR-03 | Permission | System denies access. |
| TC-086 | Program Management | Admin creates an internship program with valid information. | US-33 | FR-32 | Positive | Internship program is created successfully. |
| TC-087 | Program Management | Admin updates an internship program. | US-33 | FR-32 | Positive | Program information is updated successfully. |
| TC-088 | Program Management | Candidate applies to a closed internship program. | US-33 | FR-32 | Business Rule | System prevents application submission. |
| TC-089 | Activity Log | Admin views activity log page. | US-34 | FR-33 | Positive | Important system actions are displayed. |
| TC-090 | Activity Log | HR updates candidate status. | US-34 | FR-33, NFR-06 | Positive | Status update action is recorded in activity log. |
| TC-091 | Activity Log | Non-admin user tries to access activity log. | US-34 | FR-33, NFR-03 | Permission | System denies access. |

---

## 5. High-Priority Test Scenarios for MVP

The following test scenarios should be tested first because they cover the core MVP workflow.

| Priority | Test ID | Reason |
|---|---|---|
| High | TC-001 | Candidate registration is required before application. |
| High | TC-004 | Login is required for all protected features. |
| High | TC-011 | CV upload is required for application submission. |
| High | TC-016 | Application submission is the core candidate workflow. |
| High | TC-023 | Candidate status tracking is a key business goal. |
| High | TC-029 | HR must manage all submitted applications. |
| High | TC-040 | HR status update is a core recruitment workflow. |
| High | TC-045 | Status history is required for traceability. |
| High | TC-049 | Interview scheduling is required for interview workflow. |
| High | TC-057 | Interviewer must view assigned interviews. |
| High | TC-062 | Structured feedback is required for hiring decision. |
| High | TC-079 | Admin user creation supports access control. |
| High | TC-083 | Role assignment supports permission control. |

## 6. End-to-End Test Flow

This flow checks whether the main recruitment workflow works from start to finish.

| Step | Actor | Action | Expected Result |
|---|---|---|---|
| 1 | Candidate | Register account | Candidate account is created. |
| 2 | Candidate | Complete profile and upload CV | Profile and CV are saved. |
| 3 | Candidate | Submit internship application | Application status becomes Submitted. |
| 4 | HR Recruiter | View submitted application | Candidate appears in candidate management list. |
| 5 | HR Recruiter | Update status to Screening | Candidate status is updated and recorded. |
| 6 | HR Recruiter | Schedule interview and assign interviewer | Interview is created and candidate status becomes Interview Scheduled. |
| 7 | Interviewer | View assigned interview | Interview appears in interviewer dashboard. |
| 8 | Interviewer | Submit structured feedback | Feedback is saved successfully. |
| 9 | Hiring Manager | View pipeline and feedback | Candidate feedback is visible. |
| 10 | Hiring Manager | Approve final decision | Decision approval is saved. |
| 11 | HR Recruiter | Send final result | Candidate receives final result notification. |
| 12 | Candidate | View final status | Final status is displayed correctly. |

## 7. Test Scenario Quality Checklist

| Checklist Item | Description |
|---|---|
| Linked to requirement | Each test scenario maps to user story and functional requirement. |
| Clear expected result | Each scenario has a clear expected system behavior. |
| Covers positive cases | Normal successful flows are included. |
| Covers negative cases | Invalid actions and failure cases are included. |
| Covers validation rules | Required fields, file type, file size, and duplicate rules are included. |
| Covers permission rules | Access control and role-based restrictions are included. |
| Covers business rules | Status transitions, closed program, and final decision rules are included. |
| Supports MVP testing | High-priority test scenarios are identified. |

## 8. BA Notes

Test scenarios are important because they help confirm that requirements are testable.

In a real project, the BA works with QA to ensure that each business requirement, functional requirement, user story, and acceptance criterion can be verified through testing.

The next step is to create a Requirement Traceability Matrix to connect business requirements, functional requirements, user stories, acceptance criteria, and test scenarios.
