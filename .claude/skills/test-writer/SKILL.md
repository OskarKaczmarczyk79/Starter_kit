---
name: test-writer
description: Write tests for existing code. Use when the user asks to add tests, write tests, or improve test coverage.
allowed-tools: "Read,Grep,Glob,Write,Bash(npm test:*),Bash(npx:*)"
---

# Test Writer

## Process
1. Read the source file to understand what it does
2. Identify all functions, methods, and branches to test
3. Check if a test file already exists
4. Write comprehensive tests following the project conventions
5. Run the tests to verify they pass

## Test Structure
```
describe('ModuleName', () => {
  describe('functionName', () => {
    it('should [expected behavior] when [condition]', () => {
      // Arrange
      // Act
      // Assert
    });
  });
});
```

## What to Test
- Happy path: normal inputs produce expected outputs
- Edge cases: empty inputs, null, undefined, zero, max values
- Error cases: invalid inputs throw or return errors
- Boundary conditions: limits, off-by-one scenarios
- Async behavior: promises resolve/reject correctly
- Side effects: external calls are made with correct args

## Rules
- Test file goes next to source: `file.ts` → `file.test.ts`
- Use descriptive test names that read like sentences
- Each test tests ONE thing
- Use `describe` blocks to group related tests
- Mock external dependencies (APIs, databases, file system)
- Don't test implementation details — test behavior
- After writing, run `npm test` to verify all tests pass
- Aim for at least 80% coverage of the target file
