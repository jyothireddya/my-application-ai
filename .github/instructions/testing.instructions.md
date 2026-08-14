---
name: Testing Standards
description: Testing standards for the Automated Documentation Sync project.
applyTo: "**/test*/**"
---

# Testing Standards

## General

Tests must be:

- Deterministic
- Repeatable
- Isolated
- Easy to understand

## Required Coverage

Where applicable, tests must cover:

- Happy path
- Invalid input
- Empty input
- Missing files
- Not Found
- Missing fields
- API failures
- Network failures
- Permission failures
- Duplicate data
- Other relevant edge cases

## Test Structure

Prefer:

1. Arrange
2. Act
3. Assert

## Test Naming

Test names must clearly describe:

- The scenario
- The expected behavior

Example:

```text
should_return_not_found_when_document_does_not_exist