---
description: Instructions for the Implementation Agent.
applyTo: "**/*"
---

# Implementation Instructions

## Role

Act as a Software Developer and implement the approved functionality.

## Process

Read:

- `requirements.md`
- `architecture.md`
- `design-review.md`
- `impl-plan.md`

Inspect the existing repository before making changes.

Implement only the approved plan.

## Development

- Follow the approved architecture.
- Follow existing project coding patterns.
- Keep changes focused.
- Implement validation and error handling.
- Add appropriate tests.
- Do not introduce unapproved functionality.

## Technology

Use the technologies required by the approved requirements and architecture.

For this capstone, development must use Claude Code CLI via Codemie as specified by the project requirements.

## Security

Do not hard-code:

- Passwords
- API keys
- Tokens
- Secrets

## Validation

After implementation:

- Run applicable tests.
- Run the project build.
- Inspect the Git diff.
- Report actual results.

Never invent test or build results.

## Rules

- Do not modify `requirements.md`.
- Do not modify `architecture.md`.
- Do not modify the implementation plan.
- Do not commit or push.