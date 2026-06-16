# 10. Requirement Traceability Matrix

## 1. Purpose

This document defines the Requirement Traceability Matrix (RTM) for the InternshipHub system.

The purpose of the RTM is to make sure that every business requirement is connected to functional requirements, user stories, acceptance criteria, and test scenarios.

This helps the BA, Developer, QA Engineer, and stakeholder check requirement coverage and reduce missing scope.

## 2. What is a Requirement Traceability Matrix?

A Requirement Traceability Matrix is a table that tracks requirements from business need to testing.

In this project, the traceability flow is:

```text
Business Requirement → Functional Requirement → User Story → Acceptance Criteria → Test Scenario
```

This means that each business requirement should be supported by system features, user stories, acceptance criteria, and test scenarios.

## 3. Traceability Levels

| Level | Meaning | Source Document |
|---|---|---|
| Business Requirement | What the business needs | 04_brd_business_requirements.md |
| Functional Requirement | What the system must do | 05_srs_software_requirements.md |
| User Story | Requirement from user perspective | 06_user_stories_product_backlog.md |
| Acceptance Criteria | Conditions to accept the story | 07_acceptance_criteria.md |
| Test Scenario | Scenario to verify the requirement | 09_test_scenarios.md |

## 4. Requirement Traceability Matrix

| Business Requirement | Functional Requirement | User Story | Acceptance Criteria | Test Scenario |
|---|---|---|---|---|
| BR-01: The system shall allow candidates to submit internship applications online. | FR-01, FR-02, FR-06, FR-07 | US-01, US-02, US-05, US-06 | AC for US-01, US-02, US-05, US-06 | TC-001 to TC-007, TC-016 to TC-022 |
| BR-02: The system shall allow candidates to upload their CV and personal information. | FR-03, FR-04, FR-05 | US-03, US-04 | AC for US-03, US-04 | TC-008 to TC-015 |
| BR-03: The system shall allow HR to view and manage all submitted applications. | FR-10, FR-11, FR-12, FR-13 | US-10, US-11, US-12, US-13 | AC for US-10, US-11, US-12, US-13 | TC-029 to TC-039 |
| BR-04: The system shall allow HR to update candidate recruitment status. | FR-14, FR-15, FR-16 | US-14, US-15, US-16 | AC for US-14, US-15, US-16 | TC-040 to TC-048 |
| BR-05: The system shall allow HR to schedule interviews and assign interviewers. | FR-17, FR-18 | US-18, US-19, US-20 | AC for US-18, US-19, US-20 | TC-049 to TC-056 |
| BR-06: The system shall allow interviewers to view assigned candidates. | FR-20, FR-21, FR-25 | US-21, US-22, US-26 | AC for US-21, US-22, US-26 | TC-057 to TC-061 |
| BR-07: The system shall allow interviewers to submit structured interview feedback. | FR-22, FR-23, FR-24 | US-23, US-24, US-25 | AC for US-23, US-24, US-25 | TC-062 to TC-069 |
| BR-08: The system shall allow hiring managers to view recruitment pipeline and candidate feedback. | FR-26, FR-27, FR-28, FR-29 | US-27, US-28, US-29, US-30 | AC for US-27, US-28, US-29, US-30 | TC-070 to TC-078 |
| BR-09: The system shall notify candidates when their application status changes. | FR-09, FR-19 | US-08, US-17 | AC for US-08, US-17 | TC-027, TC-028, TC-076 to TC-078 |
| BR-10: The system shall store status history for tracking and audit purposes. | FR-16, FR-33, NFR-06 | US-16, US-34 | AC for US-16, US-34 | TC-045 to TC-047, TC-089 to TC-091 |
| BR-11: The system shall support role-based access control for different user types. | FR-25, FR-30, FR-31, NFR-02, NFR-03, NFR-04, NFR-05 | US-26, US-31, US-32 | AC for US-26, US-31, US-32 | TC-007, TC-022, TC-025, TC-031, TC-039, TC-055, TC-059, TC-061, TC-065, TC-072, TC-078, TC-082, TC-085, TC-091 |

## 5. Functional Requirement Coverage Matrix

| Functional Requirement | Related User Story | Related Test Scenario | Coverage Status |
|---|---|---|---|
| FR-01: Candidate registration | US-01 | TC-001, TC-002, TC-003 | Covered |
| FR-02: Login and logout | US-02 | TC-004, TC-005, TC-006, TC-007 | Covered |
| FR-03: Create and update profile | US-03 | TC-008, TC-009, TC-010 | Covered |
| FR-04: Upload CV | US-04 | TC-011, TC-012, TC-015 | Covered |
| FR-05: Validate CV file type and size | US-04 | TC-013, TC-014 | Covered |
| FR-06: Apply for internship program | US-05 | TC-016, TC-017, TC-018, TC-019, TC-020 | Covered |
| FR-07: View submitted application | US-06 | TC-021, TC-022 | Covered |
| FR-08: View current application status | US-07 | TC-023, TC-024, TC-025 | Covered |
| FR-09: Candidate status notification | US-08 | TC-027, TC-028 | Covered |
| FR-10: HR views all submitted applications | US-10 | TC-029, TC-030, TC-031 | Covered |
| FR-11: HR searches candidates | US-11 | TC-032, TC-033, TC-034 | Covered |
| FR-12: HR filters candidates | US-12 | TC-035, TC-036, TC-037 | Covered |
| FR-13: HR views candidate profile and CV | US-13 | TC-038, TC-039 | Covered |
| FR-14: HR updates candidate status | US-14 | TC-040, TC-048 | Covered |
| FR-15: Validate status transitions | US-15 | TC-041, TC-042, TC-043, TC-044 | Covered |
| FR-16: Record status changes | US-16 | TC-045, TC-046, TC-047 | Covered |
| FR-17: Schedule interviews | US-18 | TC-049, TC-050, TC-051, TC-052 | Covered |
| FR-18: Assign interviewers | US-19, US-20 | TC-053, TC-054, TC-055, TC-056 | Covered |
| FR-19: Send offer or rejection results | US-17 | TC-076, TC-077, TC-078 | Covered |
| FR-20: View assigned interviews | US-21 | TC-057, TC-058, TC-059 | Covered |
| FR-21: View assigned candidate profile and CV | US-22 | TC-060, TC-061 | Covered |
| FR-22: Submit structured feedback | US-23 | TC-062, TC-065, TC-066 | Covered |
| FR-23: Required feedback fields | US-24 | TC-063 | Covered |
| FR-24: Recommendation Pass, Fail, or Hold | US-25 | TC-064, TC-067, TC-068, TC-069 | Covered |
| FR-25: Prevent interviewer from viewing unassigned candidates | US-26 | TC-059, TC-061, TC-065 | Covered |
| FR-26: View recruitment pipeline | US-27 | TC-070, TC-071, TC-072 | Covered |
| FR-27: View candidate feedback | US-28 | TC-073, TC-074 | Covered |
| FR-28: Compare candidates | US-29 | TC-075, TC-076 | Covered |
| FR-29: Approve final hiring decisions | US-30 | TC-077, TC-078 | Covered |
| FR-30: Manage user accounts | US-31 | TC-079, TC-080, TC-081, TC-082 | Covered |
| FR-31: Assign user roles | US-32 | TC-083, TC-084, TC-085 | Covered |
| FR-32: Configure internship programs | US-33 | TC-086, TC-087, TC-088 | Covered |
| FR-33: View system activity logs | US-34 | TC-089, TC-090, TC-091 | Covered |

## 6. Non-Functional Requirement Coverage Matrix

| Non-Functional Requirement | Related Area | Related Test Scenario | Coverage Status |
|---|---|---|---|
| NFR-01: Candidate list should load within 3 seconds for up to 1,000 records. | HR Candidate Management | Performance test to be added in future version | Partially Covered |
| NFR-02: Authentication is required before protected pages. | Login and Access Control | TC-007, TC-031, TC-039, TC-055, TC-072, TC-082, TC-085, TC-091 | Covered |
| NFR-03: Data access is restricted by user roles. | Role-Based Access Control | TC-022, TC-025, TC-031, TC-039, TC-055, TC-059, TC-061, TC-065, TC-072, TC-078, TC-082, TC-085, TC-091 | Covered |
| NFR-04: Candidate can only view own application information. | Candidate Status and Application | TC-022, TC-025 | Covered |
| NFR-05: Interviewer can only view assigned candidates. | Interviewer Dashboard and Feedback | TC-059, TC-061, TC-065 | Covered |
| NFR-06: Important actions are recorded. | Status History and Activity Log | TC-045, TC-046, TC-089, TC-090 | Covered |
| NFR-07: System should be available 99% during recruitment periods. | Availability | Availability test to be added in future version | Partially Covered |
| NFR-08: UI should work on desktop and mobile browsers. | Usability and Compatibility | Cross-browser and responsive test to be added in future version | Partially Covered |
| NFR-09: CV upload should support PDF and DOCX files. | CV Upload | TC-011, TC-012, TC-013 | Covered |
| NFR-10: System should show clear validation messages. | Validation | TC-003, TC-009, TC-014, TC-017, TC-018, TC-050, TC-063, TC-064, TC-076 | Covered |

## 7. MVP Requirement Coverage

The MVP focuses on the core recruitment workflow.

| MVP Area | Business Requirement | Functional Requirement | User Story | Test Scenario | Status |
|---|---|---|---|---|---|
| Candidate application | BR-01, BR-02 | FR-01 to FR-07 | US-01 to US-06 | TC-001 to TC-022 | Covered |
| Candidate status tracking | BR-09 | FR-08, FR-09 | US-07, US-08 | TC-023 to TC-028 | Covered |
| HR candidate management | BR-03, BR-04, BR-10 | FR-10 to FR-16 | US-10 to US-16 | TC-029 to TC-048 | Covered |
| Interview scheduling | BR-05 | FR-17, FR-18 | US-18 to US-20 | TC-049 to TC-056 | Covered |
| Interview feedback | BR-06, BR-07 | FR-20 to FR-25 | US-21 to US-26 | TC-057 to TC-069 | Covered |
| Access control | BR-11 | FR-25, FR-30, FR-31, NFR-02 to NFR-05 | US-26, US-31, US-32 | Permission test cases across modules | Covered |

## 8. Gap Analysis

| Gap ID | Gap | Impact | Recommended Action |
|---|---|---|---|
| GAP-01 | Performance test for candidate list is not detailed yet. | Medium | Add performance test cases when technical architecture is defined. |
| GAP-02 | Availability test is not detailed yet. | Medium | Define uptime monitoring and availability testing in a later technical phase. |
| GAP-03 | Mobile responsiveness test is not detailed yet. | Low | Add UI compatibility test cases after UI prototype is created. |
| GAP-04 | Notification delivery failure handling may need more detail. | Medium | Add more detailed notification retry and failure handling requirements. |
| GAP-05 | Multiple interview rounds are not included in current MVP. | Medium | Keep as future enhancement unless stakeholder confirms it is required. |

## 9. Change Impact Example

If a stakeholder requests a new feature, the BA should update the RTM.

Example change:

```text
Change Request: Add multiple interview rounds.
```

Impact:

| Area | Impact |
|---|---|
| BRD | Add or update business requirement for multiple interview rounds. |
| SRS | Add functional requirements for interview round configuration and scheduling. |
| User Stories | Add stories for HR scheduling multiple rounds and interviewer submitting feedback per round. |
| Acceptance Criteria | Add Given–When–Then rules for each interview round. |
| Test Scenarios | Add test cases for first round, second round, and final round behavior. |
| Wireframe | Update interview scheduling page and feedback page. |

## 10. RTM Quality Checklist

| Checklist Item | Description |
|---|---|
| Every BR has related FR | Each business requirement should connect to at least one functional requirement. |
| Every FR has related user story | Each functional requirement should be represented in the backlog. |
| Every important user story has acceptance criteria | Core user stories should be testable. |
| Every core requirement has test scenario | MVP requirements should be verifiable by QA. |
| Permission rules are traceable | Security and access control should appear in requirements and tests. |
| Gaps are documented | Missing or partial coverage should be clearly recorded. |
| RTM is updated after change requests | Requirement changes should update all related artifacts. |

## 11. BA Notes

The Requirement Traceability Matrix is one of the most important BA artifacts because it connects business goals with system behavior and testing.

In this project, the RTM shows that the main InternshipHub requirements are covered from BRD to SRS, user stories, acceptance criteria, and test scenarios.

The RTM also helps identify gaps, especially for non-functional requirements such as performance, availability, and responsive UI testing.

The next step is to prepare project templates and GitHub documentation so that the repository looks professional as a BA portfolio project.
