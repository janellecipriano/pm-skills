---
name: dependency-mapping
description: Map cross-team and external dependencies for a project — what's needed, from whom, by when — and identify the critical path and at-risk handoffs. Use when the user says "map dependencies", "what are we blocked on", "cross-team dependencies", "critical path", or needs to coordinate handoffs across teams or vendors.
---

# Dependency Mapping

Make every cross-team and external dependency visible, owned, and dated — and surface the ones that threaten the timeline.

## When to use
- Coordinating delivery that spans multiple teams or vendors.
- Diagnosing what's blocking progress or building a dependency view for a plan/review.

## Inputs to gather
- The deliverables/milestones and their target dates.
- For each: what's needed from another team/vendor, and what others need from you.
- Known owners on both sides and any commitments already made.

## Process
1. List dependencies as directional edges: **A needs X from B by date D**.
2. For each, capture: **provider**, **consumer**, **what**, **needed-by date**, **provider's committed date**, **status**, and **owner**.
3. Flag a dependency **at risk** when there's no committed date, the committed date is after needed-by, or the owner is unconfirmed.
4. Identify the **critical path** — the chain of dependencies that, if any slips, slips the whole project.
5. Note **circular/mutual** dependencies and sequencing conflicts explicitly.
6. Recommend actions: confirm owners, get commitments, decouple where possible, add buffer.

## Output format
```
## Dependency Map — {{project}}

| ID | What | Provider → Consumer | Needed by | Committed | Status | Owner | At risk? |
| --- | --- | --- | --- | --- | --- | --- | --- |

### Critical path
{{ordered chain with dates}}

### At-risk dependencies & recommended actions
- {{dependency}} — {{why at risk}} → {{action, owner, by when}}
```
If a visual helps, offer a simple text/Mermaid dependency diagram.
