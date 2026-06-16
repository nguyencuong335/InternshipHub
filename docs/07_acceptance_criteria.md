# 07. Acceptance Criteria

## 1. Purpose

This document defines acceptance criteria for the key user stories in the InternshipHub system.

Acceptance criteria help the Business Analyst, Developer, QA Engineer, and stakeholder agree on what “done correctly” means for each user story.

## 2. Acceptance Criteria Format

The acceptance criteria in this document use the Given–When–Then format.

```text
Given [initial condition]
When [user action or system event]
Then [expected result]
```

This format makes requirements easier to understand, develop, and test.

## 3. Acceptance Criteria List

---

## US-01: Candidate Registration

**User Story**

As a candidate, I want to register an account using email and password, so that I can access the InternshipHub system.

**Acceptance Criteria**

```gherkin
Given I am on the registration page
When I enter a valid email, password, and required information
Then the system creates my candidate account successfully
```

```gherkin
Given I am on the registration page
When I enter an email that already exists
Then the system shows an error message that the email is already registered
```

```gherkin
Given I am on the registration page
When I leave required fields empty
Then the system shows validation messages for the missing fields
```

---

## US-02: Candidate Login and Logout

**User Story**

As a candidate, I want to log in and log out, so that I can securely use my account.

**Acceptance Criteria**

```gherkin
Given I have a registered account
When I enter the correct email and password
Then the system logs me in and redirects me to the candidate dashboard
```

```gherkin
Given I am on the login page
When I enter an incorrect email or password
Then the system shows an invalid login message
```

```gherkin
Given I am logged in
When I click the logout button
Then the system logs me out and redirects me to the login page
```

---

## US-03: Create and Update Personal Profile

**User Story**

As a candidate, I want to create and update my personal profile, so that HR can review my information.

**Acceptance Criteria**

```gherkin
Given I am logged in as a candidate
When I enter all required profile information
Then the system saves my profile successfully
```

```gherkin
Given I am logged in as a candidate
When I leave required profile fields empty
Then the system shows validation messages for the missing fields
```

```gherkin
Given I already have a saved profile
When I update valid profile information
Then the system saves the updated information successfully
```

---

## US-04: Upload CV

**User Story**

As a candidate, I want to upload my CV, so that HR can evaluate my application.

**Acceptance Criteria**

```gherkin
Given I am logged in as a candidate
When I upload a PDF or DOCX file under 5MB
Then the system saves the CV and shows an upload success message
```

```gherkin
Given I am logged in as a candidate
When I upload a file that is not PDF or DOCX
Then the system rejects the file and shows the allowed file types
```

```gherkin
Given I am logged in as a candidate
When I upload a CV file larger than 5MB
Then the system rejects the file and shows the maximum file size limit
```

```gherkin
Given I already uploaded a CV before submitting my application
When I upload a new valid CV
Then the system replaces the old CV with the new CV
```

---

## US-05: Submit Application

**User Story**

As a candidate, I want to apply for an available internship program, so that I can be considered for the position.

**Acceptance Criteria**

```gherkin
Given I have completed my profile and uploaded a valid CV
When I select an available internship program and submit my application
Then the system creates a new application with status Submitted
```

```gherkin
Given I have not uploaded a CV
When I try to submit my application
Then the system prevents submission and shows a CV required message
```

```gherkin
Given I already applied to the same internship program
When I try to apply again
Then the system prevents duplicate application submission
```

```gherkin
Given the internship program is closed
When I try to submit an application
Then the system prevents submission and shows that the program is no longer available
```

---

## US-06: View Submitted Application

**User Story**

As a candidate, I want to view my submitted application, so that I can check the information I provided.

**Acceptance Criteria**

```gherkin
Given I have submitted an application
When I open the submitted application page
Then I can see the application information I provided
```

```gherkin
Given I am a candidate
When I try to view another candidate's submitted application
Then the system denies access
```

```gherkin
Given I have submitted an application
When I open the submitted application page
Then I can see the internship program, submitted date, profile information, and CV file name
```

---

## US-07: View Application Status

**User Story**

As a candidate, I want to view my current application status, so that I can know my recruitment progress.

**Acceptance Criteria**

```gherkin
Given I have submitted an application
When I open the application status page
Then I can see my current application status
```

```gherkin
Given I have submitted an application
When I open the application status page
Then I can see the internship program name and submitted date
```

```gherkin
Given I am a candidate
When I try to view another candidate's application status
Then the system denies access
```

```gherkin
Given my interview has been scheduled
When I open the application status page
Then I can see the interview date, time, and meeting information
```

---

## US-08: Receive Status Notification

**User Story**

As a candidate, I want to receive a notification when my application status changes, so that I do not need to contact HR manually.

**Acceptance Criteria**

```gherkin
Given my application status is updated by HR
When the status update is saved successfully
Then the system sends me a status notification
```

```gherkin
Given my email address is valid
When the system sends a status notification
Then I receive the notification through email
```

```gherkin
Given the notification cannot be sent
When the system detects the sending failure
Then the system records the failure for HR or admin review
```

---

## US-09: View Interview Information

**User Story**

As a candidate, I want to view interview information when my interview is scheduled, so that I can prepare on time.

**Acceptance Criteria**

```gherkin
Given my interview has been scheduled
When I open the application status page
Then I can see the interview date, time, interviewer name, and meeting information
```

```gherkin
Given my interview has not been scheduled
When I open the application status page
Then the system does not show interview details
```

```gherkin
Given HR updates my interview schedule
When the update is saved successfully
Then I can see the latest interview information
```

---

## US-10: View All Submitted Applications

**User Story**

As an HR recruiter, I want to view all submitted applications, so that I can manage candidates in one place.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I open the candidate management page
Then the system displays a list of submitted applications
```

```gherkin
Given I am logged in as an HR recruiter
When the candidate list is displayed
Then I can see candidate name, email, internship program, status, and applied date
```

```gherkin
Given I am not an HR recruiter, hiring manager, or admin
When I try to access the candidate management page
Then the system denies access
```

---

## US-11: Search Candidates

**User Story**

As an HR recruiter, I want to search candidates by name, email, or internship program, so that I can find candidates quickly.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I search by candidate name
Then the system displays candidates whose names match the search keyword
```

```gherkin
Given I am logged in as an HR recruiter
When I search by candidate email
Then the system displays candidates whose emails match the search keyword
```

```gherkin
Given I am logged in as an HR recruiter
When no candidate matches the search keyword
Then the system shows an empty result message
```

---

## US-12: Filter Candidates

**User Story**

As an HR recruiter, I want to filter candidates by status, program, and applied date, so that I can manage the recruitment pipeline efficiently.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I filter candidates by status
Then the system displays only candidates with the selected status
```

```gherkin
Given I am logged in as an HR recruiter
When I filter candidates by internship program
Then the system displays only candidates who applied to the selected program
```

```gherkin
Given I am logged in as an HR recruiter
When I combine status, program, and applied date filters
Then the system displays candidates that match all selected filters
```

---

## US-13: View Candidate Profile and CV

**User Story**

As an HR recruiter, I want to view candidate profile and CV, so that I can screen candidates properly.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I open a candidate detail page
Then I can see the candidate profile information
```

```gherkin
Given I am logged in as an HR recruiter
When I open a candidate detail page
Then I can view or download the candidate CV
```

```gherkin
Given I am not authorized to view candidate information
When I try to open a candidate detail page
Then the system denies access
```

---

## US-14: Update Candidate Status

**User Story**

As an HR recruiter, I want to update candidate recruitment status, so that the candidate pipeline stays accurate.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I update a candidate status from Submitted to Screening
Then the system saves the new status successfully
```

```gherkin
Given I am logged in as an HR recruiter
When I update a candidate status
Then the system records the old status, new status, updated by, and updated time
```

```gherkin
Given I am logged in as an HR recruiter
When I try to update a candidate using an invalid status transition
Then the system prevents the update and shows an error message
```

```gherkin
Given a candidate status is updated
When the update is saved successfully
Then the candidate can see the latest status on the status page
```

---

## US-15: Validate Status Transitions

**User Story**

As an HR recruiter, I want the system to validate status transitions, so that invalid recruitment status changes are prevented.

**Acceptance Criteria**

```gherkin
Given a candidate is in Submitted status
When HR updates the status to Screening
Then the system accepts the transition
```

```gherkin
Given a candidate is in Draft status
When HR tries to update the status to Offered
Then the system rejects the transition
```

```gherkin
Given a candidate is in Rejected status
When HR tries to update the status without approval
Then the system prevents the update
```

---

## US-16: Record Status Change History

**User Story**

As an HR recruiter, I want every status change to be recorded, so that the recruitment process can be tracked and audited.

**Acceptance Criteria**

```gherkin
Given HR updates a candidate status
When the update is saved successfully
Then the system records the old status, new status, updated by, and updated time
```

```gherkin
Given a candidate has status history
When HR opens the candidate detail page
Then HR can view the status history
```

```gherkin
Given a status update fails
When the update is not saved
Then the system does not create an incorrect status history record
```

---

## US-17: Send Offer or Rejection Results

**User Story**

As an HR recruiter, I want to send offer or rejection results, so that candidates receive official recruitment outcomes.

**Acceptance Criteria**

```gherkin
Given a candidate has completed the recruitment process
When HR sends an offer result
Then the system sends the offer notification to the candidate
```

```gherkin
Given a candidate has completed the recruitment process
When HR sends a rejection result
Then the system sends the rejection notification to the candidate
```

```gherkin
Given the result notification is sent successfully
When the candidate opens the application status page
Then the final result is shown correctly
```

---

## US-18: Schedule Interview

**User Story**

As an HR recruiter, I want to schedule interviews, so that selected candidates can move to the interview stage.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I select a candidate, interviewer, interview date, interview time, and meeting information
Then the system creates an interview schedule successfully
```

```gherkin
Given I am logged in as an HR recruiter
When I try to schedule an interview without selecting an interviewer
Then the system prevents scheduling and shows a required field message
```

```gherkin
Given the selected candidate is not in Screening status
When I try to schedule an interview
Then the system prevents scheduling and shows an invalid status message
```

```gherkin
Given an interview is scheduled successfully
When the schedule is created
Then the candidate status changes to Interview Scheduled
```

---

## US-19: Assign Interviewer

**User Story**

As an HR recruiter, I want to assign interviewers to candidates, so that each interview has a responsible evaluator.

**Acceptance Criteria**

```gherkin
Given I am logged in as an HR recruiter
When I assign an interviewer to a candidate interview
Then the interviewer can view the assigned interview in their dashboard
```

```gherkin
Given I am logged in as an HR recruiter
When I change the assigned interviewer
Then the old interviewer can no longer view the interview and the new interviewer can view it
```

```gherkin
Given I am not an HR recruiter
When I try to assign an interviewer
Then the system denies access
```

---

## US-20: Make Interview Details Visible to Interviewer

**User Story**

As an HR recruiter, I want interview details to be visible to assigned interviewers, so that interviewers can prepare before the interview.

**Acceptance Criteria**

```gherkin
Given HR has scheduled an interview and assigned an interviewer
When the interviewer opens their dashboard
Then the interviewer can see the interview details
```

```gherkin
Given an interviewer is not assigned to an interview
When the interviewer tries to open the interview detail
Then the system denies access
```

```gherkin
Given HR updates the interview details
When the assigned interviewer opens the dashboard
Then the interviewer can see the latest interview details
```

---

## US-21: View Assigned Interviews

**User Story**

As an interviewer, I want to view my assigned interviews, so that I know which candidates I need to interview.

**Acceptance Criteria**

```gherkin
Given I am logged in as an interviewer
When I open my interview dashboard
Then the system displays only interviews assigned to me
```

```gherkin
Given I am logged in as an interviewer
When I view an assigned interview
Then I can see candidate name, internship program, interview date, interview time, and meeting information
```

```gherkin
Given I am logged in as an interviewer
When I try to view an interview assigned to another interviewer
Then the system denies access
```

---

## US-22: View Assigned Candidate Profile and CV

**User Story**

As an interviewer, I want to view assigned candidate profile and CV, so that I can prepare for the interview.

**Acceptance Criteria**

```gherkin
Given I am assigned to interview a candidate
When I open the candidate interview detail
Then I can see the candidate profile summary
```

```gherkin
Given I am assigned to interview a candidate
When I open the candidate interview detail
Then I can view or download the candidate CV
```

```gherkin
Given I am not assigned to a candidate
When I try to view the candidate profile or CV
Then the system denies access
```

---

## US-23: Submit Structured Interview Feedback

**User Story**

As an interviewer, I want to submit structured interview feedback, so that HR and hiring manager can make better decisions.

**Acceptance Criteria**

```gherkin
Given I am the assigned interviewer
When I submit feedback with required ratings, strengths, weaknesses, and recommendation
Then the system saves the feedback successfully
```

```gherkin
Given I am the assigned interviewer
When I submit feedback without required rating or recommendation
Then the system prevents submission and shows validation messages
```

```gherkin
Given I am not assigned to the candidate interview
When I try to submit feedback
Then the system denies access
```

```gherkin
Given interview feedback is submitted successfully
When HR views the candidate detail page
Then HR can see the submitted feedback
```

---

## US-24: Provide Rating, Comments, and Recommendation

**User Story**

As an interviewer, I want to provide rating, comments, and recommendation, so that feedback is clear and useful.

**Acceptance Criteria**

```gherkin
Given I am filling in the feedback form
When I provide all required ratings and recommendation
Then the system allows me to submit the feedback
```

```gherkin
Given I am filling in the feedback form
When I leave required rating fields empty
Then the system shows validation messages
```

```gherkin
Given I am filling in the feedback form
When I add optional comments
Then the system saves the comments with the feedback
```

---

## US-25: Recommend Pass, Fail, or Hold

**User Story**

As an interviewer, I want to recommend Pass, Fail, or Hold, so that the next recruitment action is easier to decide.

**Acceptance Criteria**

```gherkin
Given I am submitting interview feedback
When I select Pass as the recommendation
Then the system saves Pass as the interviewer recommendation
```

```gherkin
Given I am submitting interview feedback
When I select Fail as the recommendation
Then the system saves Fail as the interviewer recommendation
```

```gherkin
Given I am submitting interview feedback
When I select Hold as the recommendation
Then the system saves Hold as the interviewer recommendation
```

```gherkin
Given I am submitting interview feedback
When I do not select any recommendation
Then the system prevents submission and shows a required recommendation message
```

---

## US-26: Access Only Assigned Candidates

**User Story**

As an interviewer, I want to access only candidates assigned to me, so that candidate information remains secure.

**Acceptance Criteria**

```gherkin
Given I am logged in as an interviewer
When I open my assigned candidate list
Then the system displays only candidates assigned to me
```

```gherkin
Given I am logged in as an interviewer
When I try to access a candidate not assigned to me
Then the system denies access
```

```gherkin
Given HR changes the assigned interviewer
When I am no longer assigned to the candidate
Then I can no longer access that candidate information
```

---

## US-27: View Recruitment Pipeline

**User Story**

As a hiring manager, I want to view the recruitment pipeline, so that I can monitor hiring progress.

**Acceptance Criteria**

```gherkin
Given I am logged in as a hiring manager
When I open the recruitment pipeline dashboard
Then I can see the number of candidates by status
```

```gherkin
Given I am logged in as a hiring manager
When I open the recruitment pipeline dashboard
Then I can see candidates grouped by internship program
```

```gherkin
Given I am not a hiring manager, HR recruiter, or admin
When I try to access the recruitment pipeline dashboard
Then the system denies access
```

---

## US-28: View Candidate Feedback

**User Story**

As a hiring manager, I want to view candidate feedback, so that I can understand interviewer evaluation.

**Acceptance Criteria**

```gherkin
Given I am logged in as a hiring manager
When I open a candidate detail page
Then I can see the submitted interview feedback
```

```gherkin
Given a candidate has no submitted feedback
When I open the candidate detail page
Then the system shows that feedback is not available yet
```

```gherkin
Given I am not authorized
When I try to view candidate feedback
Then the system denies access
```

---

## US-29: Compare Candidates

**User Story**

As a hiring manager, I want to compare candidates by status, rating, and feedback, so that I can make better hiring decisions.

**Acceptance Criteria**

```gherkin
Given I am logged in as a hiring manager
When I select multiple candidates for comparison
Then the system displays their status, ratings, and feedback summary side by side
```

```gherkin
Given I select fewer than two candidates
When I click compare
Then the system shows a message asking me to select at least two candidates
```

```gherkin
Given I am not authorized
When I try to use candidate comparison
Then the system denies access
```

---

## US-30: Approve Final Hiring Decision

**User Story**

As a hiring manager, I want to approve final hiring decisions, so that offers are controlled before being sent.

**Acceptance Criteria**

```gherkin
Given I am logged in as a hiring manager
When I approve a final offer decision
Then the system records the approval successfully
```

```gherkin
Given the hiring manager has approved the final decision
When HR opens the candidate detail page
Then HR can see that the decision has been approved
```

```gherkin
Given I am not a hiring manager
When I try to approve a final hiring decision
Then the system denies access
```

---

## US-31: Manage User Accounts

**User Story**

As a system admin, I want to create, update, and deactivate user accounts, so that system access can be managed.

**Acceptance Criteria**

```gherkin
Given I am logged in as a system admin
When I create a new user account with valid information
Then the system creates the user account successfully
```

```gherkin
Given I am logged in as a system admin
When I update a user's information
Then the system saves the updated information
```

```gherkin
Given I am logged in as a system admin
When I deactivate a user account
Then the user can no longer log in to the system
```

```gherkin
Given I am not a system admin
When I try to manage user accounts
Then the system denies access
```

---

## US-32: Assign User Roles

**User Story**

As a system admin, I want to assign user roles, so that each user has correct permissions.

**Acceptance Criteria**

```gherkin
Given I am logged in as a system admin
When I assign a role to a user
Then the user receives the permissions of that role
```

```gherkin
Given I am logged in as a system admin
When I change a user's role
Then the user's access permissions are updated based on the new role
```

```gherkin
Given I am not a system admin
When I try to assign roles
Then the system denies access
```

---

## US-33: Configure Internship Programs

**User Story**

As a system admin, I want to create and update internship programs, so that HR can manage different recruitment campaigns.

**Acceptance Criteria**

```gherkin
Given I am logged in as a system admin
When I create an internship program with valid information
Then the system creates the program successfully
```

```gherkin
Given I am logged in as a system admin
When I update an internship program
Then the system saves the updated program information
```

```gherkin
Given an internship program is closed
When a candidate tries to apply to that program
Then the system prevents application submission
```

---

## US-34: View System Activity Logs

**User Story**

As a system admin, I want to view system activity logs, so that important actions can be audited.

**Acceptance Criteria**

```gherkin
Given I am logged in as a system admin
When I open the activity log page
Then the system displays important system actions
```

```gherkin
Given an HR recruiter updates candidate status
When the update is saved successfully
Then the action is recorded in the activity log
```

```gherkin
Given I am not a system admin
When I try to access the activity log page
Then the system denies access
```

## 4. Acceptance Criteria Quality Checklist

| Checklist Item | Description |
|---|---|
| Clear condition | The Given part explains the starting situation. |
| Clear action | The When part explains what the user or system does. |
| Clear result | The Then part explains the expected result. |
| Testable | QA can create test cases from the acceptance criteria. |
| Linked to user story | Each acceptance criterion belongs to a user story. |
| Covers negative cases | Important error or invalid cases are included. |
| Covers permission rules | Access control is included when needed. |
| Matches SRS | Acceptance criteria should match functional requirements, validation rules, and permission rules in the SRS. |

## 5. BA Notes

Acceptance criteria make user stories testable and reduce misunderstanding between stakeholders, developers, and QA engineers.

In this project, the most important acceptance criteria focus on form validation, file upload rules, status transition rules, interview scheduling rules, feedback submission rules, and role-based access control.

The next step is to create wireframe specifications for the main screens of InternshipHub.
