# InternshipHub - Business Analyst Portfolio Project

## Project Highlights
This Business Analyst portfolio showcases a comprehensive, end-to-end requirement engineering process for an internship recruitment management system. The repository includes:
- **Business Requirements Document (BRD)** & **Software Requirements Specification (SRS)**
- **Stakeholder Analysis** & **RACI Matrix**
- **AS-IS and TO-BE Process Workflows** (Mermaid & PNG diagrams)
- **Agile Backlog & User Stories** with **Acceptance Criteria** (Given-When-Then format)
- **Wireframe Specifications** (low-fidelity screen design)
- **Test Scenarios** & **Requirement Traceability Matrix (RTM)**
- **Project Summary for Interview** to support portfolio presentation

---

## 1. Project Overview

**InternshipHub** is a Business Analyst portfolio case study for an internship application and interview management system.

The system is designed to help companies manage internship recruitment in one centralized workflow, from candidate application submission to interview feedback and final hiring decision.

This repository focuses on Business Analyst artifacts, not full software implementation. It demonstrates how a BA analyzes business problems, documents requirements, models workflows, supports Agile backlog creation, and prepares testable requirements for development and QA teams.

---

## 2. How to Use This Repository
For recruiters and hiring managers reviewing this portfolio, it is recommended to read the artifacts in the following logical sequence:
1. **[Project Overview](docs/00_project_overview.md)** - Understand the project's background and objectives.
2. **[Stakeholder Analysis](docs/01_stakeholder_analysis.md)** - Identify key users, their pain points, goals, and the RACI matrix.
3. **[AS-IS Process Analysis](docs/02_as_is_process.md)** & **[TO-BE Process Analysis](docs/03_to_be_process.md)** - Compare the current manual flow with the proposed system flow.
4. **[Business Requirements Document (BRD)](docs/04_brd_business_requirements.md)** - Review high-level business objectives and rules.
5. **[Software Requirements Specification (SRS)](docs/05_srs_software_requirements.md)** - Dive into detailed functional/non-functional requirements, data schemas, and validation rules.
6. **[User Stories and Product Backlog](docs/06_user_stories_product_backlog.md)** - See the breakdown of features into user stories and MVP sprint backlog.
7. **[Acceptance Criteria](docs/07_acceptance_criteria.md)** - Check the detailed requirements in Given-When-Then format.
8. **[Wireframe Specification](docs/08_wireframe_specification.md)** - Explore screen layouts and user interface definitions.
9. **[Test Scenarios](docs/09_test_scenarios.md)** - Review system verification scenarios and test cases.
10. **[Requirement Traceability Matrix (RTM)](docs/10_requirement_traceability_matrix.md)** - Trace business rules and functional requirements to user stories and test scenarios.
11. **[BA Interview Story](docs/11_ba_interview_story.md)** - Read the case study reflection and interview preparation story.
12. **[Project Summary for Interview](docs/12_project_summary_for_interview.md)** - Use the concise interview-ready summary for portfolio presentation.

---

## 3. Business Problem

Many companies manage internship recruitment through email, spreadsheets, chat tools, and manual notes. This process becomes difficult to control when the number of candidates increases.

Key problems include:

- Candidate information is stored in many places.
- HR needs to update candidate status manually.
- Candidates do not know their current application status.
- Interview feedback is not standardized.
- Hiring managers cannot easily view the full recruitment pipeline.
- There is no clear status history for audit and tracking.

---

## 4. Proposed Solution

InternshipHub centralizes the recruitment workflow by allowing:

- Candidates to submit applications and track status.
- HR recruiters to screen candidates, update status, and schedule interviews.
- Interviewers to view assigned candidates and submit structured feedback.
- Hiring managers to view pipeline data and approve final decisions.
- Admins to manage users, roles, and internship programs.

---

## 5. BA Artifacts Included

| Artifact | File |
|---|---|
| Project Overview | [docs/00_project_overview.md](docs/00_project_overview.md) |
| Stakeholder Analysis | [docs/01_stakeholder_analysis.md](docs/01_stakeholder_analysis.md) |
| AS-IS Process Analysis | [docs/02_as_is_process.md](docs/02_as_is_process.md) |
| TO-BE Process Analysis | [docs/03_to_be_process.md](docs/03_to_be_process.md) |
| Business Requirements Document | [docs/04_brd_business_requirements.md](docs/04_brd_business_requirements.md) |
| Software Requirements Specification | [docs/05_srs_software_requirements.md](docs/05_srs_software_requirements.md) |
| User Stories and Product Backlog | [docs/06_user_stories_product_backlog.md](docs/06_user_stories_product_backlog.md) |
| Acceptance Criteria | [docs/07_acceptance_criteria.md](docs/07_acceptance_criteria.md) |
| Wireframe Specification | [docs/08_wireframe_specification.md](docs/08_wireframe_specification.md) |
| Test Scenarios | [docs/09_test_scenarios.md](docs/09_test_scenarios.md) |
| Requirement Traceability Matrix | [docs/10_requirement_traceability_matrix.md](docs/10_requirement_traceability_matrix.md) |
| BA Interview Story | [docs/11_ba_interview_story.md](docs/11_ba_interview_story.md) |
| Project Summary for Interview | [docs/12_project_summary_for_interview.md](docs/12_project_summary_for_interview.md) |

---

## 6. Diagram Files

| Diagram | Source File | Rendered Image |
|---|---|---|
| AS-IS Process Diagram | [diagrams/as_is_process.mmd](diagrams/as_is_process.mmd) | [assets/as_is_process.png](assets/as_is_process.png) |
| TO-BE Process Diagram | [diagrams/to_be_process.mmd](diagrams/to_be_process.mmd) | [assets/to_be_process.png](assets/to_be_process.png) |

### AS-IS Process Diagram
![AS-IS Process](assets/as_is_process.png)

### TO-BE Process Diagram
![TO-BE Process](assets/to_be_process.png)

---

## 7. Repository Structure

```text
├── README.md
├── .gitignore
├── assets/
│   ├── as_is_process.png
│   └── to_be_process.png
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
│   ├── 11_ba_interview_story.md
│   └── 12_project_summary_for_interview.md
├── diagrams/
│   ├── as_is_process.mmd
│   └── to_be_process.mmd
└── templates/
    ├── stakeholder_interview_questions.md
    ├── requirement_template.md
    └── change_request_template.md
```

---

## 8. BA Skills Demonstrated

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
| Interview storytelling | Project summary and BA interview story |

---

## 9. What I Learned as a Business Analyst

This project helped me learn how to move from a business problem to stakeholder analysis, AS-IS/TO-BE process modeling, BRD, SRS, user stories, acceptance criteria, wireframe specification, test scenarios, and RTM. It also helped me understand that a Business Analyst must make requirements clear, testable, and connected to business value.

---

## 10. Key Project Scope

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
