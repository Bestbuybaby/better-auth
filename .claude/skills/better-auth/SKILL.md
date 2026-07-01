```markdown
# better-auth Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `better-auth` TypeScript codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to write and run tests. While no specific workflows were detected, this guide provides best practices and suggested commands to streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userService.ts`, `authProvider.ts`

### Import Style
- Use **relative imports** for referencing other files.
  - Example:
    ```typescript
    import { validateUser } from './validateUser';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In authProvider.ts
    export function authenticate() { ... }

    // In another file
    import { authenticate } from './authProvider';
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use the `chore` prefix for maintenance tasks.
  - Example:
    ```
    chore: update dependencies and fix minor lint issues
    ```

## Workflows

### Commit Changes
**Trigger:** When you are ready to commit code changes.
**Command:** `/commit-changes`

1. Stage your changes:
    ```
    git add .
    ```
2. Write a commit message following the conventional commit format (e.g., `chore: ...`):
    ```
    git commit -m "chore: describe your change here"
    ```
3. Push your changes:
    ```
    git push
    ```

### Run Tests
**Trigger:** Before pushing or merging changes.
**Command:** `/run-tests`

1. Locate test files matching the `*.test.*` pattern.
2. Run your test suite using your preferred test runner (framework is unknown; adjust as needed):
    ```
    # Example for Jest
    npx jest
    ```
3. Review test results and fix any failing tests.

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example: `authProvider.test.ts`
- The specific test framework is not detected; common choices include Jest or Mocha.
- Place tests alongside the files they test or in a dedicated `tests` directory.

**Example test file:**
```typescript
// authProvider.test.ts
import { authenticate } from './authProvider';

describe('authenticate', () => {
  it('should return true for valid credentials', () => {
    expect(authenticate('user', 'pass')).toBe(true);
  });
});
```

## Commands
| Command         | Purpose                                 |
|-----------------|-----------------------------------------|
| /commit-changes | Guide for committing code changes       |
| /run-tests      | Steps to run the test suite             |
```
