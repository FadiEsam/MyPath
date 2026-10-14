# Requirements

## Table of Contents

- [1. Purpose](#1-purpose)
- [2. Documents](#2-documents)
- [3. How to Use These Documents](#3-how-to-use-these-documents)
- [4. Requirements Identification](#4-requirements-identification)
- [5. Completion Conditions](#5-completion-conditions)

## 1. Purpose

This folder documents the requirements of MyPath.

It describes what the system should do, the rules it must follow, how users interact with it, and how its requirements will be verified.

These documents guide system analysis, design, development, and testing.

## 2. Documents

| Document                         | Purpose                                              |
| -------------------------------- | ---------------------------------------------------- |
| `functional-requirements.md`     | Defines the system's required features.              |
| `business-rules.md`              | Defines rules that control system behavior.          |
| `user-flows.md`                  | Describes user interactions step by step.            |
| `non-functional-requirements.md` | Defines quality and technical behavior requirements. |
| `acceptance-criteria.md`         | Defines how requirement completion is verified.      |

## 3. How to Use These Documents

Read the documents in the following order:

1. Functional Requirements
2. Business Rules
3. User Flows
4. Non-Functional Requirements
5. Acceptance Criteria

Use the requirement IDs when referring to a requirement during design, development, or testing.

Do not document database schemas, API endpoints, or detailed interface designs here. Those belong to their appropriate project phases.

## 4. Requirements Identification

Each requirement must have a stable ID.

- `FR`: Functional Requirement
- `BR`: Business Rule
- `UF`: User Flow
- `NFR`: Non-Functional Requirement
- `AC`: Acceptance Criterion

IDs should not be reused for different requirements.

If a requirement changes, update its existing entry when it still represents the same requirement. Add a new ID when a genuinely new requirement is introduced.

## 5. Completion Conditions

This phase is ready for review when:

- The required features are documented.
- Important business rules and user flows are defined.
- Quality requirements are documented and can be evaluated.
- Acceptance criteria cover the agreed requirements.
- Unresolved decisions are clearly identified.
- The documents are consistent with the project foundation.

Completing this phase does not mean the system has been implemented or tested.
