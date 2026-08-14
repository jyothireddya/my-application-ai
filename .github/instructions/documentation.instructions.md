---
name: Documentation Standards
description: Standards for all SDLC and project documentation.
applyTo: "**/*.md"
---

# Documentation Standards

## General Rules

All Markdown documentation must be:

- Clear
- Accurate
- Consistent
- Easy to understand
- Traceable to approved requirements

Do not invent information.

If required information is unavailable, explicitly use:

`Not Found`

## SDLC Documentation

### requirements.md

Requirements must trace back to the User Story.

Functional requirements must have unique IDs such as:

- FR-001
- FR-002

Non-functional requirements must have unique IDs such as:

- NFR-001
- NFR-002

### architecture.md

Architecture must be based on approved requirements.

Document:

- Components
- Responsibilities
- Data flow
- Technology choices
- Security
- Error handling
- External integrations

### design-review.md

Design review must document:

- Findings
- Risks
- Severity
- Recommendations
- Decisions
- Open questions

### impl-plan.md

Implementation tasks must be:

- Prioritized
- Dependency ordered
- Testable

### code-review.md

Code review must document:

- Correctness
- Security
- Error handling
- Test coverage
- Code clarity
- DRY
- Dependency safety

### verification-report.md

Verification must contain evidence for:

- Build
- Unit tests
- Integration tests
- Requirements coverage
- Edge cases
- Documentation quality
- Security checks

## Documentation Synchronization

Documentation must reflect the actual implementation.

Do not claim functionality exists unless it is implemented and verified.

When implementation changes affect documentation, identify and update the
affected documentation.

## Markdown Quality

Use:

- Meaningful headings
- Tables where useful
- Bullet lists for collections
- Code blocks for commands and code
- Consistent terminology

Avoid unnecessary duplication.