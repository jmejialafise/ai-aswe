# Spec Log

Archives a completed feature spec and records architectural decisions in the Long-Term Brain.

**Trigger:** Use when the user runs `/spec-log` or asks to archive a spec. The user may type the target spec name (e.g. folder under `.ai/active-specs/`) after the command — that is the TARGET SPECIFICATION.

## Context

- Read `.ai/memory/adr-log.md` for the CURRENT ADR LOG.

## Instructions

1. **Identify Target** — If no target was provided, list `.ai/active-specs/` and ask which feature to archive. Then stop.
2. **Knowledge Extraction** — Read the completed `prd.md`, `user-stories.md`, and any recent `.ai/session/walkthrough.md`. Note any major architectural decisions (e.g. new DB, library pattern).
3. **Update ADR Log** — If there are significant decisions, APPEND a new row to the table in `.ai/memory/adr-log.md` (date, feature name, decision, brief justification).
4. **Archive** — MOVE the feature folder from `.ai/active-specs/<target>/` to `.ai/memory/archive/<target>/`.
5. **Output** — Give a short summary of the archived feature and confirm the workspace is clean.
