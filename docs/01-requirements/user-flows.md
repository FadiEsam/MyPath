# User Flows

## Table of Contents

- [1. Purpose](#1-purpose)
- [2. Create and Update a Skill](#2-create-and-update-a-skill)
- [3. Record a Learning Activity](#3-record-a-learning-activity)
- [4. Complete a Course](#4-complete-a-course)
- [5. Create and Organize a Project](#5-create-and-organize-a-project)
- [6. Track Work Time](#6-track-work-time)
- [7. Record External Work](#7-record-external-work)
- [8. Review Performance](#8-review-performance)
- [9. Review a Skill's Evidence](#9-review-a-skills-evidence)
- [10. Future Freelance Workflow](#10-future-freelance-workflow)

## 1. Purpose

This document describes how a user completes common tasks in MyPath.

Each flow identifies the starting point, main steps, expected result, and important alternative outcomes.

These flows describe behavior, not screen layouts.

## 2. Create and Update a Skill

**Related requirements:** FR-001, FR-002, FR-003.

1. The user opens skill management.
2. The user chooses to create a skill.
3. The user enters its name and relevant information.
4. The user records an initial proficiency level if known.
5. The user saves the skill.
6. The system validates the required information.
7. The skill becomes available for association with relevant activities.

**Alternative flow:**

- If required information is invalid, the system explains the problem and allows the user to correct it.

**Expected result:** A valid skill record is available for future learning and work.

## 3. Record a Learning Activity

**Related requirements:** FR-006, FR-007, FR-008.

1. The user chooses to create a learning activity.
2. The user selects the activity type.
3. The user enters its title and relevant details.
4. For a course, the user may provide a resource link and expected duration.
5. The user associates relevant skills when appropriate.
6. The user defines the expected outcome.
7. The system validates and saves the activity.

**Expected result:** The learning activity can be tracked and reviewed.

## 4. Complete a Course

**Related requirements:** FR-008, FR-009.

1. The user opens a learning activity.
2. The user reviews the recorded course information.
3. The user marks the course as completed.
4. The system records the completion status and date.
5. The user records relevant outcomes, such as a certificate, new knowledge, or a practice task.
6. The user may update a related skill if the learning outcome justifies the change.

**Expected result:** The completed course and its documented outcomes are available for later review.

## 5. Create and Organize a Project

**Related requirements:** FR-010, FR-011, FR-012, FR-013.

1. The user creates a project.
2. The user records the project title and description.
3. The user identifies its intended outcome.
4. The user organizes the work into meaningful phases.
5. The user associates relevant skills with the project or its phases.
6. The user updates the project status as work progresses.
7. The user records completed work and the final outcome.

**Expected result:** The project has a clear structure and can be analyzed using its work and time records.

## 6. Track Work Time

**Related requirements:** FR-015, FR-016, FR-017, FR-019.

1. The user selects a supported activity or work item.
2. The user starts the timer.
3. The user works on the selected activity.
4. The user pauses the timer when work temporarily stops, if needed.
5. The user resumes the timer when work continues.
6. The user finishes the session.
7. The system retains the recorded duration and its work context.

**Alternative flows:**

- If the user pauses the timer, paused time is excluded from active work duration.
- If the user attempts an invalid action, the system must preserve data integrity and explain the available next step.
- If a timing session is interrupted unexpectedly, recovery behavior follows the rule defined for session persistence.

**Expected result:** A timing record is associated with the relevant work item.

## 7. Record External Work

**Related requirements:** FR-018, FR-019.

1. The user chooses to add a manual time entry.
2. The user selects the relevant activity or work item.
3. The user enters the time information required by the system.
4. The user confirms the entry.
5. The system validates the entry and stores its source as manual.

**Expected result:** External or offline work can contribute to time summaries without pretending that it was captured automatically.

## 8. Review Performance

**Related requirements:** FR-021, FR-022, FR-023, FR-024, FR-025.

1. The user opens the performance view.
2. The user selects a reporting period.
3. The user selects an available category, such as skills, projects, or learning activities.
4. The system summarizes the relevant recorded data.
5. The user reviews time spent and completed work.
6. The user compares periods when the necessary data is available.
7. The system indicates missing information where it affects a result.

**Expected result:** The user can evaluate progress using actual recorded activity and outcomes.

## 9. Review a Skill's Evidence

**Related requirements:** FR-004, FR-005.

1. The user opens a skill.
2. The system displays its recorded proficiency information.
3. The system lists associated courses, tasks, and projects where available.
4. The user reviews the evidence of learning and practice.
5. The user updates the skill information if justified.

**Expected result:** The user can review a skill together with relevant learning and practice evidence.

## 10. Future Freelance Workflow

**Related requirements:** FR-029, FR-030, FR-031, FR-032, FR-033.

This workflow is planned for a later phase.

1. The user records a client and related work.
2. The user records an invoice when applicable.
3. The user records payments received.
4. The user records relevant expenses, such as hosting costs.
5. The system calculates applicable financial summaries.
6. The user reviews income, expenses, outstanding amounts, and profit for a selected period.

**Expected result:** Freelance work and financial performance can be reviewed using recorded financial data.

The detailed workflow depends on the financial business rules being finalized before implementation.
