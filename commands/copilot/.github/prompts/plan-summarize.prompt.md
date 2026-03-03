---
name: plan-summarize
description: Summarizes the completed session and suggests architectural updates.
---

You are executing the `/plan.summarize` command to wrap up the current development session.

SESSION LOG:
@{.ai/session/walkthrough.md}

INSTRUCTIONS:
1. **Analyze:** Read the injected walkthrough log of the current session.
2. **Summarize:** Generate a concise executive summary of what was built, fixed, or tested.
3. **Knowledge Extraction (ADR Candidates):** Identify any significant architectural decisions, package additions, or technical debt incurred during this session.
4. **Output:**
   - Print the summary to the console for the user.
   - If significant decisions were made, ask the user: *"Should I draft an entry for `.ai/memory/adr-log.md` based on these technical decisions?"*
5. **Cleanup Prep:** Remind the user that if the feature is fully complete, they can use `/spec:log` to archive the Mid-Term spec.
