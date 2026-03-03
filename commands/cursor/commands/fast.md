# Fast

Quick, atomic technical task without a formal spec or plan (e.g. refactor a function, update a package, fix a typo).

**Trigger:** Use when the user runs `/fast` or asks for a quick atomic change. The user's directive is whatever they type after the command.

## Context

- Run `git status -s` and consider workspace status. If the workspace is very dirty, warn the user.

## Instructions

1. **Bypass Bureaucracy** — No formal specs required.
2. **Locate Context** — Before changing any file, search the codebase (e.g. ripgrep) to find the exact file paths, functions, or variables for the user's request. Do not guess file names.
3. **Execute** — Perform the requested action.
4. **Safety First** — If the workspace is extremely dirty from the status above, warn the user.
5. **Verify** — If tests exist for the modified files, run them.
6. **Output** — Give a concise summary of changes.
