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
      -[9.2.1 Recommended Migration Workflow](#921-recommended-migration-workflow)
      -[9.2.2 One Technology Change at a Time](#922-one-technology-change-at-a-time)
      -[9.2.3 Migration Principles](#923-migration-principles)
  - [10. Documentation and Traceability](#10-documentation-and-traceability)
  - [11. Testing and Maintainability](#11-testing-and-maintainability)

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

Technology migrations must be performed incrementally, with a clear separation between the current stable version and the new version under development. The goal is to simplify troubleshooting, preserve existing functionality, and reduce the risk of breaking the entire system.

Before introducing a new technology:

1. **Identify the reason for migration.** Explain the problem the new technology solves and why improving the existing implementation is insufficient or less suitable.
2. **Review the affected components.** Identify dependencies, related modules, existing functionality, database interactions, and potential compatibility issues.
3. **Define the migration scope.** Specify the components that will change, the expected results, and the tests required to verify the migration.
4. **Preserve the current stable version.** Save a reliable version of the project before making changes. Use Git branches, tags, or another suitable version-control method to ensure that the previous version remains recoverable.
5. **Create a separate version for the migration.** Develop and test the new technology in an isolated branch or environment without modifying the stable version directly.
6. **Implement the migration incrementally.** Change only the components required for the selected technology and preserve existing behavior wherever possible.
7. **Test and troubleshoot.** Compare the new implementation against the stable version, identify regressions, and resolve problems using the known-working implementation as a reference.
8. **Verify the complete system.** Run the required tests and confirm that all affected features, integrations, database operations, and existing workflows continue to work correctly.
9. **Adopt the new version.** Once the migration passes the required checks, designate the new version as the stable version and update the project documentation.
10. **Remove obsolete versions only when appropriate.** Delete old branches, temporary environments, or duplicate files only when they are no longer needed, the new version is stable, and the previous version remains recoverable through version control or backups.

#### 9.2.1 Recommended Migration Workflow

The standard migration process follows these steps:

1. **Stable Version (v1):** Preserve the last known-working version before starting the migration.
2. **New Version (v2):** Create a separate development branch or environment based on v1.
3. **Migration:** Implement the selected technology change in v2 while keeping v1 unchanged.
4. **Comparison and Troubleshooting:** Test v2 against v1 to identify unexpected behavior. Use v1 as a reference when investigating and resolving problems.
5. **System Validation:** Verify that the complete application works correctly, including existing functionality and any affected integrations.
6. **Version Adoption:** Promote v2 to the new stable version only after all required checks pass.
7. **Cleanup:** Remove obsolete development branches or temporary files if they are no longer useful. Keep an appropriate recovery point for the previous stable version.

If validation fails, v1 remains the reliable reference, and the migration continues in v2 until the issues are resolved. If necessary, development can return to v1 while the migration is reviewed or corrected.

#### 9.2.2 One Technology Change at a Time

**Only one major technology migration should be performed at a time.** Do not combine independent technology migrations into a single change.

For example, do not migrate the backend from PHP to Laravel while simultaneously replacing the frontend built with HTML, CSS, and JavaScript with React.

Instead, follow a separate migration process for each change:

- **Migration A:** Introduce Laravel while keeping the existing frontend technologies unchanged. Test the backend migration and confirm that the application continues to work correctly.
- **Migration B:** After Laravel is stable, consider migrating the frontend to React in a separate version and repeat the migration workflow.

This separation makes it easier to identify the source of errors, isolate compatibility issues, compare implementations, and roll back individual changes without unnecessarily affecting unrelated components.

A technology migration should not begin until the previous migration has been validated and accepted as stable.

#### 9.2.3 Migration Principles

- Preserve a recoverable, known-working version before every migration.
- Keep the stable version separate from the version under development.
- Make small, traceable changes with clearly defined scopes.
- Preserve existing functionality, data integrity, and application behavior.
- Use the previous stable implementation as a reference when troubleshooting.
- Validate each migration before beginning another major technology change.
- Update architecture documentation, dependencies, configuration, and tests to reflect the new implementation.
- Avoid unnecessary abstractions or technology changes that do not provide a clear benefit.

The objective is not to prevent future technology changes, but to make each change controlled, testable, reversible, and independently verifiable.

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

