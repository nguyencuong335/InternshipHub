# 08. Wireframe Specification

## 1. Purpose

This document describes the main screen wireframes for the InternshipHub system.

The goal of this wireframe specification is to help stakeholders, developers, and QA engineers understand the layout, main components, user actions, and business rules of each important screen.

This document focuses on low-fidelity wireframes and functional screen behavior, not final UI design.

## 2. Wireframe Scope

The wireframe specification covers the following screens:

| Screen ID | Screen Name | Main User |
|---|---|---|
| WF-01 | Candidate Registration Page | Candidate |
| WF-02 | Candidate Login Page | Candidate, HR, Interviewer, Hiring Manager, Admin |
| WF-03 | Candidate Profile Page | Candidate |
| WF-04 | Internship Application Page | Candidate |
| WF-05 | Candidate Application Status Page | Candidate |
| WF-06 | HR Candidate Management Page | HR Recruiter |
| WF-07 | Candidate Detail Page | HR Recruiter |
| WF-08 | Interview Scheduling Page | HR Recruiter |
| WF-09 | Interviewer Dashboard | Interviewer |
| WF-10 | Interview Feedback Form | Interviewer |
| WF-11 | Hiring Manager Pipeline Dashboard | Hiring Manager |
| WF-12 | Admin User Management Page | System Admin |

---

## WF-01: Candidate Registration Page

### Purpose

Allow a new candidate to create an account in the InternshipHub system.

### User Role

Candidate

### Main Components

| Component | Description |
|---|---|
| Full Name Input | Candidate enters full name. |
| Email Input | Candidate enters email address. |
| Password Input | Candidate enters password. |
| Confirm Password Input | Candidate confirms password. |
| Register Button | Candidate submits registration form. |
| Login Link | Candidate navigates to login page if they already have an account. |
| Validation Message Area | System shows errors or success messages. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| InternshipHub - Candidate Registration             |
+---------------------------------------------------+
| Full Name:        [________________________]       |
| Email:            [________________________]       |
| Password:         [________________________]       |
| Confirm Password: [________________________]       |
|                                                   |
| [ Register ]                                      |
|                                                   |
| Already have an account? Login                    |
|                                                   |
| Validation messages appear here                   |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF01-R01 | Full name, email, password, and confirm password are required. |
| WF01-R02 | Email must follow valid email format. |
| WF01-R03 | Email must be unique. |
| WF01-R04 | Password and confirm password must match. |

### Related User Stories

US-01

---

## WF-02: Login Page

### Purpose

Allow users to log in to the system based on their role.

### User Role

Candidate, HR Recruiter, Interviewer, Hiring Manager, System Admin

### Main Components

| Component | Description |
|---|---|
| Email Input | User enters email. |
| Password Input | User enters password. |
| Login Button | User submits login form. |
| Error Message Area | System shows invalid login message. |
| Register Link | Candidate can go to registration page. |

### Low-Fidelity Layout

```text
+------------------------------------------+
| InternshipHub - Login                    |
+------------------------------------------+
| Email:    [________________________]     |
| Password: [________________________]     |
|                                          |
| [ Login ]                                |
|                                          |
| New candidate? Register                  |
|                                          |
| Error messages appear here               |
+------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF02-R01 | Email and password are required. |
| WF02-R02 | User is redirected based on their role after successful login. |
| WF02-R03 | Invalid login must show a clear error message. |
| WF02-R04 | Deactivated users cannot log in. |

### Related User Stories

US-02

---

## WF-03: Candidate Profile Page

### Purpose

Allow candidates to create and update their profile information.

### User Role

Candidate

### Main Components

| Component | Description |
|---|---|
| Full Name Input | Candidate full name. |
| Phone Number Input | Candidate phone number. |
| University Input | Candidate university. |
| Major Input | Candidate major. |
| Graduation Year Input | Candidate expected graduation year. |
| Portfolio Link Input | GitHub, LinkedIn, or personal website. |
| Save Button | Saves profile information. |
| Validation Message Area | Shows missing or invalid information. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| Candidate Profile                                 |
+---------------------------------------------------+
| Full Name:       [________________________]        |
| Phone Number:    [________________________]        |
| University:      [________________________]        |
| Major:           [________________________]        |
| Graduation Year: [________________________]        |
| Portfolio Link:  [________________________]        |
|                                                   |
| [ Save Profile ]                                  |
|                                                   |
| Validation messages appear here                   |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF03-R01 | Full name, phone number, university, and major are required. |
| WF03-R02 | Candidate can update profile before submitting an application. |
| WF03-R03 | Candidate can only edit their own profile. |

### Related User Stories

US-03

---

## WF-04: Internship Application Page

### Purpose

Allow candidates to upload CV and apply for an available internship program.

### User Role

Candidate

### Main Components

| Component | Description |
|---|---|
| Internship Program Dropdown | Candidate selects available internship program. |
| CV Upload Field | Candidate uploads PDF or DOCX CV. |
| CV File Name Display | Shows uploaded CV file name. |
| Submit Application Button | Candidate submits application. |
| Validation Message Area | Shows missing fields or upload errors. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| Internship Application                            |
+---------------------------------------------------+
| Internship Program: [ Select Program v ]          |
|                                                   |
| Upload CV: [ Choose File ]                        |
| Uploaded File: my_cv.pdf                          |
|                                                   |
| [ Submit Application ]                            |
|                                                   |
| Validation messages appear here                   |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF04-R01 | Candidate must select an available internship program. |
| WF04-R02 | Candidate must upload a CV before submitting application. |
| WF04-R03 | CV file must be PDF or DOCX. |
| WF04-R04 | CV file size must not exceed 5MB. |
| WF04-R05 | Candidate cannot apply to the same program more than once. |

### Related User Stories

US-04, US-05, US-06

---

## WF-05: Candidate Application Status Page

### Purpose

Allow candidates to view their current application status and interview information.

### User Role

Candidate

### Main Components

| Component | Description |
|---|---|
| Current Status Badge | Shows current application status. |
| Status Timeline | Shows recruitment progress. |
| Program Name | Shows applied internship program. |
| Submitted Date | Shows application submission date. |
| Interview Information Section | Shows interview date, time, interviewer, and meeting link if available. |
| Final Result Section | Shows offer, rejection, or hold result if available. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| Application Status                                |
+---------------------------------------------------+
| Program: Business Analyst Intern                  |
| Submitted Date: 2026-06-16                        |
| Current Status: [ Interview Scheduled ]           |
|                                                   |
| Timeline:                                         |
| Submitted -> Screening -> Interview Scheduled     |
|                                                   |
| Interview Information                             |
| Date: 2026-06-20                                  |
| Time: 09:00 AM                                    |
| Interviewer: Nguyen Van A                         |
| Meeting Link: [ Open Link ]                       |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF05-R01 | Candidate can only view their own application status. |
| WF05-R02 | Interview information is shown only when interview is scheduled. |
| WF05-R03 | Latest status must match the status managed by HR. |

### Related User Stories

US-07, US-08, US-09

---

## WF-06: HR Candidate Management Page

### Purpose

Allow HR recruiters to view, search, filter, and manage submitted applications.

### User Role

HR Recruiter

### Main Components

| Component | Description |
|---|---|
| Search Box | Search candidate by name or email. |
| Status Filter | Filter candidates by status. |
| Program Filter | Filter candidates by internship program. |
| Applied Date Filter | Filter by application date. |
| Candidate Table | Displays candidate list. |
| View Detail Button | Opens candidate detail page. |
| Update Status Action | Allows HR to update candidate status. |
| Schedule Interview Action | Opens interview scheduling page. |

### Low-Fidelity Layout

```text
+--------------------------------------------------------------------------------+
| HR Candidate Management                                                        |
+--------------------------------------------------------------------------------+
| Search: [________________]  Status: [All v]  Program: [All v]  Date: [____]     |
+--------------------------------------------------------------------------------+
| Candidate Name | Email | Program | Status | Applied Date | Actions             |
|--------------------------------------------------------------------------------|
| Nguyen A       | a@... | BA Intern | Screening | 2026-06-15 | View / Update      |
| Tran B         | b@... | AI Intern | Submitted | 2026-06-16 | View / Update      |
+--------------------------------------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF06-R01 | Only HR Recruiter, Hiring Manager, and Admin can view candidate list. |
| WF06-R02 | Only HR Recruiter can update candidate status. |
| WF06-R03 | Search and filters can be used together. |
| WF06-R04 | Candidate list should show the latest status. |

### Related User Stories

US-10, US-11, US-12

---

## WF-07: Candidate Detail Page

### Purpose

Allow HR to review candidate profile, CV, status history, and feedback.

### User Role

HR Recruiter

### Main Components

| Component | Description |
|---|---|
| Candidate Profile Section | Shows candidate personal information. |
| CV Section | Allows HR to view or download CV. |
| Application Information Section | Shows program, status, applied date. |
| Status Update Section | Allows HR to update candidate status. |
| Status History Table | Shows status changes. |
| Interview Feedback Section | Shows submitted feedback if available. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| Candidate Detail                                  |
+---------------------------------------------------+
| Name: Nguyen Van A                                |
| Email: nguyenvana@email.com                       |
| University: UIT                                   |
| Major: Information Technology                     |
| Program: BA Intern                                |
| Current Status: Screening                         |
|                                                   |
| CV: [ View CV ] [ Download CV ]                   |
|                                                   |
| Update Status: [ Select Status v ] [ Save ]       |
|                                                   |
| Status History                                    |
| Old Status | New Status | Updated By | Time       |
|                                                   |
| Interview Feedback                                |
| Feedback will appear here after interview         |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF07-R01 | HR can view candidate profile and CV. |
| WF07-R02 | HR can update candidate status only through allowed transitions. |
| WF07-R03 | Every status change must be saved in status history. |
| WF07-R04 | Feedback is visible after interviewer submits it. |

### Related User Stories

US-13, US-14, US-15, US-16

---

## WF-08: Interview Scheduling Page

### Purpose

Allow HR to schedule interviews and assign interviewers.

### User Role

HR Recruiter

### Main Components

| Component | Description |
|---|---|
| Candidate Information | Shows selected candidate information. |
| Interviewer Dropdown | HR selects interviewer. |
| Interview Date Picker | HR selects interview date. |
| Interview Time Picker | HR selects interview time. |
| Meeting Link Input | HR enters online meeting link or location. |
| Save Schedule Button | Creates interview schedule. |
| Validation Message Area | Shows required field or invalid status messages. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| Schedule Interview                                |
+---------------------------------------------------+
| Candidate: Nguyen Van A                           |
| Program: BA Intern                                |
| Current Status: Screening                         |
|                                                   |
| Interviewer: [ Select Interviewer v ]             |
| Date:        [ YYYY-MM-DD ]                       |
| Time:        [ HH:MM ]                            |
| Meeting:     [________________________]           |
|                                                   |
| [ Save Schedule ]                                 |
|                                                   |
| Validation messages appear here                   |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF08-R01 | HR can schedule interview only for candidates in Screening status. |
| WF08-R02 | Interviewer, date, time, and meeting information are required. |
| WF08-R03 | After scheduling, candidate status becomes Interview Scheduled. |
| WF08-R04 | Assigned interviewer can view the interview details. |

### Related User Stories

US-18, US-19, US-20

---

## WF-09: Interviewer Dashboard

### Purpose

Allow interviewers to view their assigned interviews.

### User Role

Interviewer

### Main Components

| Component | Description |
|---|---|
| Assigned Interview List | Shows interviews assigned to the interviewer. |
| Candidate Name | Shows candidate name. |
| Program Name | Shows internship program. |
| Interview Date and Time | Shows schedule. |
| Meeting Information | Shows meeting link or location. |
| Open Feedback Button | Opens feedback form. |

### Low-Fidelity Layout

```text
+--------------------------------------------------------------------------------+
| Interviewer Dashboard                                                          |
+--------------------------------------------------------------------------------+
| Candidate Name | Program | Date | Time | Meeting | Action                      |
|--------------------------------------------------------------------------------|
| Nguyen A       | BA Intern | 2026-06-20 | 09:00 | Meet Link | Open Feedback  |
| Tran B         | AI Intern | 2026-06-21 | 14:00 | Meet Link | Open Feedback  |
+--------------------------------------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF09-R01 | Interviewer can only view assigned interviews. |
| WF09-R02 | Interviewer can only view candidate profile and CV for assigned interviews. |
| WF09-R03 | Interviewer can open feedback form for assigned interviews. |

### Related User Stories

US-21, US-22, US-26

---

## WF-10: Interview Feedback Form

### Purpose

Allow interviewers to submit structured feedback after interviews.

### User Role

Interviewer

### Main Components

| Component | Description |
|---|---|
| Candidate Summary | Shows candidate and program information. |
| Technical Rating Field | Interviewer rates technical ability. |
| Communication Rating Field | Interviewer rates communication. |
| Strengths Field | Interviewer enters candidate strengths. |
| Weaknesses Field | Interviewer enters candidate weaknesses. |
| Recommendation Dropdown | Pass, Fail, or Hold. |
| Comment Field | Optional additional notes. |
| Submit Feedback Button | Saves feedback. |

### Low-Fidelity Layout

```text
+---------------------------------------------------+
| Interview Feedback Form                           |
+---------------------------------------------------+
| Candidate: Nguyen Van A                           |
| Program: BA Intern                                |
|                                                   |
| Technical Rating:     [ 1 2 3 4 5 ]               |
| Communication Rating: [ 1 2 3 4 5 ]               |
|                                                   |
| Strengths:                                        |
| [_____________________________________________]   |
|                                                   |
| Weaknesses:                                       |
| [_____________________________________________]   |
|                                                   |
| Recommendation: [ Pass / Fail / Hold v ]          |
| Comments:                                         |
| [_____________________________________________]   |
|                                                   |
| [ Submit Feedback ]                               |
+---------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF10-R01 | Only assigned interviewer can submit feedback. |
| WF10-R02 | Technical rating, communication rating, strengths, weaknesses, and recommendation are required. |
| WF10-R03 | Recommendation must be Pass, Fail, or Hold. |
| WF10-R04 | Submitted feedback becomes visible to HR and Hiring Manager. |

### Related User Stories

US-23, US-24, US-25

---

## WF-11: Hiring Manager Pipeline Dashboard

### Purpose

Allow hiring managers to view recruitment progress and candidate feedback.

### User Role

Hiring Manager

### Main Components

| Component | Description |
|---|---|
| Candidate Count by Status | Shows number of candidates in each stage. |
| Program Filter | Filter by internship program. |
| Candidate Pipeline Table | Shows candidates and their current status. |
| Feedback Summary | Shows interviewer recommendation. |
| Compare Candidates Action | Allows candidate comparison. |
| Approve Decision Action | Allows approval of final hiring decision. |

### Low-Fidelity Layout

```text
+--------------------------------------------------------------------------------+
| Hiring Manager Pipeline Dashboard                                              |
+--------------------------------------------------------------------------------+
| Program: [ All Programs v ]                                                     |
|                                                                                |
| Submitted: 20 | Screening: 12 | Interview: 8 | Offered: 3 | Rejected: 5         |
+--------------------------------------------------------------------------------+
| Candidate | Program | Status | Rating | Recommendation | Action                |
|--------------------------------------------------------------------------------|
| Nguyen A  | BA Intern | Interview Completed | 4.5 | Pass | View / Approve       |
| Tran B    | AI Intern | Hold                | 3.8 | Hold | View / Compare       |
+--------------------------------------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF11-R01 | Hiring Manager can view pipeline and feedback. |
| WF11-R02 | Hiring Manager cannot directly edit candidate profile. |
| WF11-R03 | Candidate comparison requires at least two selected candidates. |
| WF11-R04 | Final offer should be approved before HR sends offer notification. |

### Related User Stories

US-27, US-28, US-29, US-30

---

## WF-12: Admin User Management Page

### Purpose

Allow system admin to manage user accounts and roles.

### User Role

System Admin

### Main Components

| Component | Description |
|---|---|
| User List | Shows all system users. |
| Search Box | Search user by name or email. |
| Role Filter | Filter users by role. |
| Create User Button | Opens create user form. |
| Edit User Action | Updates user information. |
| Deactivate User Action | Deactivates user account. |
| Role Assignment Action | Assigns or changes user role. |

### Low-Fidelity Layout

```text
+--------------------------------------------------------------------------------+
| Admin User Management                                                          |
+--------------------------------------------------------------------------------+
| Search: [________________]  Role: [ All Roles v ]  [ Create User ]              |
+--------------------------------------------------------------------------------+
| Name | Email | Role | Status | Actions                                          |
|--------------------------------------------------------------------------------|
| HR A | hra@company.com | HR Recruiter | Active | Edit / Change Role / Deactivate |
| B    | b@company.com   | Interviewer  | Active | Edit / Change Role / Deactivate |
+--------------------------------------------------------------------------------+
```

### Business Rules

| Rule ID | Rule |
|---|---|
| WF12-R01 | Only System Admin can manage users and roles. |
| WF12-R02 | Deactivated users cannot log in. |
| WF12-R03 | Each user must have at least one role. |
| WF12-R04 | Role changes must update user permissions. |

### Related User Stories

US-31, US-32, US-33, US-34

---

## 3. Wireframe Review Checklist

| Checklist Item | Description |
|---|---|
| Clear screen purpose | Each screen has a clear goal. |
| Clear user role | Each screen identifies who uses it. |
| Required fields included | Important fields are listed. |
| Main actions included | Buttons and user actions are defined. |
| Business rules included | Rules and restrictions are documented. |
| Related user stories linked | Each screen maps to user stories. |
| Permission rules considered | Sensitive screens include access rules. |

## 4. BA Notes

Wireframe specification helps the BA communicate expected screen behavior before development starts.

For a BA Intern or Fresher role, the wireframe does not need to be visually perfect. The important point is to show that the BA understands user flow, required data, business rules, and screen-level behavior.

The next step is to create test scenarios from user stories, acceptance criteria, and business rules.
