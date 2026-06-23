---
name: sprint-planning
description: Plan a sprint or iteration — sprint goal, available capacity, committed scope, and risks — from a backlog. Use when the user says "plan the sprint", "sprint planning", "what should we commit to this iteration", "groom the backlog into a sprint", or needs to turn priorities + capacity into a realistic commitment.
---

# Sprint Planning

Turn a prioritized backlog and a known capacity into a realistic, goal-driven sprint commitment.

## When to use
- Planning the next sprint/iteration.
- Sanity-checking whether a proposed commitment fits capacity.

## Inputs to gather
- Sprint length and start/end dates.
- Team capacity: who's available, PTO/holidays, and any split focus. (See `capacity-planning` for deeper modeling.)
- Candidate backlog items with priority and rough sizing (see `estimation-sizing`).
- Carryover from the previous sprint.

## Process
1. Define a single, crisp **sprint goal** — the outcome that makes this sprint a success. One sentence.
2. Compute **available capacity** (people × days − meetings/PTO − buffer). Reserve ~15–20% buffer for unknowns/support.
3. Pull items by **priority** that serve the goal until capacity is reached; stop there. Don't pad to 100%.
4. For each committed item, confirm it's **ready** (clear, sized, dependencies unblocked) — defer anything not ready.
5. Note **risks/dependencies** that could derail the sprint and who owns them.
6. State explicit **stretch** items separately from the commitment.

## Output format
```
## Sprint {{n}} — {{dates}}
**Goal:** {{one sentence}}
**Capacity:** {{X person-days, after buffer}}

### Committed
| Item | Owner | Size | Notes |
| --- | --- | --- | --- |

### Stretch (only if commitment finishes early)
- {{item}}

### Risks / dependencies
- {{risk}} — owner {{name}}
```
Flag clearly if requested scope exceeds capacity, and recommend what to cut.
