---
name: retrospective
argument-hint: [team/project + raw notes]
description: Facilitate and write up a team retrospective — what went well, what didn't, and owned, time-bound action items. Use when the user says "run a retro", "retrospective", "sprint retro", "project post-completion review", "lessons learned", or wants to turn raw retro notes into a structured summary with follow-ups.
---

# Retrospective

Help a team reflect productively and leave with a small number of concrete, owned improvements — not a venting session.

## When to use
- End of a sprint, milestone, project, or quarter.
- Turning messy retro notes/transcript into a clean writeup.
- Designing a retro format/agenda.

Note: for incidents/outages use `postmortem` (blameless, root-cause focused) instead.

## Inputs to gather
- What's being retro'd and the timeframe; who participated.
- Raw input if any (notes, sticky-note dump, transcript), or run a structured prompt.

## Process
1. Pick a frame — **What went well / What didn't / What to try**, or Start–Stop–Continue, or Mad–Sad–Glad.
2. Group raw input into **themes**; don't list every duplicate sticky.
3. Keep it **blameless** — focus on systems and process, not individuals.
4. Surface the **2–4 highest-leverage improvements**, not a wishlist. Each becomes an action.
5. For every action: **owner**, **concrete next step**, **due date**, and where it's tracked.
6. Revisit **prior retro actions** — were they done? Open loops kill trust in retros.

## Output format
```
## Retro — {{team/project}} · {{period}}

### What went well
- {{theme}}

### What didn't / challenges
- {{theme}}

### Action items
| Action | Owner | Due | Status |
| --- | --- | --- | --- |

### Carryover from last retro
- {{item — done? / still open}}
```
Keep actions few and real. A retro with 12 actions has zero.
