# Plan

Generates a step-by-step plan and TDD task list based on a specification.

**Trigger:** Use this when the user runs `/plan` or asks to plan. The user may type a target after the command (e.g. `/plan auth-feature`) — treat that as the TARGET SPECIFICATION OR DIRECTIVE.

## Context

- Read `.ai/memory/constitution.md` for GLOBAL RULES (if it exists).

## Instructions

1. **Context Gathering**
   - If a specific folder name was provided in the directive (e.g. `auth-feature`), read `.ai/active-specs/<directive>/prd.md` and `.ai/active-specs/<directive>/user-stories.md`.
   - If no folder was provided, use the directive itself as the raw requirement.

2. **Strategy (`plan.md`)**  
   Create or overwrite `.ai/session/plan.md` with a high-level architectural approach. Explain *how* the components will interact.

3. **Execution Checklist (`tasks.md`)**  
   Create or overwrite `.ai/session/tasks.md` with a granular, technical checklist using Markdown checkboxes (`- [ ]`).

4. **STRICT TDD & MOCKING RULE**  
   The tasks MUST follow Test-Driven Development. For every logical block:
   - [ ] Write failing parameterized tests for [Component]. If interacting with opaque mocks, design the test to accept injected variables (from the spec) to trigger happy/sad paths. DO NOT hardcode the mock's expected behavior.
   - [ ] Implement [Component] to pass the tests.
   - [ ] Refactor and verify linting.

Do NOT write production code yet. Await the human developer's approval of the generated markdown files.
