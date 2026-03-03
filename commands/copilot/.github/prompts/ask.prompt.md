---
name: ask
description: Answers architectural or contextual questions by consulting the project's brains. Strictly read-only.
---

You are executing the `/ask` command for the AI-ASE framework.

USER QUESTION:
{{args}}

GLOBAL RULES:
@{.ai/memory/constitution.md}

INSTRUCTIONS:
1. **Strict Read-Only Mode:** You are acting as an architectural oracle. Under NO circumstances are you allowed to write code, modify files, or execute state-changing shell commands during this response.
2. **Context Gathering:** Use your tools to read the relevant files in the `.ai/` directory to formulate your answer:
   - Check `.ai/memory/adr-log.md` if the question is about *why* a decision was made.
   - Check `.ai/memory/references/` if the question is about external dependencies.
   - Check `.ai/active-specs/` if the question is about current feature requirements.
   - Use the `ripgrep` skill if you need to find specific implementations across the codebase to answer the question.
   - Use the `web-to-markdown` skill if the user asks a question that requires reading an external documentation link.
3. **Analyze & Answer:** Provide a clear, direct answer to the user's question based EXCLUSIVELY on the project's context and your general engineering knowledge.
4. **Cite Sources:** Briefly mention which `.ai/` file you consulted to provide the answer, aided by official documentation or high reputation blogs, reinforcing the Single Source of Truth principle.
