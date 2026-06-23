---
name: postmortem
description: Run a blameless postmortem / incident review — timeline, impact, root cause analysis, and corrective actions. Use when the user says "postmortem", "incident review", "RCA", "root cause analysis", "what happened with the outage", or wants to turn an incident into a structured, blameless writeup with preventive actions.
---

# Postmortem (Blameless Incident Review)

Turn an incident into learning and prevention — focused on systems and process, never on blaming individuals.

## When to use
- After an outage, regression, data issue, security event, or significant miss.

For sprint/project reflection (not incidents) use `retrospective`.

## Principles
- **Blameless.** Assume everyone acted reasonably with the information they had. Fix systems, not people. Replace "X made a mistake" with "the system allowed X to happen."
- **Facts first.** Build the timeline from evidence (logs, alerts, messages) before drawing conclusions.
- **Root cause, not first cause.** Use the **5 Whys** / contributing-factors analysis to get past the proximate trigger.
- **Actions must prevent recurrence**, be owned, and be dated.

## Inputs to gather
- What happened, when detected, when resolved; severity and who/what was impacted.
- The timeline of events and the response.
- Logs/notes if available.

## Process
1. Write a **summary**: what happened, impact (users/duration/scope), severity.
2. Build a **timeline** (UTC or stated TZ): detection → diagnosis → mitigation → resolution. Note time-to-detect and time-to-resolve.
3. Analyze **root cause(s)** and **contributing factors** (5 Whys).
4. Note **what went well** and **what made it worse** (detection gaps, slow rollback, unclear ownership).
5. Define **corrective actions**: preventive + detective, each with owner, due date, priority.
6. Capture **lessons learned**.

## Output format
```
# Postmortem — {{incident}} · {{date}}
**Severity:** {{SEV}} · **Impact:** {{users/scope/duration}} · **Status:** Resolved

## Summary
{{2–4 sentences}}

## Timeline
| Time | Event |

## Root cause & contributing factors
{{5 Whys / analysis}}

## What went well / what went poorly
- ...

## Action items
| Action | Type (prevent/detect) | Owner | Due | Priority |
```
Keep tone neutral and factual throughout.
