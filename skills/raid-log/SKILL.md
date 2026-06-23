---
name: raid-log
description: Create and maintain a RAID log — Risks, Assumptions, Issues, and Dependencies — for a project or program. Use when the user says "RAID log", "risk register", "track our risks/assumptions/issues/dependencies", "log a new risk", or needs a structured way to track and review threats and open items.
---

# RAID Log

Build and maintain a RAID log: the running record of **R**isks, **A**ssumptions, **I**ssues, and **D**ependencies that could affect delivery.

## Definitions (keep them distinct)
- **Risk** — something that *might* happen and would have impact. Has probability + impact + mitigation.
- **Assumption** — something taken as true without proof; becomes a risk if wrong. Track validation.
- **Issue** — a risk that *has* materialized, or a current problem. Needs an owner and resolution.
- **Dependency** — something you need from (or owe to) another team/vendor, with a date.

## When to use
- Standing up risk tracking for a project, or adding/updating entries during delivery.
- Prepping a risk review or steering-committee section.

## Process
1. Classify each item into exactly one of R / A / I / D.
2. For **risks**: score **Probability** (H/M/L) and **Impact** (H/M/L), derive severity, and give a **mitigation** + **owner**. Note a trigger/early warning if useful.
3. For **assumptions**: note how/when it will be **validated** and the impact if false.
4. For **issues**: capture **impact**, **owner**, **target resolution date**, and status.
5. For **dependencies**: capture **what**, **direction** (we need / they need), **owner on both sides**, and **needed-by date**.
6. Give every entry a stable **ID**, an **owner**, a **status** (Open/Mitigating/Closed), and a **last-updated** date. Sort by severity.

## Output format
Use [templates/raid-template.md](templates/raid-template.md). When updating an existing log, preserve IDs and show what changed.
