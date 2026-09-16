---
name: code-review
description: Review code for bugs, security issues, and improvements. Use when the user asks to review, audit, or check code quality.
allowed-tools: "Read,Grep,Glob,Bash(git diff:*),Bash(git log:*)"
---

# Code Review

## Process
1. Read the files or diff to review
2. Analyze for issues in priority order (see below)
3. Present findings organized by severity
4. Suggest specific fixes with code examples

## Review Checklist (in priority order)

### Critical (must fix)
- Security vulnerabilities (SQL injection, XSS, auth bypass)
- Data loss risks (missing validation, unsafe deletes)
- Race conditions or concurrency bugs
- Hardcoded secrets or credentials

### Important (should fix)
- Logic errors and off-by-one mistakes
- Missing error handling (uncaught promises, empty catches)
- Missing input validation
- Memory leaks or resource cleanup
- Breaking API contract changes

### Suggestions (nice to have)
- Code duplication that could be extracted
- Naming improvements for clarity
- Performance optimizations
- Missing types or loose typing
- Test coverage gaps

## Output Format
For each finding:
```
[SEVERITY] Short title
File: path/to/file.ts, line X
Problem: What's wrong and why it matters
Fix: Concrete suggestion with code
```

## Rules
- Focus on real bugs, not style preferences
- Every finding must include a concrete fix
- Don't nitpick formatting if a formatter is configured
- Acknowledge what's done well — not just problems
- If the code is solid, say so
