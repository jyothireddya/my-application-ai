# PR Title

Implement dependency-free local login flow with verification evidence

# Summary

This change provides the documented local-demo login flow: users can enter credentials, submit Login, receive a generic invalid-credential error, and access a protected local account page after valid credentials. The implementation and verification evidence support FR-001 through FR-004 within the local-demo scope; this PR content is prepared and awaiting human approval.

# Changes Made

The workspace is not a Git working tree, so an authoritative changed-file list cannot be produced from Git status or diff (`Not Found`). The following files are the implementation, test, and scope/documentation files identified by the reviewed SDLC evidence:

- `server.js` - Implements the dependency-free HTTP login flow, credential-validation boundary, local sessions, protected account access, logout, controlled error responses, and security-related local-demo behavior.
- `test/server.test.js` - Verifies the login form, valid and invalid credentials, account protection, logout, input and request edge cases, session behavior, and cookie attributes.
- `package.json` - Defines the Node.js runtime metadata and the available `npm.cmd test` and `npm.cmd start` scripts.
- `LOCAL-DEMO.md` - Documents local-demo limitations, including environment-provided credentials, process-local sessions, HTTP by default, and production features outside scope.
- `requirements.md` - Records the approved user-story requirements, traceability, acceptance criteria, and unresolved requirements.
- `architecture.md` - Records the implementation-neutral login boundaries, data flow, security constraints, and deferred architecture decisions.
- `design-review.md` - Records design findings, conditions, approved baseline decisions, and production blockers.
- `impl-plan.md` - Records the gated implementation sequence, testing strategy, and definition of done.
- `code-review.md` - Records correctness, security, error-handling, test-coverage, and dependency-safety review results for the local demo.
- `verification-report.md` - Records Phase 7 test, syntax, security, requirements, and limitation evidence.
- `pull-request.md` - Contains this Phase 8 PR preparation content and reviewer checklist; it is awaiting human approval.

# Test Evidence

- `npm.cmd test` - PASS: 10 tests passed, 0 failed, 0 skipped, 0 cancelled.
- `node --check server.js` - PASS.
- `node --check test/server.test.js` - PASS.
- `npm.cmd run build` - NOT AVAILABLE: no `build` script is declared.
- `npm.cmd audit --omit=dev` - NOT AVAILABLE: no lockfile exists (`ENOLOCK`).
- No separate integration-test suite is provided; the available HTTP tests exercise the running local server over loopback and passed.
- Git status and diff evidence - NOT AVAILABLE: this workspace is not a Git working tree.

# Known Limitations

- This is a local demonstration, not production authentication.
- Credentials are supplied through `LOGIN_EMAIL` and `LOGIN_PASSWORD` or test-only options; no external provider, production credential store, or secret-management design is present.
- Sessions are process-local in-memory records and are not durable, distributed, or independently revocable after process termination.
- The default server uses HTTP; HTTPS enforcement and production transport policy are out of scope.
- Account access is represented by a hard-coded local account page; durable identity, authorization, destination, and account capabilities are not defined.
- CSRF policy, rate limiting, lockout, MFA, recovery, account-state handling, provider/network failures, audit requirements, and other unresolved security or non-functional requirements are out of scope or `Not Found` pending approval.
- No lockfile-based dependency audit, Git history review, or Git diff review is available in this workspace.

# Reviewer Checklist

- [ ] Requirements satisfied
- [ ] Architecture reviewed
- [ ] Implementation reviewed
- [ ] Tests passing
- [ ] Security reviewed
- [ ] Documentation reviewed
- [ ] No secrets committed