# GitHub Manager

Expert GitHub repository manager for LLM-assisted repository operations. Covers branch strategy, commit conventions, pull request workflow, release management, GitHub Actions CI/CD, and repository maintenance. Works with Augment CLI, Augment VSCode, and Claude Code.

## Core Capabilities

### Branch Strategy
GitHub Flow with structured naming conventions. Feature, fix, hotfix, chore, docs, and release branch prefixes. Branch protection enforcement on main with required reviews and status checks. Guidance on when to use squash merge, rebase, or merge commit.

### Commit Conventions
Enforces Conventional Commits format (`feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `perf`, `ci`, `revert`). Atomic commit discipline — one logical change per commit. Automatic semantic version bump detection from commit types. Breaking change notation with `!` and `BREAKING CHANGE:` footer.

### Pull Request Workflow
PR template generation for `.github/pull_request_template.md`. PR size guidance (max ~400 lines). Self-review checklist, issue linking with `Closes #N`, and merge strategy selection. Full `gh` CLI commands for creating, reviewing, and merging PRs.

### Release Management
Semantic versioning (`MAJOR.MINOR.PATCH`) tied to Conventional Commits. Git tag creation, GitHub release publishing with auto-generated notes, and pre-release tagging. Keep a Changelog format for `CHANGELOG.md` maintenance.

### GitHub Actions CI/CD
Ready-to-use workflow templates for CI pipelines. Commands for monitoring runs, viewing failed logs, re-running jobs, and manual workflow dispatch. Secret management via `gh secret set` without exposing values.

### Issue Management
Standard label set creation with `gh label create`. Issue creation, filtering, and closing workflows. Milestone and assignment patterns.

### Repository Maintenance
Stale branch detection and cleanup. Fork synchronization with upstream. Vulnerability alert checks via GitHub API. Repository archiving. Repository health reporting (stars, forks, open issues).

### Fallback — GitHub REST API
When the `gh` CLI is not available, the agent uses `web-fetch` against `api.github.com` for read operations (repo info, PRs, commits, workflow runs). Write operations require user-provided authentication.

## Compatible Tools

| Environment | Primary method |
|-------------|---------------|
| Augment CLI | `launch-process` with `gh` + `git` CLI |
| Augment VSCode | `launch-process` + `str-replace-editor` for config files |
| Claude Code | `launch-process` with `gh` + `git` CLI |
| No `gh` CLI | `web-fetch` against GitHub REST API |

## Usage

Load `github-manager.md` in Augment Code CLI, Augment VSCode, or Claude Code. Describe your repository task — the agent will verify the environment, check `gh auth status`, and proceed with the appropriate commands. For destructive operations (deleting branches, force-push, releases) the agent always asks for explicit confirmation.

## Safety Rules

The agent never commits or pushes directly to main without a PR. It never stores, logs, or exposes tokens. It never force-pushes to shared branches. It never creates a release on broken or untested code. All destructive operations require explicit user confirmation.
