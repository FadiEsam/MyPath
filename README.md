# MyPath — Personal Career & Project Management

MyPath is a personal platform designed to help individuals organize their professional development, manage learning activities, track projects, and monitor freelance work and financial performance.

The project aims to bring these activities together in one place, making it easier to understand what you are learning, what you are building, how you spend your time, and how your work develops over time.

> **Project status:** Under development. Features and technical details may change as development progresses.

## Table of Contents

- [1. Overview](#1-overview)
- [2. The Problem MyPath Addresses](#2-the-problem-mypath-addresses)
- [3. Project Goals](#3-project-goals)
- [4. Main Features](#4-main-features)
- [5. How MyPath Works](#5-how-mypath-works)
- [6. Target Users](#6-target-users)
- [7. Project Scope](#7-project-scope)
- [8. Development Approach](#8-development-approach)
- [9. Technology Stack](#9-technology-stack)
- [10. Project Structure](#10-project-structure)
- [11. Current Status](#11-current-status)
- [12. Future Development](#12-future-development)
- [13. Security and Privacy](#13-security-and-privacy)
- [14. License](#14-license)

---

## 1. Overview

MyPath is more than a task manager or a simple time-tracking application. It is designed to connect learning, skills, projects, professional services, and financial records so that users can build a clearer picture of their professional development.

For example, a person learning web development could use MyPath to:

- Organize courses and learning resources.
- Track skills such as HTML, CSS, JavaScript, PHP, and SQL.
- Plan a website project through design, database, backend, and frontend phases.
- Record the time spent learning and working on each project phase.
- Organize freelance services and client projects.
- Record invoices, revenue, expenses, and project-related costs.
- Review historical data to understand their progress and work patterns.

The main idea is to connect these activities rather than manage each one separately.

## 2. The Problem MyPath Addresses

Professional development often involves several disconnected tools.

A person might use one application for tasks, another for courses, a spreadsheet for project hours, and separate records for freelance income and expenses.

This separation can make it difficult to answer important questions:

- Which skills have I actually practiced?
- How much time have I spent on a particular skill?
- Which projects have helped me develop specific skills?
- How much time did each phase of a project require?
- Which freelance services generate revenue?
- What are the actual costs and profits of completed projects?

MyPath aims to organize these records in a connected system, allowing users to review their activities and make better decisions based on recorded information.

## 3. Project Goals

The main goals of MyPath are:

1. **Professional development:** Maintain organized records of skills, learning activities, and practical experience.
2. **Learning management:** Organize courses and learning resources and record the time spent studying.
3. **Project management:** Plan projects, divide them into phases, and track their execution.
4. **Time tracking:** Record time spent on learning and project activities, including work performed outside the platform.
5. **Freelance management:** Organize services, client projects, invoices, and related expenses.
6. **Financial analysis:** Review revenue, costs, and profit using available financial records.
7. **Data-driven decisions:** Use accumulated records to identify patterns and improve future planning.

These goals describe the intended direction of the project. They do not mean that every feature is already implemented.

## 4. Main Features

The following sections describe the planned functional areas of MyPath.

### 4.1. Skills Management

The skills area is intended to organize technical and professional skills.

Examples include:

- HTML and CSS
- JavaScript
- PHP
- SQL and PostgreSQL
- UI/UX Design
- Database Development
- API Development
- Software Testing

Each skill may include a description, a knowledge or proficiency level, related subskills, and statistics derived from linked learning activities and projects.

Subskills help describe the scope of a skill. They are not intended to become independent skill records with separate project and time statistics unless the design changes.

### 4.2. Courses and Learning

The learning area is intended to help users organize courses and educational resources.

A course record may include:

- Course title and description.
- Learning resource URL.
- Course duration, when known.
- Recorded study time.
- Completion status.
- Related skills and practical projects.
- Certificate information, when available.

Completing a course may also prompt the user to review related skills, update proficiency information, record a certificate, or create a practical project.

### 4.3. Projects and Tasks

The project area is intended to support personal learning projects and real freelance work.

Projects can be divided into phases representing different types of work.

For example, a website project might contain:

1. Requirements and planning.
2. UI/UX design.
3. Database design and implementation.
4. Backend development and API implementation.
5. Frontend development.
6. Testing and quality assurance.
7. Deployment and maintenance.

The exact phases depend on the project. Not every project must follow the same sequence.

Projects may connect to relevant skills, tasks, learning activities, time records, and financial records.

### 4.4. Time Tracking

Time tracking is intended to measure time spent on courses, skills, projects, and individual project phases.

The system is planned to support starting, pausing, resuming, and completing tracked work.

Because some work happens outside the platform, users should also be able to record time spent on activities such as:

- Drawing interface sketches on paper.
- Planning system architecture.
- Studying on external learning websites.
- Writing code in an external editor.
- Researching technical problems.
- Using development and productivity tools.

Recorded time is intended to reflect the user's reported work, not automatically prove that every recorded minute was productive.

### 4.5. Freelance Services and Client Projects

The freelance area is intended to organize services that a user can offer to clients.

Examples include:

- Website development.
- UI/UX design.
- Database development.
- API development.
- Software testing.
- Website maintenance.

Service records may describe the service, its related skills, the user's experience level, estimated delivery time, and pricing.

Client projects may connect to service records, project phases, invoices, expenses, and work hours.

### 4.6. Financial Records and Analysis

The financial area is intended to help users understand the financial performance of their freelance activities.

Relevant records may include:

- Client invoices.
- Revenue and received payments.
- Project-related expenses.
- Hosting and domain costs.
- Payment processing fees, where applicable.
- Outstanding amounts.
- Project costs and profit.

Financial reports may present monthly comparisons, service revenue, expenses, and profit margins.

Financial calculations depend on the accuracy and completeness of the recorded data. MyPath is not intended to replace professional accounting or tax advice.

## 5. How MyPath Works

The intended relationship between the main parts of the platform can be summarized as follows:

1. **Learn:** Add courses and learning resources.
2. **Develop skills:** Connect learning activities and practical work to relevant skills.
3. **Build projects:** Organize work into projects, tasks, and phases.
4. **Track time:** Record time associated with learning and project activities.
5. **Offer services:** Connect professional skills to services offered to clients.
6. **Record financial activity:** Track invoices, revenue, expenses, and payments.
7. **Review results:** Use accumulated data to understand work patterns and financial performance.

For example, completing a backend development phase in a client project can contribute to the project's total recorded hours and the time associated with relevant skills. If the project is paid, its financial records can also contribute to revenue and profitability reports.

This connected approach is one of the central design principles of MyPath.

## 6. Target Users

MyPath is initially being designed for personal use, with the possibility of supporting broader use cases in the future.

Potential users include:

- Students preparing for their first professional role.
- Developers learning new technologies.
- People building portfolios through practical projects.
- Freelancers managing services and client work.
- Independent professionals tracking time and financial performance.

The initial development priority is to create a useful and reliable system for personal use before considering expansion to other users.

## 7. Project Scope

The initial focus is on organizing professional development and freelance work.

### Included in the Intended Scope

- Skills and subskills.
- Courses and learning resources.
- Projects, tasks, and project phases.
- Time tracking and manual time records.
- Freelance services and client projects.
- Invoices and financial records.
- Statistics and reports based on available data.

### Not a Primary Goal of the Initial Version

- A general-purpose social network.
- A marketplace for selling software or digital products.
- A full enterprise resource planning (ERP) system.
- An automatic employee-monitoring or productivity-surveillance tool.
- A replacement for professional accounting software.

Additional features may be considered later if they support the project's main goals.

## 8. Development Approach

MyPath is being developed incrementally.

The development process emphasizes understanding the requirements, documenting design decisions, organizing the system architecture, and implementing features in manageable stages.

The general development workflow is:

1. Define requirements and constraints.
2. Design the system architecture and data model.
3. Plan the user interface and user experience.
4. Implement backend functionality and APIs.
5. Implement the frontend.
6. Test functionality, data integrity, security, and usability.
7. Deploy the application when it is ready.
8. Maintain the system and improve it based on actual use.

The exact implementation order may vary when dependencies or technical decisions require it.

Documentation is part of the development process. It helps keep requirements, architecture decisions, and implementation plans understandable as the project grows.

## 9. Technology Stack

The final technology stack should be documented here after the project's implementation choices are confirmed.

The technology section should distinguish between:

- **Selected technologies:** Confirmed technologies used by the project.
- **Planned technologies:** Technologies intended for future implementation.
- **Under evaluation:** Technologies still being considered.

No technology should be described as implemented merely because it is being studied or planned.

For current technical decisions, refer to the project's architecture and development documentation.

## 10. Project Structure

The repository contains the source code and documentation associated with MyPath.

As development progresses, the repository may include:

- Application source code.
- Database design and migration files.
- API implementation and documentation.
- Frontend components and interface assets.
- Automated and manual testing resources.
- Architecture and requirements documentation.
- Setup and maintenance instructions.

The exact directory structure and setup process should be documented according to the actual implementation.

Files containing private system information, local environment details, or internal notes should not be published unless they have been reviewed and explicitly approved for sharing.

## 11. Current Status

MyPath is under active development.

The project is progressing through requirements analysis, planning, documentation, and technical design before and alongside implementation.

The repository's documentation describes the intended system and its design decisions. Individual features should be considered available only when they have actually been implemented and verified.

As development progresses, this section should be updated to distinguish between:

- Planned features.
- Features currently being developed.
- Implemented features.
- Tested and verified features.
- Known limitations.

No completion percentage or estimated progress should be presented without reliable supporting data.

## 12. Future Development

Future development will depend on the results of implementation and actual personal use.

Potential areas for future improvement include:

- More detailed analytics and reporting.
- Better connections between skills, courses, and projects.
- Improved time-recording and correction workflows.
- More detailed freelance financial analysis.
- Deployment and operational monitoring.
- Support for additional users and appropriate access controls, if the project expands beyond personal use.

These are potential directions rather than commitments or guarantees.

## 13. Security and Privacy

Security and privacy should be considered throughout development.

Important practices include:

- Never commit passwords, API keys, or private credentials.
- Keep environment-specific settings outside version control.
- Validate and authorize API requests.
- Apply appropriate access controls to private information.
- Protect client and financial records.
- Review dependencies and security updates.
- Back up important data and test recovery procedures.
- Review repository contents before publishing changes.

The Git ignore rules help prevent accidental publication of selected local files, but they do not replace security reviews or remove information already committed to Git history.

## 14. License

See the [LICENSE](LICENSE) file for licensing terms.