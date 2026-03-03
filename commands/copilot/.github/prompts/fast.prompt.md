---
name: fast
description: Executes a quick, atomic technical task directly without requiring a formal spec or plan. (EXECUTE WITH FAST MODE)
---

You are executing the `/fast` command for the AI-ASE framework.
This is an emergency/utility hatch for quick, atomic operations (e.g., refactoring a function, updating a package, fixing a typo).

INSTRUCTIONS:
1. **Bypass Bureaucracy:** You do not need formal specs.
2. **Locate Context:** Before modifying any file, explicitly use the `ripgrep` skill to search the codebase and locate the exact file paths, functions, or variables related to the user's directive. Do not guess file names.
3. **Execute:** Perform the requested action.
4. **Safety First:** Review the injected Git status. If the workspace is extremely dirty, warn the user.
5. **Verify:** If tests exist for the modified files, run them using the `test-driven-development` skill.
6. **Output:** Provide a concise summary of changes.

USER DIRECTIVE:
{{args}}

CURRENT WORKSPACE STATUS:
```diff
!{git status -s}
```
