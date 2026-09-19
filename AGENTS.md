# PTNK HUB CLUB — AI Development Rules

## 1. Core principle

Work like a lazy senior developer:
efficient, simple, and deliberate.

Before writing code, check:

1. Does this need to be built at all?
2. Does the existing project already solve it?
3. Does the standard library or native platform feature solve it?
4. Does an already-installed dependency solve it?
5. Can the implementation be simpler?
6. Only then write the minimum code required.

## 2. Avoid unnecessary complexity

- Do not create abstractions unless they are actually needed.
- Do not add dependencies without a clear reason.
- Do not create boilerplate that provides no current value.
- Prefer deletion and simplification over adding more code.
- Prefer boring, readable solutions over clever solutions.
- Keep the number of files as small as reasonably possible.
- Do not refactor unrelated code.

## 3. Project scope

- Follow the current project requirements and documentation.
- Do not invent features that were not requested.
- Do not expand the scope without a clear reason.
- Check `docs/` before making decisions that affect project requirements.
- Treat project documentation as the source of truth for product requirements.

## 4. AI behavior

Before making a significant change:

- Understand the existing structure.
- Check whether the requested functionality already exists.
- Reuse existing code when appropriate.
- Explain important assumptions when they affect implementation.
- Do not silently make major architectural decisions.
- Do not overwrite existing work without checking it first.

## 5. Dependencies

- Avoid adding a new dependency when an existing solution is sufficient.
- Do not install libraries just because they are popular.
- Every new dependency should have a concrete project reason.
- Keep dependencies consistent with the project's chosen stack.

## 6. Code quality

- Keep code readable and maintainable.
- Prefer straightforward implementations.
- Handle errors that could cause data loss or broken application state.
- Validate input at trust boundaries.
- Consider security and accessibility.
- Do not sacrifice correctness merely to reduce lines of code.

## 7. Testing and verification

Non-trivial logic must leave behind at least one practical way to verify it.

Prefer the smallest useful check:

- a small test,
- an assertion,
- a validation command,
- or a reproducible manual check.

Trivial one-line changes do not require a dedicated test.

## 8. Changes

When modifying the project:

- Make the smallest change that solves the requirement.
- Do not modify unrelated files.
- Preserve existing functionality.
- Check the result after significant changes.
- If a change introduces a known limitation, document it clearly.

## 9. Git

- Do not delete or rewrite Git history unless explicitly requested.
- Do not remove `.git/`.
- Do not commit secrets, credentials, API keys, or generated dependency folders.
- Keep commits focused on related changes.
- Check `git status` before major operations.

## 10. Spec Kit

When using Spec Kit:

- Follow the project's specification before implementation.
- Do not skip requirements simply because implementation is easier.
- Keep specifications, plans, and tasks consistent with the actual project.
- Do not create unnecessary specifications for trivial changes.

## 11. Ponytail principle

When a shortcut is intentionally chosen:

```text
ponytail:
```
