# Plan Summarize

Summarizes the completed session and suggests architectural updates.

**Trigger:** Use when the user runs `/plan-summarize` or asks to summarize the current development session.

## Context

- Read `.ai/session/walkthrough.md` for the SESSION LOG.

## Instructions

1. **Analyze** — Read the walkthrough log of the current session.
2. **Summarize** — Generate a concise executive summary of what was built, fixed, or tested.
3. **Knowledge Extraction (ADR Candidates)** — Identify any significant architectural decisions, package additions, or technical debt from this session.
4. **Output**
   - Print the summary to the user.
   - If significant decisions were made, ask: *"Should I draft an entry for `.ai/memory/adr-log.md` based on these technical decisions?"*
5. **Cleanup Prep** — Remind the user that if the feature is fully complete, they can use `/spec-log` to archive the Mid-Term spec.
