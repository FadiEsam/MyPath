# Acceptance Criteria

## Table of Contents

- [1. Purpose](#1-purpose)
- [2. Verification Approach](#2-verification-approach)
- [3. Skills Management](#3-skills-management)
  - [AC-001: Create a Skill](#ac-001-create-a-skill)
  - [AC-002: Associate Evidence with a Skill](#ac-002-associate-evidence-with-a-skill)
- [4. Learning Activities](#4-learning-activities)
  - [AC-003: Record a Course](#ac-003-record-a-course)
  - [AC-004: Complete a Learning Activity](#ac-004-complete-a-learning-activity)
- [5. Projects and Work Phases](#5-projects-and-work-phases)
  - [AC-005: Organize a Project](#ac-005-organize-a-project)
  - [AC-006: Record Project Outcomes](#ac-006-record-project-outcomes)
- [6. Time Tracking](#6-time-tracking)
  - [AC-007: Record a Timed Session](#ac-007-record-a-timed-session)
  - [AC-008: Record Manual Time](#ac-008-record-manual-time)
  - [AC-009: Calculate Time Totals](#ac-009-calculate-time-totals)
- [7. Progress Analysis](#7-progress-analysis)
  - [AC-010: Review Performance](#ac-010-review-performance)
- [8. Quality Requirements](#8-quality-requirements)
  - [AC-011: Validate Data Integrity](#ac-011-validate-data-integrity)
  - [AC-012: Verify Security Practices](#ac-012-verify-security-practices)
  - [AC-013: Verify Maintainability](#ac-013-verify-maintainability)
  - [AC-014: Verify Performance](#ac-014-verify-performance)
- [9. Completion and Review](#9-completion-and-review)

## 1. Purpose

This document defines the conditions used to verify that MyPath requirements have been implemented correctly.

A requirement should not be considered complete merely because its interface or code exists.

## 2. Verification Approach

Use the following verification methods where appropriate:

- **Functional test:** Checks whether a feature behaves as required.
- **Data validation:** Checks whether stored information and calculations are correct.
- **Integration test:** Checks whether connected parts of the system work together.
- **Inspection:** Checks code, configuration, or documentation against a requirement.
- **Performance test:** Measures behavior under defined workload conditions.

Acceptance criteria must be updated when the related requirement changes.

## 3. Skills Management

### AC-001: Create a Skill

Related requirements: FR-001, FR-003.

- A valid skill can be created and saved.
- The saved skill can be found and reviewed.
- Invalid required information is rejected with understandable feedback.
- A skill's recorded proficiency is not automatically increased simply because time was logged.

### AC-002: Associate Evidence with a Skill

Related requirements: FR-004, FR-005.

- A supported learning activity or project can be associated with the relevant skill.
- The association can be reviewed later.
- Missing evidence is not presented as confirmed experience.

## 4. Learning Activities

### AC-003: Record a Course

Related requirements: FR-006, FR-007.

- The user can record a course title.
- A resource link and expected duration can be recorded when available.
- Missing optional information does not prevent saving a valid course.
- Invalid input is handled according to the applicable validation rules.

### AC-004: Complete a Learning Activity

Related requirements: FR-008, FR-009.

- The activity can be marked as completed.
- Its completion status and date are retained.
- Recorded learning outcomes can be reviewed.
- Completing the activity does not automatically create an unsupported skill-level increase.

## 5. Projects and Work Phases

### AC-005: Organize a Project

Related requirements: FR-010, FR-011, FR-013.

- A valid project can be created.
- Work phases can be associated with the project.
- Project information and status can be reviewed.
- A project can contain the general work phases needed to describe its lifecycle.
- The system does not require a separate phase for every individual technology.

### AC-006: Record Project Outcomes

Related requirements: FR-012, FR-014.

- Relevant skills can be associated with project work.
- Completed work and the project outcome can be recorded.
- The project status and recorded outcome remain distinguishable.

## 6. Time Tracking

### AC-007: Record a Timed Session

Related requirements: FR-015, FR-016, FR-017.

- The timer can be started for a supported activity.
- A running timer can be paused and resumed.
- Finishing the session retains its duration.
- Paused time is excluded from active work duration.
- The recorded session is associated with the selected work item.
- Invalid state transitions do not create incorrect time records.

### AC-008: Record Manual Time

Related requirements: FR-018, FR-019.

- The user can record time for work performed outside the timer.
- The manual entry is associated with the relevant work item.
- The system identifies the entry as manually recorded.
- Invalid entries are rejected or returned for correction.

### AC-009: Calculate Time Totals

Related requirements: FR-020, FR-022.

- The total matches the valid underlying time records.
- Relevant filters and reporting periods are applied consistently.
- The same time entry is not counted twice in the same total.
- Missing or invalid data does not silently produce a misleading result.

## 7. Progress Analysis

### AC-010: Review Performance

Related requirements: FR-021, FR-023, FR-024, FR-025.

- The user can review recorded activities and completed work.
- Time totals are derived from recorded time entries.
- Weekly and monthly summaries use clearly defined date ranges.
- Period comparisons use consistent calculation rules.
- Missing data is handled transparently.
- Time spent and completed outcomes are reported as different measurements.

## 8. Quality Requirements

### AC-011: Validate Data Integrity

Related requirements: NFR-004, NFR-006, NFR-007.

- Important inputs are validated.
- Stored records remain consistent with the applicable business rules.
- Important summaries can be checked against their underlying records.

### AC-012: Verify Security Practices

Related requirements: NFR-010, NFR-011, NFR-012.

- Application input is handled using appropriate security practices.
- Database credentials are not exposed in public application files.
- Environment-specific secrets are excluded from version control.
- Relevant validation and security tests pass.

### AC-013: Verify Maintainability

Related requirements: NFR-015, NFR-016, NFR-017.

- Code responsibilities are organized clearly.
- Important calculations and business rules have suitable tests.
- Tests can be repeated and their results reviewed.

### AC-014: Verify Performance

Related requirements: NFR-008, NFR-009.

- Common operations are tested under documented conditions.
- Measured results are compared with the performance targets established for the project.
- Performance is not marked as accepted without recorded evidence.

## 9. Completion and Review

A requirement can be accepted when:

- Its implementation satisfies the related acceptance criteria.
- Relevant tests or inspection results provide sufficient evidence.
- Applicable business rules are respected.
- No unresolved issue prevents the requirement from meeting its intended purpose.
- Related documentation is updated when necessary.

Requirements that have not been implemented or verified must remain identified as incomplete.

Future requirements are not conditions for accepting the initial version unless they are explicitly moved into its agreed scope.
