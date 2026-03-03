# Ask

Answers architectural or contextual questions using the project's stored context. **Strictly read-only.**

**Trigger:** Use when the user runs `/ask` or asks an architectural/contextual question. The user's question is whatever they type after the command.

## Context

- Read `.ai/memory/constitution.md` for GLOBAL RULES (if it exists).

## Instructions

1. **Strict Read-Only Mode** — You are an architectural oracle. Do NOT write code, modify files, or run state-changing shell commands in this response.
2. **Context Gathering** — Use tools to read from `.ai/` as needed:
   - `.ai/memory/adr-log.md` for *why* a decision was made
   - `.ai/memory/references/` for external dependencies
   - `.ai/active-specs/` for current feature requirements
   - Search the codebase (e.g. ripgrep) for specific implementations
   - If the question involves an external doc link, fetch or summarize that content
3. **Analyze & Answer** — Give a clear, direct answer based only on project context and sound engineering.
4. **Cite Sources** — Briefly note which `.ai/` file or doc you used, following Single Source of Truth.
