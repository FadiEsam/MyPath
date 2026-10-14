# Business Rules

# Table of Contents

- [1. Purpose](#1-purpose)
- [2. Skills](#2-skills)
  - [BR-001: Skills Are Independent Records](#br-001-skills-are-independent-records)
  - [BR-002: Subskills Do Not Require Independent Time Tracking](#br-002-subskills-do-not-require-independent-time-tracking)
  - [BR-003: Skill Evidence](#br-003-skill-evidence)
- [3. Learning Activities](#3-learning-activities)
  - [BR-004: Activities Have a Defined Type](#br-004-activities-have-a-defined-type)
  - [BR-005: Course Completion](#br-005-course-completion)
  - [BR-006: Learning Resource Links](#br-006-learning-resource-links)
- [4. Projects and Work Phases](#4-projects-and-work-phases)
  - [BR-007: Projects Contain Organized Work](#br-007-projects-contain-organized-work)
  - [BR-008: Work Phases Represent General Areas of Work](#br-008-work-phases-represent-general-areas-of-work)
  - [BR-009: Completion Must Reflect Actual Work](#br-009-completion-must-reflect-actual-work)
- [5. Time Tracking](#5-time-tracking)
  - [BR-010: Time Must Have a Meaningful Context](#br-010-time-must-have-a-meaningful-context)
  - [BR-011: Timer States Must Be Clear](#br-011-timer-states-must-be-clear)
  - [BR-012: Manual Time Entries](#br-012-manual-time-entries)
  - [BR-013: Avoid Double Counting](#br-013-avoid-double-counting)
  - [BR-014: External Work Can Be Recorded](#br-014-external-work-can-be-recorded)
- [6. Progress Analysis](#6-progress-analysis)
  - [BR-015: Use Recorded Data](#br-015-use-recorded-data)
  - [BR-016: Missing Data Must Remain Visible](#br-016-missing-data-must-remain-visible)
  - [BR-017: Time and Achievement Are Different](#br-017-time-and-achievement-are-different)
  - [BR-018: Comparisons Must Use Consistent Periods](#br-018-comparisons-must-use-consistent-periods)
- [7. Financial Records](#7-financial-records)
  - [BR-019: Income and Expenses Must Be Distinguished](#br-019-income-and-expenses-must-be-distinguished)
  - [BR-020: Profit Uses Recorded Financial Data](#br-020-profit-uses-recorded-financial-data)
  - [BR-021: Hosting and Other Business Costs](#br-021-hosting-and-other-business-costs)
- [8. Data Integrity](#8-data-integrity)
  - [BR-022: Preserve Meaningful History](#br-022-preserve-meaningful-history)
  - [BR-023: Derived Values Must Be Consistent](#br-023-derived-values-must-be-consistent)
- [9. Rules Requiring Further Decisions](#9-rules-requiring-further-decisions)

## 1. Purpose

This document defines the rules that govern MyPath's behavior.

Functional requirements describe what the system does. Business rules define the conditions and restrictions that those functions must follow.

## 2. Skills

### BR-001: Skills Are Independent Records

A skill represents a knowledge or competency area that can be used across multiple activities and projects.

### BR-002: Subskills Do Not Require Independent Time Tracking

Subskills may describe parts of a broader skill or help explain its proficiency level.

They do not automatically become separate projects or independent time-tracking categories.

### BR-003: Skill Evidence

A course, task, or project may provide evidence of learning or practice for one or more skills.

Recording an activity does not automatically prove that the user's proficiency has increased.

## 3. Learning Activities

### BR-004: Activities Have a Defined Type

Each learning activity must have a type and an expected output appropriate to that type.

Examples include a course, a practice task, and a learning exercise.

### BR-005: Course Completion

Completing a course and improving a skill are separate outcomes.

A completed course may lead to a skill update, certificate record, or practice task, but these outcomes should not be assumed to have occurred automatically.

### BR-006: Learning Resource Links

A learning activity may refer to an external resource, including a website or video platform.

The existence of a link does not mean MyPath can verify the user's activity on that external service.

## 4. Projects and Work Phases

### BR-007: Projects Contain Organized Work

A project may contain multiple work phases, and each phase may contain related activities.

The project structure should reflect meaningful work rather than create unnecessary organizational levels.

### BR-008: Work Phases Represent General Areas of Work

Phases should support meaningful analysis, such as UI/UX, Database, Backend, Frontend, and Testing.

Individual technologies such as HTML, CSS, and JavaScript may be associated with the relevant work without requiring a separate project phase for each technology.

### BR-009: Completion Must Reflect Actual Work

A project or task must not be treated as completed merely because time was recorded.

Completion depends on the relevant work outcome and its applicable completion criteria.

## 5. Time Tracking

### BR-010: Time Must Have a Meaningful Context

Recorded time must be associated with an identifiable activity or work item.

Where applicable, the record should also be associated with its project, phase, and skill.

### BR-011: Timer States Must Be Clear

A timing session must distinguish between its applicable states, such as active, paused, and finished.

The system must not count paused time as active work time.

### BR-012: Manual Time Entries

Manually entered time must be distinguishable from time captured by the timer.

This helps the user understand how each duration was recorded.

### BR-013: Avoid Double Counting

The same period of work must not be counted twice in the same total.

The detailed rules for overlapping sessions, corrections, and duplicate entries must be finalized before implementation.

### BR-014: External Work Can Be Recorded

Work performed outside MyPath, including learning, planning, and coding in external tools, may be recorded manually.

MyPath must not assume that it can automatically observe all such activity.

## 6. Progress Analysis

### BR-015: Use Recorded Data

Performance summaries must be calculated from available records.

### BR-016: Missing Data Must Remain Visible

When information required for a calculation is missing, the system must not silently invent a value.

### BR-017: Time and Achievement Are Different

Time spent, completed work, and skill proficiency are separate measurements.

A larger number of hours does not automatically mean better performance or a higher skill level.

### BR-018: Comparisons Must Use Consistent Periods

Weekly and monthly comparisons must use clearly defined date ranges and consistent calculation rules.

## 7. Financial Records

### BR-019: Income and Expenses Must Be Distinguished

Income, received payments, outstanding amounts, and expenses represent different financial concepts.

They must not be treated as interchangeable values.

### BR-020: Profit Uses Recorded Financial Data

Profit summaries must use the applicable recorded income and expenses.

The system must not present revenue as profit.

### BR-021: Hosting and Other Business Costs

Hosting and other relevant service costs may be recorded as expenses and associated with the appropriate client, service, or project when applicable.

These rules apply when financial tracking is introduced.

## 8. Data Integrity

### BR-022: Preserve Meaningful History

Changes to records should not silently invalidate historical time or performance summaries.

The handling of edited, archived, or deleted records must be defined before implementing the relevant operations.

### BR-023: Derived Values Must Be Consistent

Totals and summaries should be derived from the underlying records using consistent calculation rules.

The same data should not produce conflicting totals in different views.

## 9. Rules Requiring Further Decisions

The following details require explicit decisions before the related functions are implemented:

- Whether multiple timers may run at the same time.
- How overlapping manual and timed entries are handled.
- How users correct or remove time records.
- Whether unfinished timing sessions survive a browser restart.
- How archived or deleted activities affect historical reports.
- How proficiency levels are defined and when they may change.
- How invoices, partial payments, refunds, and expenses affect financial summaries.

Do not treat these unresolved details as finalized business rules.
