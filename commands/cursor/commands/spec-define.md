# Spec Define

Creates a new feature directory in the Mid-Term Brain with a formal PRD and User Stories.

**Trigger:** Use when the user runs `/spec-define` or asks to define a spec. The FEATURE DIRECTIVE / NAME is what they type after the command.

## Context

- Read `.ai/memory/constitution.md` for PROJECT CONTEXT (if it exists).

## Instructions

1. **Analyze** — Understand the FEATURE DIRECTIVE using the global rules.
2. **Create Workspace** — Create a new directory under `.ai/active-specs/` using a slugified feature name (e.g. `.ai/active-specs/user-auth/`).
3. **Draft PRD** — Create `prd.md` in that folder. It MUST include:
   - Objective (the "Why")
   - Scope (in-scope and strictly out-of-scope)
   - Technical constraints or dependencies
   - Testing strategy / Quality Gates
4. **Draft User Stories** — Create `user-stories.md` in that folder as a Markdown checklist (`- [ ]`).  
   **CRITICAL MOCKING RULE:** For any story that touches an external system or mock, list the "Mock Trigger Variables" for happy and sad paths in the story (e.g. *Use `card_token=tok_fail` to simulate 400 Bad Request*). Ask the user for these values if unknown.
5. **Output** — Confirm the spec was created and suggest `/spec-clarify` to refine or `/plan <feature-name>` to start execution.
