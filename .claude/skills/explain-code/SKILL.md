---
name: explain-code
description: Explain how a piece of code works in plain English. Use when the user asks to explain, understand, or break down code.
allowed-tools: "Read,Grep,Glob"
---

# Code Explainer

## Process
1. Read the file or code snippet the user points to
2. Identify the overall purpose of the code
3. Break it down section by section
4. Explain using clear, beginner-friendly language

## Output Format

### Overview
One sentence: what does this code do and why does it exist?

### Step-by-step Breakdown
Walk through the code in logical sections:
- What each section does
- Why it's done that way
- Any patterns or conventions used (name them)

### Key Concepts
List any design patterns, algorithms, or concepts a beginner should know:
- Name the pattern/concept
- One-line explanation
- Why it's used here

### Gotchas
Anything non-obvious or tricky about this code:
- Edge cases handled (or not handled)
- Implicit dependencies
- Performance considerations

## Rules
- Use plain English, avoid unnecessary jargon
- If you use a technical term, explain it in parentheses
- Use analogies when they help
- Be honest about complexity — don't oversimplify
