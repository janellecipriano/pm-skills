---
name: status-report
description: Write a concise project or program status report with an overall RAG (red/amber/green) health rating, progress since last update, what's next, risks/blockers, and explicit asks. Use when the user says "write a status report", "weekly update", "status update", "where are we on X", or needs a stakeholder-ready progress summary.
---

# Status Report

Produce a scannable status update a busy stakeholder can read in under a minute.

## When to use
- Recurring project/program updates (weekly, biweekly) for stakeholders or leadership.
- An ad-hoc "where are we?" snapshot.

## Inputs to gather
- Reporting period and audience (team vs. exec changes the altitude).
- What got done since last update; what's planned next.
- Current blockers/risks and any decisions or help needed.
- If available, prior report (to show deltas) and target dates.

## Process
1. Set an overall **RAG status** and one-line rationale:
   - 🟢 Green — on track. 🟡 Amber — at risk, has a plan. 🔴 Red — off track, needs intervention.
2. Lead with a **TL;DR** (2–3 sentences): health, biggest progress, biggest risk.
3. List **progress** as completed outcomes (not activity). Show schedule deltas vs. plan.
4. List **next** — the few things that matter most for the coming period.
5. Surface **risks/blockers** with owner and mitigation.
6. End with **asks** — specific, addressed to a named person, with a needed-by date. Omit if none.

## Style
- Outcomes over activity. Numbers over adjectives. Be honest about amber/red — hiding slippage erodes trust.
- Keep it short; link out for detail.

## Output format
Use [templates/status-template.md](templates/status-template.md).
