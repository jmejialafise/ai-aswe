# Spec Clarify

Reads an active specification, asks clarifying questions, and updates the PRD and User Stories.

**Trigger:** Use when the user runs `/spec-clarify` or asks to clarify a spec. The user may type the target spec (folder name under `.ai/active-specs/`) after the command — that is the TARGET SPECIFICATION.

## Instructions

1. **Identify Target** — If no target was provided, list directories in `.ai/active-specs/` and ask which one to clarify. Then stop.
2. **Read Context** — If a target was provided, read `prd.md` and `user-stories.md` from `.ai/active-specs/<target>/`.
3. **Analyze & Question** — Find technical ambiguities, missing edge cases, or vague acceptance criteria. Ask the user specific questions to resolve them.
4. **Update** — After the user answers, update `prd.md` and `user-stories.md` (append or edit relevant sections; do not overwrite destructively).
5. **Output** — Summarize what was changed in the specification files.
