---
name: program-health-dashboard
argument-hint: [workstreams + statuses]
description: Assemble a one-page program health snapshot across multiple workstreams — RAG status, milestones, top risks, dependencies, and metrics in a single scannable view. Use when the user says "program dashboard", "program health", "portfolio status", "one-pager across workstreams", "roll up all the projects", or needs an at-a-glance view of a multi-stream program.
---

# Program Health Dashboard

Roll multiple workstreams into a single, scannable one-page health view for program leads and steering committees.

## When to use
- A program spans several projects/workstreams and needs one combined view.
- Prepping a steering/portfolio review.

For a single project's narrative update, use `status-report`; for a leadership narrative, `exec-summary`.

## Inputs to gather
- The workstreams and their owners.
- Per workstream: RAG status, next milestone + date, top risk, key metric.
- Cross-program risks and dependencies (pull from `raid-log` / `dependency-mapping`).

## Process
1. Set an **overall program RAG** with a one-line rationale (worst-of, weighted by importance — explain the logic).
2. Build the **workstream table**: name · owner · RAG · next milestone (date) · trend (↑/→/↓ vs. last period) · top risk.
3. Surface **top cross-program risks/blockers** (3–5 max) with owners.
4. Show **key metrics** vs. target where the program is measured (tie to `okr-tracking`).
5. List **upcoming milestones** across all streams in date order.
6. Note **decisions needed** from leadership.

## Output format
```
# {{Program}} — Health · {{date}}
**Overall:** 🟢/🟡/🔴 — {{rationale}}

## Workstreams
| Workstream | Owner | Status | Next milestone (date) | Trend | Top risk |
| --- | --- | --- | --- | --- | --- |

## Top risks & blockers (program-level)
| Risk | Impact | Owner | Mitigation |

## Key metrics
| Metric | Target | Current | Status |

## Upcoming milestones
| Date | Milestone | Workstream |

## Decisions needed
- {{ask}}
```
Keep it to one page — this is a glance, not a deep read. Link out for detail.
