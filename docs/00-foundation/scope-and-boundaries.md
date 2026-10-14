# Table of Contents

- [Scope and Boundaries](#scope-and-boundaries)
  - [1. Purpose](#1-purpose)
  - [2. Initial Scope](#2-initial-scope)
    - [2.1 Learning Management](#21-learning-management)
    - [2.2 Skills Management](#22-skills-management)
    - [2.3 Project Management](#23-project-management)
    - [2.4 Work Time Tracking](#24-work-time-tracking)
    - [2.5 Personal Reports](#25-personal-reports)
  - [3. Future Scope](#3-future-scope)
    - [3.1 Freelance Management](#31-freelance-management)
    - [3.2 Portfolio and Public Views](#32-portfolio-and-public-views)
    - [3.3 Client View](#33-client-view)
    - [3.4 Recruiter View](#34-recruiter-view)
    - [3.5 Multi-User Access](#35-multi-user-access)
  - [4. Out of Scope for the Initial Version](#4-out-of-scope-for-the-initial-version)
  - [5. System Boundaries](#5-system-boundaries)
    - [5.1 External Tools](#51-external-tools)
    - [5.2 Time and Productivity](#52-time-and-productivity)
    - [5.3 Skill Evaluation](#53-skill-evaluation)
    - [5.4 Financial Information](#54-financial-information)
    - [5.5 Future Audiences](#55-future-audiences)
  - [6. Scope Changes](#6-scope-changes)
  - [7. Document Ownership](#7-document-ownership)

---

# Scope and Boundaries

## 1. Purpose

This document defines the scope of MyPath.

It separates the initial personal system from future capabilities and identifies areas that are not part of the current scope.

Detailed requirements and acceptance criteria will be defined in the requirements phase.

## 2. Initial Scope

The initial system focuses on personal use on a local computer.

### 2.1 Learning Management

The system is intended to support:

- Recording courses and learning resources.
- Saving course links and available duration information.
- Tracking course status and completion.
- Recording time spent learning.
- Recording learning outcomes and related skills.

### 2.2 Skills Management

The system is intended to support:

- Maintaining a list of skills.
- Recording skill descriptions and proficiency levels.
- Organizing related knowledge or subskills.
- Connecting skills to relevant courses and practical projects.
- Reviewing practical evidence of skill development.

A course completion or a recorded number of hours does not automatically prove a higher skill level.

### 2.3 Project Management

The system is intended to support:

- Creating and managing projects.
- Dividing projects into ordered phases.
- Organizing tasks and work activities.
- Connecting project phases to relevant skills.
- Tracking project status and progress.
- Recording project-related learning and practical outcomes.

### 2.4 Work Time Tracking

The system is intended to support:

- Starting, pausing, resuming, and ending work sessions.
- Recording time against the appropriate activity or project phase.
- Recording work performed outside the platform.
- Reviewing recorded sessions and correcting mistakes under defined rules.
- Calculating time totals from stored work sessions.

The system should distinguish recorded time from verified productivity. A timer alone cannot prove that work was performed accurately or continuously.

### 2.5 Personal Reports

The system may provide summaries based on available data, such as:

- Time spent on courses, skills, and projects.
- Project and phase time totals.
- Learning activity history.
- Recorded skill development evidence.

Reports must use actual recorded data and explain important limitations. The system must not invent performance scores or reliable industry benchmarks without sufficient evidence.

## 3. Future Scope

The following capabilities may be introduced after the initial system becomes useful and stable.

### 3.1 Freelance Management

- Service definitions, descriptions, prices, and estimated durations.
- Client records and project agreements.
- Invoices and payment records.
- Project income and expenses.
- Hosting and other service costs.
- Profit and financial summaries.

Financial reports must use clearly defined formulas and distinguish revenue, received payments, expenses, and profit.

### 3.2 Portfolio and Public Views

- Public presentation of selected skills.
- Selected projects and practical evidence.
- Certificates and achievements.
- Service descriptions and contact information.

Private records must not become public by default.

### 3.3 Client View

- Viewing available services and relevant projects.
- Reviewing service descriptions and estimated delivery times.
- Submitting service requests.
- Following project information that the owner has chosen to share.

### 3.4 Recruiter View

- Viewing selected skills and proficiency information.
- Reviewing relevant projects and experience.
- Viewing selected evidence and achievements.
- Presenting relevant work history where appropriate.

Recorded personal study time must not automatically be presented as professional employment experience.

### 3.5 Multi-User Access

If the platform becomes a public service, it may require:

- User registration and authentication.
- Roles and permissions.
- Data ownership and access rules.
- Secure account and session management.
- Protection against access to other users' private records.

These requirements must be designed before public multi-user access is implemented.

## 4. Out of Scope for the Initial Version

The following are not required for the initial personal version:

- Public user registration.
- Multi-user collaboration.
- Client and recruiter accounts.
- Online payment processing.
- Automatic bank transaction synchronization.
- Automatic proof of user activity or productivity.
- Artificial intelligence features that evaluate skills or judge project quality.
- Native mobile applications.
- Microservices architecture.
- Mandatory use of Laravel, React, or another unlearned framework.

These exclusions do not prevent reconsidering a feature later through an explicit scope change.

## 5. System Boundaries

### 5.1 External Tools

Courses, code editors, design tools, and other external applications remain independent systems.

The platform may store links, notes, and manually recorded activities related to those tools. It does not assume that it can automatically access or verify their data.

### 5.2 Time and Productivity

The platform records work sessions and calculates time from stored records.

It does not guarantee that recorded time equals focused work time, nor does it treat time spent as direct proof of skill.

### 5.3 Skill Evaluation

Skill levels are estimates based on defined criteria and available evidence. They are not official certifications unless supported by a genuine external credential.

### 5.4 Financial Information

Financial summaries are based on the transactions and costs entered into the system. They are not automatically verified accounting records or legal and tax advice.

### 5.5 Future Audiences

Client, recruiter, and public views are separate presentation and access concerns. They must not be allowed to expose all personal workspace data.

## 6. Scope Changes

New capabilities may be added when they provide clear value.

Before a significant change is accepted:

1. Describe the problem it solves.
2. Identify the affected requirements and modules.
3. Review its effects on existing data and workflows.
4. Identify security, privacy, and maintenance implications.
5. Update the relevant documentation and decision records.

A future idea does not become an implementation requirement until it is explicitly approved.

## 7. Document Ownership

This document defines scope and boundaries.

Detailed behavior belongs in the requirements documents. Technical implementation decisions belong in system design and architecture decision records.
