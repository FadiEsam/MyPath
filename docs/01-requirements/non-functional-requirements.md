# Non-Functional Requirements

## Table of Contents

# Table of Contents

- [1. Purpose](#1-purpose)
- [2. Usability](#2-usability)
  - [NFR-001: Clear Navigation](#nfr-001-clear-navigation)
  - [NFR-002: Consistent Terminology](#nfr-002-consistent-terminology)
  - [NFR-003: Understandable Feedback](#nfr-003-understandable-feedback)
- [3. Data Accuracy and Integrity](#3-data-accuracy-and-integrity)
  - [NFR-004: Accurate Time Calculations](#nfr-004-accurate-time-calculations)
  - [NFR-005: Consistent Financial Calculations](#nfr-005-consistent-financial-calculations)
  - [NFR-006: Valid Data](#nfr-006-valid-data)
  - [NFR-007: Traceable Results](#nfr-007-traceable-results)
- [4. Performance](#4-performance)
  - [NFR-008: Responsive Common Operations](#nfr-008-responsive-common-operations)
  - [NFR-009: Efficient Data Retrieval](#nfr-009-efficient-data-retrieval)
- [5. Security and Privacy](#5-security-and-privacy)
  - [NFR-010: Safe Input Handling](#nfr-010-safe-input-handling)
  - [NFR-011: Secure Database Access](#nfr-011-secure-database-access)
  - [NFR-012: Sensitive Configuration](#nfr-012-sensitive-configuration)
  - [NFR-013: Personal Data Protection](#nfr-013-personal-data-protection)
  - [NFR-014: Future Access Control](#nfr-014-future-access-control)
- [6. Maintainability](#6-maintainability)
  - [NFR-015: Organized Code](#nfr-015-organized-code)
  - [NFR-016: Documented Business Logic](#nfr-016-documented-business-logic)
  - [NFR-017: Automated Verification](#nfr-017-automated-verification)
- [7. Extensibility](#7-extensibility)
  - [NFR-018: Technology Evolution](#nfr-018-technology-evolution)
  - [NFR-019: Future Features](#nfr-019-future-features)
- [8. Reliability and Recovery](#8-reliability-and-recovery)
  - [NFR-020: Preserve Confirmed Records](#nfr-020-preserve-confirmed-records)
  - [NFR-021: Handle Failures Clearly](#nfr-021-handle-failures-clearly)
  - [NFR-022: Data Recovery](#nfr-022-data-recovery)
- [9. Testability](#9-testability)
  - [NFR-023: Verifiable Requirements](#nfr-023-verifiable-requirements)
  - [NFR-024: Repeatable Tests](#nfr-024-repeatable-tests)
- [10. Requirements to Measure Later](#10-requirements-to-measure-later)

## 1. Purpose

This document defines the quality attributes MyPath should maintain.

These requirements guide system design, development, and testing.

## 2. Usability

### NFR-001: Clear Navigation

The system shall organize its functions and information so the user can identify where to perform common tasks.

### NFR-002: Consistent Terminology

The system shall use consistent names for skills, activities, projects, phases, time records, and financial records.

### NFR-003: Understandable Feedback

The system shall provide clear feedback when an operation succeeds, fails, or requires additional information.

## 3. Data Accuracy and Integrity

### NFR-004: Accurate Time Calculations

Time totals shall be calculated consistently from valid recorded time entries.

### NFR-005: Consistent Financial Calculations

Financial totals shall follow documented business rules and use consistent currency and rounding rules.

### NFR-006: Valid Data

The system shall validate input data and prevent invalid operations from creating inconsistent records.

### NFR-007: Traceable Results

Where practical, summaries shall be traceable to the records used to calculate them.

## 4. Performance

### NFR-008: Responsive Common Operations

Common operations, such as opening a record, saving an activity, and viewing a summary, should complete within an acceptable time under the expected workload.

The target response times and test conditions must be defined before performance testing.

### NFR-009: Efficient Data Retrieval

The system should retrieve and summarize data without unnecessarily loading unrelated records.

## 5. Security and Privacy

### NFR-010: Safe Input Handling

The system shall validate and safely handle user input to reduce common application security risks.

### NFR-011: Secure Database Access

Database access shall use appropriate controls and shall not expose database credentials through public application files.

### NFR-012: Sensitive Configuration

Secrets and environment-specific configuration shall not be committed as exposed credentials in the repository.

### NFR-013: Personal Data Protection

The system shall avoid collecting personal information that is not required for its intended functions.

### NFR-014: Future Access Control

If multiple user accounts are introduced, the system shall enforce appropriate authentication, authorization, and data separation before those accounts are used.

## 6. Maintainability

### NFR-015: Organized Code

The implementation shall use a clear structure that separates responsibilities and avoids unnecessary duplication.

### NFR-016: Documented Business Logic

Important calculation rules and non-obvious business behavior shall be documented and testable.

### NFR-017: Automated Verification

Important business rules and calculations should have automated tests where practical.

## 7. Extensibility

### NFR-018: Technology Evolution

The architecture should allow future technology changes without requiring unnecessary changes to unrelated business logic.

### NFR-019: Future Features

The system should be organized so that future capabilities, such as user accounts, public portfolio views, and client-facing features, can be evaluated and added without avoidable architectural coupling.

This requirement does not mean that future features must be implemented in the initial version.

## 8. Reliability and Recovery

### NFR-020: Preserve Confirmed Records

Successful data changes shall be stored reliably and shall not be silently lost during normal operation.

### NFR-021: Handle Failures Clearly

The system shall handle expected errors without exposing internal secrets or misleading the user about whether an operation succeeded.

### NFR-022: Data Recovery

A suitable backup and recovery approach must be defined before MyPath stores important real-world data that cannot easily be recreated.

## 9. Testability

### NFR-023: Verifiable Requirements

Requirements shall be written so their implementation can be checked through inspection, tests, or observable system behavior.

### NFR-024: Repeatable Tests

Tests for important calculations and business rules should produce consistent results under the same conditions.

## 10. Requirements to Measure Later

The following targets require measurement or a documented decision before they can be considered finalized:

- Maximum acceptable response time for common operations.
- Expected number of records and concurrent users.
- Browser compatibility requirements.
- Backup frequency and recovery objectives.
- Accessibility and responsive layout targets.
- Data retention and deletion policies.

Do not claim that a quality target has been met without suitable verification.
