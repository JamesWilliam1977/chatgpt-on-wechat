```markdown
# chatgpt-on-wechat Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the key development patterns, coding conventions, and contribution workflows used in the `chatgpt-on-wechat` repository. The project is implemented in TypeScript and focuses on maintainable code structure, clear commit messaging, and streamlined contribution processes. Whether you're contributing code, improving documentation, or writing tests, this guide will help you align with the project's established practices.

## Coding Conventions

### File Naming
- **Style:** PascalCase
- **Example:**  
  ```plaintext
  ChatService.ts
  MessageHandler.ts
  ```

### Import Style
- **Relative imports** are used for internal modules.
- **Example:**
  ```typescript
  import { ChatService } from './ChatService';
  ```

### Export Style
- **Named exports** are preferred.
- **Example:**
  ```typescript
  export function sendMessage() { ... }
  export const MESSAGE_LIMIT = 10;
  ```

### Commit Messages
- **Conventional commit style** is used.
- **Prefix:** `docs` (for documentation-related changes)
- **Average length:** ~41 characters
- **Example:**
  ```
  docs: update contribution guidelines
  ```

## Workflows

### Update Contribution and Issue Templates
**Trigger:** When you want to improve or add documentation and templates for contributing, issues, or pull requests.  
**Command:** `/update-templates`

1. Edit or create files in `.github/ISSUE_TEMPLATE/` (e.g., `1.bug.yml`, `2.feature.yml`, `config.yml`)
2. Edit or create `.github/PULL_REQUEST_TEMPLATE.md`
3. Edit or create `CONTRIBUTING.md`
4. Commit your changes with a `docs:` prefix in the commit message
5. Open a pull request for review

**Files Involved:**
- `.github/ISSUE_TEMPLATE/1.bug.yml`
- `.github/ISSUE_TEMPLATE/2.feature.yml`
- `.github/ISSUE_TEMPLATE/config.yml`
- `.github/PULL_REQUEST_TEMPLATE.md`
- `CONTRIBUTING.md`

**Example Commit:**
```
docs: add feature request issue template
```

## Testing Patterns

- **Test File Naming:** Files follow the `*.test.*` pattern.
  - Example: `ChatService.test.ts`
- **Testing Framework:** Not explicitly specified; check for test runner configuration in the repository.
- **Test Example:**
  ```typescript
  import { sendMessage } from './ChatService';

  test('sendMessage returns expected output', () => {
    expect(sendMessage('hello')).toBe('Message sent: hello');
  });
  ```

## Commands

| Command           | Purpose                                                        |
|-------------------|----------------------------------------------------------------|
| /update-templates | Update or add contribution guidelines and issue/PR templates   |
```
