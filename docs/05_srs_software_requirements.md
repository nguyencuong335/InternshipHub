# 05. Software Requirements Specification

## 1. Purpose

This document describes the software requirements for the InternshipHub system.

The purpose of this SRS is to convert business requirements into clear functional requirements, non-functional requirements, user roles, validation rules, and system behavior.

This document helps developers understand what to build and helps QA engineers understand what to test.

## 2. Product Scope

InternshipHub is a web-based internship recruitment management system.

The system supports candidates, HR recruiters, interviewers, hiring managers, and system admins in managing the internship application process from application submission to final hiring decision.

## 3. User Roles

| Role | Description |
|---|---|
| Candidate | A user who applies for internship programs and tracks application status. |
| HR Recruiter | A user who manages applications, screens candidates, schedules interviews, and updates candidate status. |
| Interviewer | A user who reviews assigned candidates and submits interview feedback. |
| Hiring Manager | A user who reviews candidate pipeline and approves final hiring decisions. |
| System Admin | A user who manages system users, roles, permissions, and internship programs. |

## 4. Functional Requirements

### 4.1 Candidate Module

| Requirement ID | Functional Requirement | Priority |
|---|---|---|
| FR-01 | The system shall allow candidates to register an account using email and password. | Must |
| FR-02 | The system shall allow candidates to log in and log out. | Must |
| FR-03 | The system shall allow candidates to create and update their personal profile. | Must |
| FR-04 | The system shall allow candidates to upload a CV file. | Must |
| FR-05 | The system shall validate CV file type and file size. | Must |
| FR-06 | The system shall allow candidates to apply for an available internship program. | Must |
| FR-07 | The system shall allow candidates to view their submitted application. | Must |
| FR-08 | The system shall allow candidates to view their current application status. | Must |
| FR-09 | The system shall notify candidates when their application status changes. | Should |

### 4.2 HR Recruiter Module

| Requirement ID | Functional Requirement | Priority |
|---|---|---|
| FR-10 | The system shall allow HR recruiters to view all submitted applications. | Must |
| FR-11 | The system shall allow HR recruiters to search candidates by name, email, or internship program. | Must |
| FR-12 | The system shall allow HR recruiters to filter candidates by status, program, and applied date. | Must |
| FR-13 | The system shall allow HR recruiters to view candidate profile and CV. | Must |
| FR-14 | The system shall allow HR recruiters to update candidate recruitment status. | Must |
| FR-15 | The system shall validate candidate status transitions. | Must |
| FR-16 | The system shall record every candidate status change. | Must |
| FR-17 | The system shall allow HR recruiters to schedule interviews. | Must |
| FR-18 | The system shall allow HR recruiters to assign interviewers to candidates. | Must |
| FR-19 | The system shall allow HR recruiters to send offer or rejection results. | Should |

### 4.3 Interviewer Module

| Requirement ID | Functional Requirement | Priority |
|---|---|---|
| FR-20 | The system shall allow interviewers to view their assigned interviews. | Must |
| FR-21 | The system shall allow interviewers to view assigned candidate profile and CV. | Must |
| FR-22 | The system shall allow interviewers to submit structured interview feedback. | Must |
| FR-23 | The system shall require interviewers to provide rating, comments, and recommendation. | Must |
| FR-24 | The system shall allow interviewers to recommend Pass, Fail, or Hold. | Must |
| FR-25 | The system shall prevent interviewers from viewing candidates not assigned to them. | Must |

### 4.4 Hiring Manager Module

| Requirement ID | Functional Requirement | Priority |
|---|---|---|
| FR-26 | The system shall allow hiring managers to view the recruitment pipeline. | Should |
| FR-27 | The system shall allow hiring managers to view candidate feedback. | Should |
| FR-28 | The system shall allow hiring managers to compare candidates by status, rating, and feedback. | Could |
| FR-29 | The system shall allow hiring managers to approve final hiring decisions. | Should |

### 4.5 Admin Module

| Requirement ID | Functional Requirement | Priority |
|---|---|---|
| FR-30 | The system shall allow admins to create, update, and deactivate user accounts. | Must |
| FR-31 | The system shall allow admins to assign user roles. | Must |
| FR-32 | The system shall allow admins to create and update internship programs. | Should |
| FR-33 | The system shall allow admins to view system activity logs. | Should |

## 5. Non-Functional Requirements

| Requirement ID | Non-Functional Requirement | Category | Priority |
|---|---|---|---|
| NFR-01 | The system should load the candidate list within 3 seconds for up to 1,000 records. | Performance | Should |
| NFR-02 | The system shall require authentication before users access protected pages. | Security | Must |
| NFR-03 | The system shall restrict data access based on user roles. | Security | Must |
| NFR-04 | Candidate can only view their own application information. | Security | Must |
| NFR-05 | Interviewer can only view candidates assigned to them. | Security | Must |
| NFR-06 | The system shall record important actions such as status updates, interview scheduling, and feedback submission. | Auditability | Must |
| NFR-07 | The system should be available 99% during recruitment periods. | Availability | Should |
| NFR-08 | The system UI should work on desktop and mobile browsers. | Usability | Should |
| NFR-09 | CV upload should support PDF and DOCX files. | Compatibility | Must |
| NFR-10 | The system should show clear validation messages when user input is invalid. | Usability | Must |

## 6. Data Requirements

### 6.1 Candidate Profile Data

| Field | Required | Description |
|---|---|---|
| Full Name | Yes | Candidate full name |
| Email | Yes | Candidate email address |
| Phone Number | Yes | Candidate contact number |
| University | Yes | Candidate university |
| Major | Yes | Candidate major |
| Graduation Year | No | Expected graduation year |
| CV File | Yes | Candidate CV file |
| Portfolio Link | No | GitHub, LinkedIn, or personal website |
| Applied Program | Yes | Internship program selected by candidate |

### 6.2 Application Data

| Field | Required | Description |
|---|---|---|
| Application ID | Yes | Unique application identifier |
| Candidate ID | Yes | Candidate linked to the application |
| Program ID | Yes | Internship program |
| Application Status | Yes | Current recruitment status |
| Applied Date | Yes | Date when candidate submitted application |
| Last Updated Date | Yes | Last status update time |
| Updated By | Yes | User who updated the application |

### 6.3 Interview Feedback Data

| Field | Required | Description |
|---|---|---|
| Interview ID | Yes | Unique interview identifier |
| Candidate ID | Yes | Candidate being interviewed |
| Interviewer ID | Yes | Assigned interviewer |
| Technical Rating | Yes | Technical evaluation score |
| Communication Rating | Yes | Communication evaluation score |
| Strengths | Yes | Candidate strengths |
| Weaknesses | Yes | Candidate weaknesses |
| Recommendation | Yes | Pass, Fail, or Hold |
| Comments | No | Additional interviewer comments |

## 7. Candidate Status Flow

The system shall support the following candidate status flow:

```text
Draft → Submitted → Screening → Interview Scheduled → Interview Completed → Offered
                                                               ↘ Rejected
                                                               ↘ Hold
```

## 8. Status Transition Rules

| Current Status | Allowed Next Status |
|---|---|
| Draft | Submitted |
| Submitted | Screening, Rejected |
| Screening | Interview Scheduled, Rejected |
| Interview Scheduled | Interview Completed, Rejected |
| Interview Completed | Offered, Rejected, Hold |
| Hold | Offered, Rejected |
| Offered | No next status |
| Rejected | No next status by default |

## 9. Permission Matrix

| Feature | Candidate | HR Recruiter | Interviewer | Hiring Manager | Admin |
|---|---|---|---|---|---|
| Submit application | Yes | No | No | No | No |
| View own status | Yes | No | No | No | No |
| View all candidates | No | Yes | No | Yes | Yes |
| Update candidate status | No | Yes | No | No | No |
| Schedule interview | No | Yes | No | No | No |
| View assigned interview | No | No | Yes | No | No |
| Submit interview feedback | No | No | Yes | No | No |
| View pipeline dashboard | No | Yes | No | Yes | Yes |
| Manage users and roles | No | No | No | No | Yes |
| Configure internship programs | No | No | No | No | Yes |

## 10. Validation Rules

| Rule ID | Validation Rule |
|---|---|
| VR-01 | Candidate full name must not be empty. |
| VR-02 | Candidate email must follow a valid email format. |
| VR-03 | Candidate phone number must not be empty. |
| VR-04 | CV file is required before application submission. |
| VR-05 | CV file must be PDF or DOCX. |
| VR-06 | CV file size must not exceed 5MB. |
| VR-07 | Candidate cannot apply to the same internship program more than once. |
| VR-08 | HR cannot schedule an interview without selecting candidate, interviewer, date, and time. |
| VR-09 | Interviewer cannot submit feedback without rating and recommendation. |
| VR-10 | System must reject unauthorized access based on user role. |

## 11. Error Handling

| Error Case | System Behavior |
|---|---|
| User submits incomplete form | System shows required field validation messages. |
| User uploads unsupported CV file type | System rejects the file and shows allowed file types. |
| Candidate tries to access another candidate's application | System denies access. |
| Interviewer tries to view unassigned candidate | System denies access. |
| HR selects invalid status transition | System prevents update and shows error message. |
| Interview feedback is missing required fields | System prevents submission and shows validation messages. |

## 12. Open Questions

| Question ID | Open Question |
|---|---|
| OQ-01 | Should candidates be allowed to edit submitted applications? |
| OQ-02 | Should HR be able to export candidate data to Excel? |
| OQ-03 | Should the system support multiple interview rounds? |
| OQ-04 | Should candidates receive email only, or both email and in-system notification? |
| OQ-05 | Should hiring managers approve every offer, or only selected programs? |

## 13. BA Notes

This SRS converts business requirements into detailed software requirements.

The most important parts for development and testing are functional requirements, non-functional requirements, permission matrix, validation rules, status transition rules, and error handling.