---
name: commit-msg
description: Generate a conventional commit message from staged changes. Use when the user wants to commit code or asks for a commit message.
allowed-tools: "Bash(git diff:*),Bash(git status:*),Bash(git log:*)"
---

# Commit Message Generator

## Process
1. Run `git diff --staged --stat` to see which files changed
2. Run `git diff --staged` to see the actual changes
3. Analyze the changes and determine the primary change type
4. Generate a commit message following the format below

## Format
```
<type>(<scope>): <subject>

<body>

<footer>
```

## Types
- `feat`: New feature or functionality
- `fix`: Bug fix
- `refactor`: Code restructure (no behavior change)
- `docs`: Documentation changes
- `test`: Adding or updating tests
- `chore`: Build process, dependencies, config
- `style`: Formatting, whitespace (no logic change)
- `perf`: Performance improvements

## Rules
- Subject line: max 50 characters, imperative mood ("add" not "added")
- Body: explain WHY the change was made, not just WHAT changed
- If multiple types of changes, use the most significant one
- Reference issue numbers in footer if applicable: `Closes #123`
- Keep it concise but informative
