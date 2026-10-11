# Table of Contents

- [Architecture Principles](#architecture-principles)
  - [1. Purpose](#1-purpose)
  - [2. Current Technology Stack](#2-current-technology-stack)
  - [3. Modular Monolith](#3-modular-monolith)
  - [4. Separation of Responsibilities](#4-separation-of-responsibilities)
    - [4.1 Presentation](#41-presentation)
    - [4.2 API and Request Handling](#42-api-and-request-handling)
    - [4.3 Application and Business Logic](#43-application-and-business-logic)
    - [4.4 Data Access](#44-data-access)
    - [4.5 Infrastructure](#45-infrastructure)
  - [5. Frontend and Backend Communication](#5-frontend-and-backend-communication)
  - [6. Database Principles](#6-database-principles)
  - [7. Data Integrity and Time Tracking](#7-data-integrity-and-time-tracking)
  - [8. Configuration and Security](#8-configuration-and-security)
  - [9. Technology Evolution](#9-technology-evolution)
    - [9.1 Framework Adoption](#91-framework-adoption)
    - [9.2 Migration Rules](#92-migration-rules)
    - [9.3 Compatibility](#93-compatibility)
  - [10. Documentation and Traceability](#10-documentation-and-traceability)
  - [11. Testing and Maintainability](#11-testing-and-maintainability)
  - [12. Architecture Decision Authority](#12-architecture-decision-authority)

# Architecture Principles

## 1. Purpose

This document defines the principles used to design, implement, and maintain MyPath.

These principles guide technical decisions but do not replace detailed system design, database design, or API specifications.

## 2. Current Technology Stack

The initial implementation uses:

- PHP without a framework for backend logic.
- HTML, CSS, and JavaScript for the frontend.
- PostgreSQL as the local database.

The project may adopt Laravel, React, or other technologies in the future.

A technology change must be based on a real need, not only on the availability of a new tool.

## 3. Modular Monolith

The initial system should follow a modular monolith architecture.

This means the application runs as one system but is divided into modules with clear responsibilities.

Potential modules include:

- Learning and Courses.
- Skills.
- Projects and Tasks.
- Work Time Tracking.
- Services and Portfolio.
- Freelance Finance.

The final module boundaries will be confirmed during system design.

Each module should own its main business rules and provide clear ways for other modules to use its functionality.

Modules should not access each other's internal implementation without a clear reason.

Microservices are not required for the initial system.

## 4. Separation of Responsibilities

The system should separate the following responsibilities.

### 4.1 Presentation

Displays information and collects user input.

The frontend should not contain authoritative business rules or connect directly to PostgreSQL.

### 4.2 API and Request Handling

Receives requests, validates input, invokes the required application logic, and returns consistent responses.

The exact API structure will be defined in the API contracts.

### 4.3 Application and Business Logic

Implements the system's operations and business rules.

Examples include completing a course, changing a project phase, and calculating work time.

Business rules should remain independent of page layout whenever practical.

### 4.4 Data Access

Handles database queries and persistence.

Database access should be organized so that queries and database-specific details are not scattered throughout unrelated parts of the application.

### 4.5 Infrastructure

Contains technical support functions such as configuration, logging, and database connection management.

The initial implementation should use only the infrastructure it actually needs.

## 5. Frontend and Backend Communication

The frontend and backend should communicate through defined interfaces.

The initial design may use a REST API with JSON requests and responses.

The API should define:

- Available endpoints.
- Request methods and parameters.
- Input validation rules.
- Response structures.
- Error formats.
- Authentication requirements when applicable.

The frontend must not depend on undocumented backend behavior.

This separation makes it easier to replace or extend the frontend without rewriting all backend business logic.

## 6. Database Principles

PostgreSQL is the initial database.

The database design should follow these principles:

- Give each entity a clear purpose.
- Define relationships explicitly.
- Use appropriate primary keys, foreign keys, and constraints.
- Avoid storing the same authoritative information in multiple places.
- Use database transactions when an operation requires multiple changes to succeed together.
- Use parameterized queries for database operations.
- Track schema changes through migration files.
- Define rules for deleting, updating, and retaining important records.

Derived values should be calculated from reliable source data where practical.

For example, project time totals should be calculated from associated work sessions rather than independently entered in several records.

## 7. Data Integrity and Time Tracking

Work sessions are the primary records for measured work time.

The system should define clear rules for:

- Starting and ending a session.
- Pausing and resuming work.
- Handling interrupted or unfinished sessions.
- Correcting mistaken records.
- Preventing invalid or overlapping sessions where the workflow requires it.
- Assigning a session to the correct activity or project phase.

Time tracking must remain separate from skill evaluation.

The number of recorded hours alone must not automatically determine a user's proficiency level.

## 8. Configuration and Security

Environment-specific settings must be separated from application code.

Examples include database connection settings and other environment-dependent values.

- Real credentials must not be committed to version control.
- `.env.example` must contain placeholders, not real secrets.
- User input must be validated on the server.
- Database queries must use parameterized statements.
- Error responses must not expose credentials or sensitive internal details.
- Personal and financial data must be protected.
- Public access must be explicitly controlled when public features are introduced.

Security requirements must be reviewed again before the application is exposed to a public network.

## 9. Technology Evolution

The system must be able to evolve as the developer learns new technologies.

### 9.1 Framework Adoption

Laravel may replace or reorganize parts of the PHP implementation later.

React may replace parts of the current frontend later.

These changes should be incremental where practical.

### 9.2 Migration Rules

Before introducing a new technology:

1. Identify the problem it solves.
2. Review the affected components and dependencies.
3. Decide whether the current implementation can be maintained or improved more simply.
4. Define a migration approach.
5. Preserve existing functionality and data.
6. Update documentation and tests.

Do not introduce unnecessary abstractions solely to prepare for hypothetical future changes.

### 9.3 Compatibility

When a component is replaced, preserve its existing behavior unless a change is explicitly approved.

Keep API contracts stable where practical. If a breaking change is necessary, document the change and update affected consumers.

## 10. Documentation and Traceability

Important system behavior should be traceable through related documents and code.

- Requirements define what the system must do.
- System design defines how components interact.
- Database design defines the data model and constraints.
- API contracts define communication between components.
- Tests verify expected behavior.
- Architecture decision records explain significant technical decisions.

When an approved change affects these areas, update the relevant documents.

Avoid copying the same authoritative definition into many files.

## 11. Testing and Maintainability

Code should be organized so that important behavior can be tested.

Testing should cover normal cases, invalid inputs, important edge cases, and relevant data integrity rules.

Changes should remain focused and understandable.

Avoid unnecessary dependencies, duplicated business logic, and large files that combine unrelated responsibilities.

A change is not considered verified simply because the code has been written. Relevant tests must be executed and their results reported accurately.

## 12. Architecture Decision Authority

This document defines general principles.

Specific technical choices, approved exceptions, and major architecture changes should be recorded in `docs/09-decisions/`.

If two requirements or decisions conflict, the conflict must be identified and resolved rather than silently choosing one.