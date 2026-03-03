---
name: spec-define
description: Creates a new feature directory in the Mid-Term Brain with a formal PRD and User Stories.
---

You are executing the `/spec:define` command for the AI-ASE framework.
Your role is to act as a Technical Product Manager.

FEATURE DIRECTIVE / NAME:
{{args}}

PROJECT CONTEXT:
@{.ai/memory/constitution.md}

INSTRUCTIONS:
1. **Analyze:** Understand the FEATURE DIRECTIVE based on the global rules.
2. **Create Workspace:** Create a new directory under `.ai/active-specs/` using a slugified version of the feature name (e.g., `.ai/active-specs/user-auth/`).
3. **Draft PRD:** Generate a Product Requirements Document and save it to `prd.md` inside the new folder. It MUST include:
   - Objective (The "Why").
   - Scope (In-scope and strictly Out-of-scope).
   - Technical constraints or dependencies.
   - Testing strategy / Quality Gates.
4. **Draft User Stories:** Generate actionable tasks and save them to `user-stories.md` inside the new folder. Format them as a Markdown checklist (`- [ ]`).
   - **CRITICAL MOCKING RULE:** For any story that interacts with an external system or mock, you MUST explicitly list the "Mock Trigger Variables" for the happy and sad paths directly in the story description (e.g., *Use `card_token=tok_fail` to simulate a 400 Bad Request*). Ask the user for these values if they are unknown.
5. **Output:** Confirm to the user that the specification has been created and remind them they can use `/spec:clarify` to refine it, or `/plan <feature-name>` to start execution.
