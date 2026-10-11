\# Table of Contents



\- \[Project Glossary](#project-glossary)

&#x20; - \[1. Purpose](#1-purpose)

&#x20; - \[2. Learning and Skills](#2-learning-and-skills)

&#x20;   - \[Course](#course)

&#x20;   - \[Learning Resource](#learning-resource)

&#x20;   - \[Skill](#skill)

&#x20;   - \[Subskill](#subskill)

&#x20;   - \[Skill Level](#skill-level)

&#x20;   - \[Learning Outcome](#learning-outcome)

&#x20;   - \[Evidence](#evidence)

&#x20; - \[3. Projects and Work Organization](#3-projects-and-work-organization)

&#x20;   - \[Project](#project)

&#x20;   - \[Project Phase](#project-phase)

&#x20;   - \[Task](#task)

&#x20;   - \[Work Session](#work-session)

&#x20;   - \[Recorded Time](#recorded-time)

&#x20;   - \[Estimated Duration](#estimated-duration)

&#x20;   - \[Actual Duration](#actual-duration)

&#x20; - \[4. Freelance and Professional Terms](#4-freelance-and-professional-terms)

&#x20;   - \[Service](#service)

&#x20;   - \[Client](#client)

&#x20;   - \[Portfolio Project](#portfolio-project)

&#x20;   - \[Recruiter View](#recruiter-view)

&#x20; - \[5. Financial Terms](#5-financial-terms)

&#x20;   - \[Invoice](#invoice)

&#x20;   - \[Payment](#payment)

&#x20;   - \[Revenue](#revenue)

&#x20;   - \[Expense](#expense)

&#x20;   - \[Profit](#profit)

&#x20; - \[6. System and Technical Terms](#6-system-and-technical-terms)

&#x20;   - \[Frontend](#frontend)

&#x20;   - \[Backend](#backend)

&#x20;   - \[API](#api)

&#x20;   - \[Database](#database)

&#x20;   - \[Database Migration](#database-migration)

&#x20;   - \[Module](#module)

&#x20;   - \[Modular Monolith](#modular-monolith)

&#x20;   - \[Authentication](#authentication)

&#x20;   - \[Authorization](#authorization)

&#x20; - \[7. General Rules](#7-general-rules)



\#Project Glossary



\## 1. Purpose



This document defines the main terms used in Freelance \& Personal Progress OS.



Use these definitions consistently in documentation, database design, API contracts, and source code.



The glossary defines shared terminology. It does not define database tables, fields, or detailed business rules.



\## 2. Learning and Skills



\### Course



A structured learning resource, such as an online course, training program, or recorded series of lessons.



A course may have a title, provider, URL, estimated duration, completion status, and learning notes.



\### Learning Resource



Any resource used to learn, including courses, tutorials, articles, documentation, and videos.



A learning resource does not have to be a formal course.



\### Skill



A capability or area of knowledge that the user wants to learn, practice, evaluate, or present professionally.



Examples include PHP, JavaScript, PostgreSQL, UI/UX Design, and Software Testing.



\### Subskill



A narrower topic or competency within a broader skill.



A subskill helps describe the scope of knowledge. It does not automatically require independent time tracking or statistics.



If a subskill needs its own projects, records, and independent reporting, it may need to be modeled as a separate skill.



\### Skill Level



An estimate of the user's current proficiency in a skill, based on defined criteria and available evidence.



A skill level is not automatically increased by course completion or time spent.



\### Learning Outcome



Knowledge, an ability, or a result gained from a learning activity.



Examples include understanding a concept, completing an exercise, or building a small application.



\### Evidence



Information that supports a claim about learning or practical ability.



Examples include completed projects, relevant code, demonstrations, certificates, and assessment results.



Evidence does not always guarantee that a skill has been mastered.



\## 3. Projects and Work Organization



\### Project



A defined body of work with a purpose and an expected result.



A project may be created for learning, personal use, portfolio development, or a real client.



\### Project Phase



An ordered stage within a project.



Examples include UI/UX Design, Database Design, Backend Development, Frontend Development, Testing, and Deployment.



A project may have multiple phases, and each phase may involve multiple skills.



\### Task



A specific unit of work that contributes to a learning activity, project, phase, or other goal.



A task describes what needs to be done. It is not the same as a work session, which records time spent working.



\### Work Session



A recorded period of work associated with an activity, task, or project phase.



A session contains time-related information and may include status, notes, or correction details as defined by the system.



Work sessions are the primary source for recorded work-time calculations.



\### Recorded Time



The duration calculated from stored work-session records according to the system's time-tracking rules.



Recorded time is not guaranteed to equal focused or productive time.



\### Estimated Duration



The expected time needed to complete a course, task, phase, project, or service.



An estimate is a planning value, not a record of time already spent.



\### Actual Duration



The duration calculated from relevant recorded sessions or other explicitly defined actual-time records.



Its meaning must be clear for each report and must not be confused with estimated duration.



\## 4. Freelance and Professional Terms



\### Service



A type of professional work that the user offers or plans to offer.



Examples include website development, database design, API development, UI/UX design, and software testing.



A service may be related to one or more skills.



\### Client



A person or organization that requests, receives, or pays for freelance work.



Client records belong to the freelance management scope and are not required for every personal project.



\### Portfolio Project



A project selected to demonstrate skills, practical experience, or professional ability to an external audience.



A portfolio project may be a learning project or a client project, subject to privacy and permission requirements.



\### Recruiter View



A presentation of selected skills, projects, evidence, and relevant experience for people evaluating a candidate's suitability for a role.



It should not automatically expose private learning records or all recorded hours.



\## 5. Financial Terms



\### Invoice



A record describing an amount charged or requested for goods or services.



An invoice is not the same as a confirmed payment.



\### Payment



A record of money received or paid, according to the relevant financial workflow.



Payment status and invoice status must be defined separately when partial payments, refunds, or unpaid invoices are supported.



\### Revenue



Income recognized according to the financial rules adopted by the system.



Revenue must not automatically be treated as cash received.



\### Expense



A recorded cost related to work or operating the freelance activity.



Examples may include hosting, domain renewal, or other project-related costs.



\### Profit



A calculated financial result based on defined revenue and expense rules.



The system must document the formula used for each profit report and must not confuse profit with total revenue or cash balance.



\## 6. System and Technical Terms



\### Frontend



The part of the application responsible for presenting information and receiving user input.



The initial frontend uses HTML, CSS, and JavaScript.



\### Backend



The server-side part of the application responsible for request handling, business logic, and coordination with data storage.



The initial backend uses PHP without a framework.



\### API



An interface that allows application components to exchange requests and responses through defined rules.



The initial design may use a REST API with JSON.



\### Database



An organized system for storing and retrieving application data.



The initial database uses PostgreSQL locally.



\### Database Migration



A versioned change to the database structure, such as creating a table or adding a constraint.



Migrations help track and reproduce database changes.



\### Module



A logical part of the application responsible for a related group of capabilities and business rules.



\### Modular Monolith



An application deployed as one system but organized into modules with clear responsibilities and boundaries.



\### Authentication



The process of verifying a user's identity.



Authentication does not, by itself, determine which data the user may access.



\### Authorization



The process of deciding what an authenticated user or other actor is allowed to do.



\## 7. General Rules



\- Use the same term for the same concept throughout the project.

\- Avoid using one term to describe different concepts.

\- Prefer clear names that explain a record's purpose.

\- Define new domain-specific terms here when they become important.

\- If a term's meaning changes, update this document and review affected documentation and code.

\- Use established technical terms where appropriate, even when explanations are written in simple English.

