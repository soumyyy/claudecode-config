---
description: Hand off a task to OpenAI Codex CLI agent
argument-hint: [task description]
allowed-tools: Bash(codex:*)
---

# Codex Handoff

Hand off a task to the OpenAI Codex CLI agent running in the current working directory.

## Task

$ARGUMENTS

## Instructions

1. If no task was provided (arguments are empty), inform the user they should provide a task description, e.g.: `/codex refactor the auth module to use async/await`

2. Otherwise, run Codex non-interactively with the task:

```
codex exec "$ARGUMENTS"
```

Use the Bash tool to execute: `codex exec "$ARGUMENTS"`

3. Stream/display the full output from Codex to the user.

4. After Codex completes, summarize what it did and any next steps the user should take (e.g., review diffs, run tests, apply changes with `codex apply`).

## Notes

- Codex runs in the current working directory
- Use `codex apply` afterwards to apply any generated diffs
- For interactive mode, the user can run `codex` directly in their terminal
