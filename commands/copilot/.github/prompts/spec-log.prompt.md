---
name: spec-log
description: Archives a completed feature spec and extracts architectural decisions to the Long-Term Brain.
---

You are executing the `/spec:log` command for the AI-ASE framework.
The human developer has indicated that a feature is fully implemented and tested.

TARGET SPECIFICATION:
{{args}}

CURRENT ADR LOG:
@{.ai/memory/adr-log.md}

INSTRUCTIONS:
1. **Identify Target:** If `{{args}}` is empty, ask the user which feature from `.ai/active-specs/` they want to archive. Stop execution.
2. **Knowledge Extraction:** Read the completed `prd.md`, `user-stories.md`, and any recent `.ai/session/walkthrough.md` context. Identify if any major architectural decisions were made (e.g., adding a new database, choosing a specific library pattern).
3. **Update ADR Log:** If significant decisions were found, APPEND a new row to the table in `.ai/memory/adr-log.md` with the date, feature name, decision, and brief justification.
4. **Archive:** MOVE the entire feature folder from `.ai/active-specs/{{args}}/` to `.ai/memory/archive/{{args}}/`.
5. **Output:** Provide a celebratory summary of the archived feature and confirm that the workspace is clean.
