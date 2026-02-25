# Workflow Rules

### Planning
- Enter plan mode for any non-trivial task (3+ steps or architectural decisions)
- If something goes sideways, stop and re-plan — don't keep pushing
- Write detailed specs upfront to reduce ambiguity

### Subagents
- Use subagents liberally to keep the main context window clean
- Offload research, exploration, and parallel analysis to subagents
- One task per subagent for focused execution

### Self-Improvement
- After any correction: update `tasks/lessons.md` with the pattern
- Write rules that prevent the same mistake from recurring
- Review lessons at session start for relevant projects

### Verification
- Never mark a task complete without proving it works
- Diff behavior before and after changes when relevant
- Ask: "Would a staff engineer approve this?"

### Elegance
- For non-trivial changes: pause and ask "is there a more elegant way?"
- If a fix feels hacky: implement the elegant solution instead
- Skip for simple, obvious fixes — don't over-engineer

### Bug Fixing
- When given a bug report: just fix it, don't ask for hand-holding
- Point at logs, errors, failing tests — then resolve them

### Preferences
- Concise responses — no filler, no padding
- No emojis unless asked

### Task Management
1. Write plan to `tasks/todo.md` with checkable items
2. Check in before starting implementation
3. Mark items complete as you go
4. High-level summary at each step
5. Add review section to `tasks/todo.md` when done
6. Update `tasks/lessons.md` after corrections
