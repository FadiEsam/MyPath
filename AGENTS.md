\# AGENTS.md



\## Table of Contents



\- \[1. Purpose](#1-purpose)

\- \[2. Project Overview](#2-project-overview)

\- \[3. Project Documentation](#3-project-documentation)

\- \[4. Technology Stack](#4-technology-stack)

\- \[5. Architecture and Code Organization](#5-architecture-and-code-organization)

\- \[6. Requirements and Business Rules](#6-requirements-and-business-rules)

\- \[7. Database Guidelines](#7-database-guidelines)

\- \[8. Security Guidelines](#8-security-guidelines)

\- \[9. Coding Standards](#9-coding-standards)

\- \[10. Testing and Verification](#10-testing-and-verification)

\- \[11. Development Workflow](#11-development-workflow)

\- \[12. Scope Control](#12-scope-control)

\- \[13. Git and Version Control](#13-git-and-version-control)

\- \[14. Communication and Decision-Making](#14-communication-and-decision-making)



\## 1. Purpose



This file defines the working instructions for AI coding agents and other development assistants working on MyPath.



Its purpose is to maintain consistency, protect established project decisions, reduce unnecessary complexity, and support maintainable development.



All agents must read and follow these instructions before making significant changes to the project.



When a task conflicts with an existing requirement, architecture decision, or security rule, the agent must identify the conflict before proceeding.



\## 2. Project Overview



MyPath is a personal career, learning, project management, time-tracking, and freelance business management platform.



Its initial version is designed primarily for personal use. The project may expand in the future to support separate views for clients, recruiters, and other users.



The platform is intended to help track and analyze:



\- Skills, knowledge levels, and learning progress.

\- Courses, learning resources, and practice activities.

\- Projects, tasks, development phases, and working time.

\- Freelance services, clients, and project records.

\- Invoices, revenue, expenses, hosting costs, and profitability.

\- Historical records and measurable performance indicators.



MyPath is not intended to be a general-purpose freelance marketplace, social network, enterprise resource planning system, or employee surveillance tool.



The initial implementation must prioritize practical personal use, reliable data, clear organization, and future maintainability.



\## 3. Project Documentation



Project documentation is an important part of development, not an optional activity.



Before implementing a feature, consult the relevant documentation under `docs/` and review existing decisions when necessary.



Follow these rules:



\- Treat approved requirements and documented decisions as the primary references for intended system behavior.

\- Update affected documentation when an approved change alters requirements, architecture, data models, or other documented behavior.

\- Avoid duplicating detailed explanations across multiple documents.

\- Use clear, simple English in project documentation.

\- Include a functional Markdown table of contents in every project document that requires one.

\- Ensure each table of contents link matches the actual heading and GitHub Markdown anchor.

\- Keep documentation consistent with the implemented system.

\- Do not invent requirements or present proposed features as approved decisions.

\- Do not create unnecessary documentation files when an existing document is the appropriate location.



Use the following files according to their responsibilities:



\- `README.md`: Project introduction, setup, and usage information.

\- `AGENTS.md`: Development instructions for AI agents.

\- `CHANGELOG.md`: A record of notable project changes.

\- `docs/`: Requirements, architecture, database design, and other detailed project documentation.

\- `decision-log.md`, if present: Historical architectural and business decisions, including their rationale.



If a referenced document does not exist, do not assume its contents. Identify the missing information when it affects the task.



\## 4. Technology Stack



The initial technology stack is:



\- Backend: PHP without a framework.

\- Frontend: HTML, CSS, and JavaScript.

\- Database: PostgreSQL.

\- Development environment: Local development environment.



Use the existing stack unless a change has been explicitly approved.



Do not introduce Laravel, React, Next.js, TypeScript, or other frameworks and technologies solely because they may be useful in the future.



Future technology changes are permitted when supported by a clear requirement, learning objective, or architectural decision.



Prefer simple, understandable implementations over unnecessary abstractions, dependencies, and infrastructure.



Do not assume that every technology listed in future plans is already installed or configured.



\## 5. Architecture and Code Organization



Follow the project's documented architecture and directory structure.



Apply the following principles:



\- Separate responsibilities between application logic, data access, request handling, and presentation where appropriate.

\- Keep business rules independent of presentation whenever practical.

\- Avoid unnecessary coupling between modules.

\- Use reusable components when they reduce duplication without making the system harder to understand.

\- Prefer clear interfaces and predictable data flow.

\- Avoid introducing distributed services or complex infrastructure without a demonstrated need.

\- Preserve existing project conventions unless a change is justified and approved.



Do not reorganize large parts of the codebase or introduce a new architectural pattern as an unrelated side effect of a small feature.



Before changing the architecture, explain the reason, affected components, benefits, and potential risks.



\## 6. Requirements and Business Rules



Existing approved requirements and business rules must be respected.



In particular:



\- Distinguish skills, services, projects, tasks, courses, and learning resources according to their documented responsibilities.

\- Record time against the appropriate task, project phase, or skill as defined by the approved data model.

\- Keep financial records sufficiently structured to support revenue, expenses, hosting costs, and profitability analysis.

\- Do not introduce unsupported progress percentages or performance claims.

\- Base analytical results on available and sufficiently reliable data.

\- Do not silently change the meaning of existing records or calculations.

\- Keep personal-use requirements separate from possible future multi-user features.



When requirements are incomplete or contradictory, explain the ambiguity and ask for clarification if it materially affects the implementation.



Do not resolve important business decisions through assumptions hidden in code.



\## 7. Database Guidelines



PostgreSQL is the initial database system.



Follow these guidelines:



\- Use appropriate primary keys, foreign keys, constraints, and indexes.

\- Define relationships and deletion behavior according to the documented data model.

\- Use transactions for operations that must succeed or fail as a unit.

\- Use parameterized queries for database operations.

\- Avoid unnecessary duplication of authoritative data.

\- Store timestamps and dates using appropriate database types and consistent conventions.

\- Represent money using appropriate exact numeric types rather than floating-point types.

\- Use database migrations or an equivalent documented, repeatable schema-change process.

\- Update the relevant schema documentation when the data model changes.

\- Use seed data only for development or explicitly intended initialization.

\- Never use real secrets or sensitive production data in sample datasets.



Do not modify existing schema structures, delete data, or change relationships without understanding the impact.



Database changes must remain consistent with application logic and existing records.



\## 8. Security Guidelines



Security must be considered throughout development.



At a minimum:



\- Validate and normalize input on the server side.

\- Use parameterized database queries.

\- Escape output appropriately to reduce cross-site scripting risks.

\- Apply CSRF protection to relevant state-changing web requests.

\- Use secure password hashing if authentication is introduced.

\- Enforce authorization on the server side when access control is introduced.

\- Never expose credentials, API keys, database passwords, or other secrets in source code.

\- Keep local environment files and sensitive configuration out of version control.

\- Avoid exposing internal errors, stack traces, or sensitive database details to users.

\- Avoid logging passwords, authentication tokens, or unnecessary personal information.

\- Treat uploaded files and external input as untrusted.



Security measures must match the actual features being implemented. Do not claim that the system is secure without appropriate verification.



\## 9. Coding Standards



Write code that is clear, consistent, and maintainable.



Follow these rules:



\- Use meaningful and consistent names for variables, functions, classes, tables, and files.

\- Keep functions and modules focused on clearly defined responsibilities.

\- Avoid unnecessary duplication and deeply nested logic.

\- Add comments when they explain important reasoning, constraints, or non-obvious behavior.

\- Do not add comments that merely repeat what the code already says.

\- Handle errors explicitly and provide useful diagnostic information without exposing sensitive details.

\- Avoid adding dependencies for functionality that can be implemented simply with the existing stack.

\- Follow the established formatting and naming conventions of the relevant language.

\- Remove temporary debugging code before completing a task.



Do not rewrite unrelated code merely to match personal style preferences.



\## 10. Testing and Verification



Testing must reflect the scope and risk of each change.



When applicable:



\- Test normal and expected use cases.

\- Test invalid input and relevant boundary conditions.

\- Verify database constraints and important relationships.

\- Test authorization and security-sensitive behavior.

\- Test error handling and failure scenarios.

\- Run relevant existing automated tests after modifications.

\- Verify that existing functionality has not been unintentionally broken.



If automated tests do not exist, use appropriate manual verification and identify any important remaining gaps.



Never claim that tests passed, code executed successfully, or a feature was verified unless the corresponding checks were actually performed.



Clearly distinguish implemented functionality from functionality that remains untested.



\## 11. Development Workflow



For each development task, follow this workflow:



1\. Understand the request and its expected outcome.

2\. Inspect the relevant source files and documentation.

3\. Identify affected components, dependencies, and potential risks.

4\. Check whether the task conflicts with approved requirements or decisions.

5\. Implement the smallest complete solution that satisfies the requirement.

6\. Run relevant tests or verification procedures.

7\. Update affected documentation when necessary.

8\. Summarize the changes, verification results, and any remaining limitations.



For complex or high-impact changes, present the proposed approach and obtain approval before implementation when the decision has not already been authorized.



For small, clearly defined changes, proceed without unnecessary confirmation.



Do not silently skip required steps because an implementation appears straightforward.



\## 12. Scope Control



Keep development focused on the current approved scope.



\- Do not add unrelated features.

\- Do not introduce future multi-user functionality before it is required.

\- Do not implement payment processing, AI integrations, or external services unless explicitly approved.

\- Do not add unnecessary frameworks, packages, or infrastructure.

\- Do not change business rules to simplify implementation without approval.

\- Do not create artificial metrics or fabricate historical data.

\- Do not remove existing functionality without understanding the consequences and obtaining approval when required.



Future expansion should be supported through clear design and reasonable modularity, not through premature implementation.



\## 13. Git and Version Control



Follow the project's `.gitignore` rules and existing Git workflow.



\- Do not commit secrets, credentials, local environment files, or sensitive personal data.

\- Keep temporary files, generated artifacts, and local-only configuration out of version control when appropriate.

\- Review changes before committing.

\- Avoid unrelated changes in the same task.

\- Use meaningful commit messages when creating commits is requested or authorized.

\- Do not rewrite Git history, force-push, or discard existing work without explicit authorization.

\- Do not overwrite user changes that have not been reviewed.

\- Keep the repository documentation consistent with committed changes.



Do not assume permission to commit, push, publish, or deploy simply because you have permission to modify local files.



\## 14. Communication and Decision-Making



Communicate important implementation details clearly and concisely.



When completing a task, report:



\- What changed.

\- Why the change was necessary.

\- Which files or components were affected.

\- Which tests or verification steps were performed.

\- Any known limitations, unresolved questions, or follow-up work.



Ask for clarification before making significant decisions that could affect business rules, data integrity, security, architecture, or project scope.



For minor implementation details, use the simplest reasonable solution consistent with the documented requirements.



When a new decision changes an existing approved decision, identify the conflict and update the appropriate documentation after approval.



Do not claim that a task is complete if required implementation or verification remains unfinished.

