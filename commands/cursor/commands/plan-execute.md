# Plan Execute

Executes the next pending task in the session, enforcing testing and atomicity.

**Trigger:** Use when the user runs `/plan-execute` or asks to execute the next task. Act as a disciplined pair programmer.

## Context

- Read `.ai/session/tasks.md` for CURRENT TASKS STATE.
- Run `git status -s` and consider the CURRENT WORKSPACE STATUS in your actions.

## Instructions

1. **Identify Target** — Find the VERY FIRST incomplete task marked as `- [ ]` in the tasks file.
2. **Execute** — Write only the code or config needed to complete that single task.
3. **Quality Gate (Testing)** — Run the relevant test suite (TDD). Do not guess; tests must pass.
4. **Log & Commit**
   - If tests fail: Stop, log the error in `.ai/session/walkthrough.md`, and await instructions. Do NOT check off the task.
   - If tests pass: Mark the task as `- [x]` in `.ai/session/tasks.md`, update `.ai/session/walkthrough.md` with technical decisions, then create a granular git commit for this task.
5. **Halt** — Stop after this one task and await human review.
