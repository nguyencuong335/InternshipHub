# 12. Project Summary for Interview

## 1. Project Pitch

**InternshipHub** is a web-based recruitment management platform designed specifically for the internship lifecycle. It streamlines and automates the process of candidate application, automated validation, HR screening, interviewer scheduling, feedback collection, and final hiring approval. By providing a single system of record, it replaces fragmented communication tools and manual spreadsheets, reducing administrative workload and improving hiring quality.

## 2. Business Problem

Prior to the system, the company managed internship recruitment via disjointed email threads, chat apps, and tracking spreadsheets. This caused several operational pain points:
- **Inefficiency:** HR manually tracked candidate status and scheduled interviews, causing high admin overhead.
- **Low Transparency:** Candidates had no way to track their application status, resulting in excessive status inquiries.
- **Unstructured Feedback:** Interviewers submitted feedback via chat or email in varying formats, making it hard to compare candidate skills objectively.
- **Information Silos:** Hiring managers had no central dashboard to view candidate pipeline data, causing delays in hiring decisions.
- **Poor Auditability:** No historical log of candidate status changes existed to track recruiter performance or ensure process compliance.

## 3. Key Stakeholders

- **Candidate:** Submits applications, uploads CVs, and views application status updates.
- **HR Recruiter:** Manages applications, screens profiles, schedules interviews, assigns interviewers, and handles candidate status transitions.
- **Interviewer:** Reviews assigned candidate profiles, conducts interviews, and submits structured feedback (rating, comment, recommendation).
- **Hiring Manager:** Oversees the recruitment pipeline, compares candidates, and signs off on final hiring decisions.
- **System Admin:** Manages user accounts, configures roles and permissions, and maintains internship program metadata.

## 4. Main Requirements

The solution is structured into five core modules:
1. **Candidate Module:** Account registration/login, profile creation, CV file upload with validation (PDF/DOCX, <=5MB), and application submission.
2. **HR Recruiter Module:** Application dashboard with search/filters, status updates with transition validation, interview scheduling, and offer/rejection distribution.
3. **Interviewer Module:** Dashboard of assigned candidates, candidate CV viewer, and structured feedback form (technical/communication rating, comments, recommendation).
4. **Hiring Manager Module:** Pipeline overview dashboard, candidate comparison tool, and hiring approval workflow.
5. **Admin Module:** User/role management, internship program configuration, and audit log viewer.

## 5. AS-IS vs TO-BE Process

- **AS-IS (Manual Process):** Candidate emails application -> HR manually downloads CV and logs it in a spreadsheet -> HR manually contacts candidate to schedule interviews -> Interview is conducted -> Interviewer sends feedback text via email/Slack -> HR manually updates the spreadsheet -> Hiring Manager makes final decisions based on ad-hoc discussions -> HR manually sends final notification.
- **TO-BE (System-Driven Process):** Candidate registers on the portal -> Candidate uploads CV -> System validates file type/size and creates application -> HR reviews candidate profile in the system -> HR schedules interview and assigns interviewer in-app -> System automatically sends notifications -> Interviewer submits structured feedback form in-app -> Hiring Manager views consolidated pipeline and feedback to make decisions -> System logs status history and helps HR send final offers/rejections.

## 6. Hardest Part

The most challenging aspect of this project was defining the **Candidate Status Transition Rules** and enforcing the corresponding **Permission Matrix**.
- **The Challenge:** Enforcing that candidate states transition only through the approved lifecycle (e.g., preventing a recruiter from moving a candidate from "Draft" directly to "Interview Scheduled", or from "Rejected" to "Offered" without proper authorization).
- **The Resolution:** I mapped out the status transitions into a state transition matrix and wrote specific Validation Rules (VR-07 to VR-10). I then created a detailed Permission Matrix showing exactly what feature actions each user role can perform, ensuring strict Role-Based Access Control (RBAC).

## 7. What I Learned

Through this project, I strengthened my end-to-end business analysis skills:
- **Logical Flow:** Learned to structure requirements logically, tracing from high-level business problems down to functional specifications, user stories, acceptance criteria, and test scenarios.
- **Structured Specifications:** Understood that requirements must be explicit, testable, and free of ambiguity (e.g., using specific file sizes like "5MB" or strict status transition rules) to avoid misalignment with developers and QA.
- **Traceability:** Realized the critical importance of a Requirement Traceability Matrix (RTM) to ensure that every business objective is addressed by functional requirements, mapped to user stories, and verified by test scenarios.

## 8. How I Would Present This Project in an Interview

1. **Start with the "Why" (Business Value):** I would frame the project by explaining the business problem first—how manual recruitment was causing delays, high admin overhead, and poor candidate experience.
2. **Walk Through the Methodology:** I would describe my process from stakeholder identification and AS-IS modeling to translating business needs into the BRD and SRS.
3. **Highlight Key Artifacts:** I would show how I decomposed functional requirements into Agile user stories with clear Given-When-Then acceptance criteria, and how I collaborated with QA by defining test scenarios.
4. **Demonstrate Conflict/Complexity Resolution:** I would use the status transition rules and permission matrix as an example of how I resolved complex business logic and translated it into clear rules for development.
5. **Summarize with Outcomes:** I would conclude by pointing to the success metrics (e.g., reducing manual tracking effort by 50% and improving status update accuracy to 95%).
