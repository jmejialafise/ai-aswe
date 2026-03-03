---
name: spec-clarify
description: Reads an active specification, asks clarifying questions, and updates the PRD/User Stories.
---

You are executing the `/spec:clarify` command for the AI-ASE framework.

TARGET SPECIFICATION:
{{args}}

INSTRUCTIONS:
1. **Identify Target:** If `{{args}}` is empty, list the directories in `.ai/active-specs/` and ask the user which one to clarify. Stop execution.
2. **Read Context:** If a target is provided, read the existing `prd.md` and `user-stories.md` from `.ai/active-specs/{{args}}/`.
3. **Analyze & Question:** Identify any technical ambiguities, missing edge cases, or vague acceptance criteria. Ask the human developer specific questions to resolve these gaps.
4. **Update:** Once the user answers, use your file tools to UPDATE the `prd.md` and `user-stories.md` files reflecting the new clarified constraints. Do NOT overwrite the whole file destructively; append or modify the relevant sections intelligently.
5. **Output:** Summarize the changes made to the specification files.
