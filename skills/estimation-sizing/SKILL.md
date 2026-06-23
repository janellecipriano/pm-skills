---
name: estimation-sizing
description: Facilitate estimation and turn sizes into a credible delivery forecast — T-shirt sizes or story points, assumptions, and a range rather than a false-precision date. Use when the user says "estimate this", "size these stories", "how long will this take", "story points", "give me a delivery range", or needs to convert scope into a defensible timeline.
---

# Estimation & Sizing

Help a team size work honestly and translate sizes into a *range*, not a fake-precise date.

## When to use
- Sizing a set of stories/initiatives, or producing a delivery forecast from scope.
- Sanity-checking an estimate that feels too confident.

## Principles
- Estimate **relative** size (T-shirt: XS/S/M/L/XL, or points) before absolute time.
- Always estimate a **range** (optimistic / likely / pessimistic), never a single number.
- Make **assumptions explicit** — every estimate rides on them.
- Bigger = less certain. Break L/XL items down before committing.
- Account for the **non-coding tax**: review, testing, integration, meetings, ramp-up.

## Process
1. Clarify scope per item; flag anything too vague to size (size = "needs breakdown").
2. Assign a relative size and a **confidence** (H/M/L). Split low-confidence big items.
3. Capture the **assumptions** behind each estimate.
4. Convert to time using a stated **velocity / throughput** or size→days mapping — show the conversion.
5. Roll up to a **range** and add buffer for risk/unknowns proportional to uncertainty.
6. Present as "likely X, could be Y–Z" with the drivers of the spread.

## Output format
```
| Item | Size | Confidence | Assumptions | Est. range |
| --- | --- | --- | --- | --- |

**Rollup:** likely {{X}}, range {{Y–Z}} ({{unit}})
**Key drivers of uncertainty:** {{...}}
**Assumptions:** {{...}}
```
Resist pressure for a single date — offer the range and the conditions under which the optimistic end holds.
