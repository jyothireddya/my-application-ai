# PR Title

Update Pull Request Agent to create and verify GitHub PRs

# Summary

Update the Pull Request Agent so it has the repository and branch context needed to create and verify the final GitHub pull request. The agent now reads `pull-request.md`, checks GitHub authentication and repository state, and documents the configured source and base branches.

# Changes Made

- `.github/agents/pull-request.agent.md` - Adds the repository, base branch, source branch, PR document input, GitHub authentication check, and repository/PR inspection steps.
- `pull-request.md` - Synchronizes the PR title and description with the actual changes in this branch.

# Test Evidence

- `git status` - PASS: only the two documented files were changed before commit.
- `git log --oneline --all --decorate -10` - PASS: confirmed the source branch initially matched `main`.
- `git diff main...feature/automated-documentation-sync` - PASS: confirmed there were no committed feature-branch differences before this change.
- `gh auth status` - PASS: GitHub CLI is authenticated as `jyothireddya`.

# Known Limitations

- The login implementation and its tests are already present in `main`; they are not duplicated in this pull request.
- No application runtime code was changed in this branch.

# Reviewer Checklist

- [ ] Agent instructions accurately describe the repository workflow
- [ ] PR title and description match the branch changes
- [ ] No secrets committed