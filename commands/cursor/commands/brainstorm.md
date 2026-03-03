# Brainstorm

Acts as a Product Manager / Tech Lead to explore and expand a vague feature idea before writing a formal spec.

**Trigger:** Use when the user runs `/brainstorm` or asks to brainstorm. The user's raw idea (and any URL they provide) is the input.

## Context

- Read `.ai/memory/constitution.md` for PROJECT CONTEXT / Global Rules (if it exists).
- If the user provided an external URL, fetch or summarize that content first (e.g. documentation).

## Instructions

1. **Analyze** — Read the user's raw idea. If they gave a URL, use it to extract content before continuing.
2. **Ideate** — Structure your thinking; identify edge cases and architectural bottlenecks using the constitution.
3. **Dialogue** — Ask the user 2–4 focused questions to clarify scope (out-of-scope, data models, UX).
4. **Call to Action** — Suggest `/spec-define` once the idea is clear enough.
