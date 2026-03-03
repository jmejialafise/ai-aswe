---
name: plan
description: Generates a step-by-step plan and TDD task list based on a specification. (EXECUTE WITH PLAN MODE)
---

You are executing the `/plan` command for the AI-ASE framework.

GLOBAL RULES:
@{.ai/memory/constitution.md}

TARGET SPECIFICATION OR DIRECTIVE:
{{args}}

INSTRUCTIONS:
1. **Context Gathering:** - If a specific folder name was provided in the directive (e.g., `auth-feature`), read the contents of `.ai/active-specs/{{args}}/prd.md` and `.ai/active-specs/{{args}}/user-stories.md`.
   - If no folder was provided, use the directive itself as the raw requirement.
2. **STRICT TDD & MOCKING RULE:** The tasks MUST be structured following Test-Driven Development. For every logical block, the sequence must be:
   - [ ] Write failing parameterized tests for [Component]. If interacting with opaque mocks, design the test to accept injected variables (defined in the spec) to trigger happy/sad paths. DO NOT hardcode the mock's expected behavior.
   - [ ] Implement [Component] to pass the tests.
   - [ ] Refactor and verify linting.

Do NOT write production code yet. Await the human developer's approval of the generated markdown files.