# InternshipHub - Business Analyst Portfolio Project

## 1. Project Overview

**InternshipHub** is a Business Analyst portfolio case study for an internship application and interview management system.

The system is designed to help companies manage internship recruitment in one centralized workflow, from candidate application submission to interview feedback and final hiring decision.

This repository focuses on Business Analyst artifacts, not full software implementation. It demonstrates how a BA analyzes business problems, documents requirements, models workflows, supports Agile backlog creation, and prepares testable requirements for development and QA teams.

## 2. Business Problem

Many companies manage internship recruitment through email, spreadsheets, chat tools, and manual notes. This process becomes difficult to control when the number of candidates increases.

Key problems include:

- Candidate information is stored in many places.
- HR needs to update candidate status manually.
- Candidates do not know their current application status.
- Interview feedback is not standardized.
- Hiring managers cannot easily view the full recruitment pipeline.
- There is no clear status history for audit and tracking.

## 3. Proposed Solution

InternshipHub centralizes the recruitment workflow by allowing:

- Candidates to submit applications and track status.
- HR recruiters to screen candidates, update status, and schedule interviews.
- Interviewers to view assigned candidates and submit structured feedback.
- Hiring managers to view pipeline data and approve final decisions.
- Admins to manage users, roles, and internship programs.

## 4. BA Artifacts Included

| Artifact | File |
|---|---|
| Project Overview | `docs/00_project_overview.md` |
| Stakeholder Analysis | `docs/01_stakeholder_analysis.md` |
| AS-IS Process Analysis | `docs/02_as_is_process.md` |
| TO-BE Process Analysis | `docs/03_to_be_process.md` |
| Business Requirements Document | `docs/04_brd_business_requirements.md` |
| Software Requirements Specification | `docs/05_srs_software_requirements.md` |
| User Stories and Product Backlog | `docs/06_user_stories_product_backlog.md` |
| Acceptance Criteria | `docs/07_acceptance_criteria.md` |
| Wireframe Specification | `docs/08_wireframe_specification.md` |
| Test Scenarios | `docs/09_test_scenarios.md` |
| Requirement Traceability Matrix | `docs/10_requirement_traceability_matrix.md` |
| BA Interview Story | `docs/11_ba_interview_story.md` |

## 5. Diagram Files

| Diagram | File |
|---|---|
| AS-IS Process Diagram | `diagrams/as_is_process.mmd` |
| TO-BE Process Diagram | `diagrams/to_be_process.mmd` |

You can preview Mermaid diagrams by using:

- VS Code Mermaid preview extensions
- Mermaid Live Editor
- GitHub Markdown preview, if Mermaid rendering is supported

## 6. Repository Structure

```text
internshiphub-ba-portfolio/
├── README.md
├── .gitignore
├── docs/
│   ├── 00_project_overview.md
│   ├── 01_stakeholder_analysis.md
│   ├── 02_as_is_process.md
│   ├── 03_to_be_process.md
│   ├── 04_brd_business_requirements.md
│   ├── 05_srs_software_requirements.md
│   ├── 06_user_stories_product_backlog.md
│   ├── 07_acceptance_criteria.md
│   ├── 08_wireframe_specification.md
│   ├── 09_test_scenarios.md
│   ├── 10_requirement_traceability_matrix.md
│   └── 11_ba_interview_story.md
├── diagrams/
│   ├── as_is_process.mmd
│   └── to_be_process.mmd
└── templates/
    ├── stakeholder_interview_questions.md
    ├── requirement_template.md
    └── change_request_template.md
```

## 7. BA Skills Demonstrated

| BA Skill | Evidence in This Repository |
|---|---|
| Business problem analysis | Project overview, business problem, business objectives |
| Stakeholder analysis | Stakeholder list, goals, pain points, RACI matrix |
| Process modeling | AS-IS and TO-BE process analysis |
| Requirement documentation | BRD and SRS |
| Agile requirement writing | Epics, user stories, product backlog, MVP backlog |
| Acceptance criteria writing | Given-When-Then acceptance criteria |
| Wireframe thinking | Low-fidelity wireframe specification |
| QA collaboration | Test scenarios and expected results |
| Traceability | Requirement Traceability Matrix |
| Change awareness | Change request template and gap analysis |

## 8. Key Project Scope

### In Scope

- Candidate registration and login
- Candidate profile and CV upload
- Internship application submission
- Candidate status tracking
- HR candidate management
- Candidate status updates
- Interview scheduling
- Interviewer feedback submission
- Hiring manager pipeline view
- Admin user and role management
- Requirement traceability and test scenarios

### Out of Scope

- AI-based CV screening
- Online coding test
- Payroll management
- Employee onboarding
- Integration with external HRM systems
- Full production-level source code
