# Claude Code Reviewer

A code review agent for Claude Code that examines changes for correctness, security vulnerabilities, performance issues, and maintainability.

## What it does

- Reviews changed code with a diff-first approach.
- Checks security risks, including injection, authentication, and sensitive-data exposure.
- Examines error handling, tests, dependencies, and performance.
- Applies language-specific checks for TypeScript, Python, Rust, Go, and SQL.
- Reports findings by severity with a clear risk explanation and actionable fix.
- Ends with a review summary and merge recommendation.

## Repository contents

| File | Purpose |
| --- | --- |
| `code-reviewer.md` | Agent definition and review instructions. |
| `LICENSE` | MIT License for this repository. |

## Usage

1. Make the agent available in your Claude Code agent configuration using the installation method supported by your setup.
2. Invoke `code-reviewer` when you want a review of changed code.
3. Provide the pull request, diff, files, or specific area that needs review.

For best results, include the relevant project conventions, expected behavior, and any risk areas that deserve extra attention.

## Review output

The agent structures findings by severity:

- **CRITICAL**: Issues that should block merging.
- **HIGH**: Significant correctness, security, or reliability concerns.
- **MEDIUM**: Problems that should be addressed but may not block a release.
- **LOW / SUGGESTION**: Improvements to clarity, maintainability, or consistency.

Each finding should explain the risk and give a concrete fix.

Read [`code-reviewer.md`](./code-reviewer.md) for the complete agent instructions.
