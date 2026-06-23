---
name: decision-log
argument-hint: [the decision + context]
description: Capture decisions in a durable, searchable log — the decision, context, options considered, rationale, owner, and date. Use when the user says "log this decision", "decision record", "ADR", "document what we decided", "decision log", or wants to record why a choice was made so it isn't relitigated later.
---

# Decision Log

Record decisions (and *why*) so the team has a single source of truth and stops relitigating settled questions.

## When to use
- A meaningful decision was made (technical, product, process, scope, prioritization).
- Writing or maintaining a decision log / ADR (Architecture/Any Decision Record) set.

## Inputs to gather
- The decision itself, in one sentence.
- The context/problem that forced a choice.
- Options considered and why the chosen one won (and others lost).
- Who decided, who was consulted, and the date.

## Process
1. State the **decision** as a clear, active sentence ("We will ...").
2. Capture **context** — what made this necessary, constraints, deadline.
3. List **options considered** with the key trade-off of each, and mark the chosen one.
4. Give the **rationale** — why this option, including what you're explicitly accepting as a downside.
5. Note **status** (Proposed / Accepted / Superseded), **decider**, **stakeholders consulted**, and **date**.
6. Record **consequences / follow-ups** and link any decision this supersedes.

## Output format — one record per decision
```
### {{ID}}: {{Decision title}}
- **Status:** Accepted · **Date:** {{date}} · **Decider:** {{name}} · **Consulted:** {{names}}
- **Context:** {{why a decision was needed}}
- **Decision:** We will {{decision}}.
- **Options considered:**
  - {{Option A}} — {{trade-off}}  ✅ chosen
  - {{Option B}} — {{trade-off}}
- **Rationale:** {{why, including accepted downsides}}
- **Consequences / follow-ups:** {{what changes; tasks created}}
```
Keep records append-only: supersede rather than edit history.
