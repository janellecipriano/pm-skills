---
name: launch-readiness
description: Run a go/no-go launch-readiness review for a product or feature release across all functions (product, eng, QA, design, docs, support, marketing, legal, ops). Use when the user says "launch readiness", "go/no-go", "are we ready to ship/launch", "release checklist", or needs a cross-functional sign-off before shipping.
---

# Launch Readiness

Drive a cross-functional readiness review that ends in a clear **Go / No-Go / Go-with-conditions** recommendation.

## When to use
- Approaching a release and you need to confirm every function is ready.
- Preparing a go/no-go meeting or sign-off doc.

## Inputs to gather
- What's launching, the target date/window, and the rollout plan (e.g., %-based, regions, GA vs. beta).
- Status by function; known open issues and their severity.
- Success metrics and the rollback/kill-switch plan.

## Process — review each readiness area
For each area, capture **status (🟢/🟡/🔴), owner, evidence/notes, and blocking?**:
1. **Product/Scope** — acceptance criteria met; scope cuts agreed.
2. **Engineering** — code complete, feature-flagged, perf/scale checked, on-call ready.
3. **Quality** — test pass, critical bugs triaged to zero, edge cases covered.
4. **Design/UX** — final review, accessibility, edge/empty/error states.
5. **Docs & Support** — help content, runbooks, support team briefed.
6. **Go-to-market** — comms, release notes (`release-notes`), pricing/packaging if relevant.
7. **Legal/Privacy/Compliance** — reviews and approvals where required.
8. **Data/Analytics** — instrumentation live; success metrics measurable.
9. **Rollout & rollback** — staged plan, monitoring/alerts, tested rollback, named decision owner.

## Decision
- **Go** — all critical areas green.
- **Go with conditions** — minor ambers with named owners + dates; list the conditions.
- **No-Go** — any red in a blocking area; state what must close and the re-review date.

## Output format
A readiness table (area · status · owner · notes · blocking?) followed by the **recommendation**, the **conditions/blockers**, and the **rollback plan**. State the decision owner and the go/no-go meeting time.
