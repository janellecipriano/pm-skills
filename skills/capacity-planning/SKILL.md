---
name: capacity-planning
argument-hint: [team + horizon + demand]
description: Model team capacity against committed and planned demand to spot over-allocation and forecast what can realistically be delivered. Use when the user says "capacity planning", "do we have bandwidth", "are we over-allocated", "headcount vs. demand", "can we take on X", or needs to balance workload against available people.
---

# Capacity Planning

Compare the work a team has signed up for against the capacity it actually has, and make over-allocation visible before it becomes slippage.

## When to use
- Deciding whether the team can absorb new work.
- Planning a quarter/sprint allocation across people and workstreams.
- Diagnosing chronic over-commitment.

## Inputs to gather
- People on the team and their availability (FTE %, PTO/holidays, on-call, shared allocations).
- The time horizon (sprint, month, quarter).
- Committed + requested work with rough sizing (see `estimation-sizing`).

## Process
1. Compute **gross capacity** = people × working days in the horizon.
2. Subtract **overhead**: meetings, support/on-call, PTO, ramp-up, and a realistic productivity factor (people aren't 100% project-billable — often ~60–80%). State the factor used.
3. That's **net available capacity**.
4. Sum **committed demand** (sized work) and compare to net capacity → **surplus or deficit**.
5. Break down by **person/role** to catch individual over-allocation even when the team total looks fine (a single bottleneck skill blocks everything).
6. If over-allocated, present **options**: cut/defer scope, add people, extend timeline, reduce overhead. Recommend one.

## Output format
```
## Capacity — {{team}} · {{horizon}}
| Person | Avail % | Net days | Allocated days | Over/Under |
| --- | --- | --- | --- | --- |

**Team:** net capacity {{X}} vs. demand {{Y}} → **{{surplus/deficit}} of Z days**
**Assumptions:** productivity factor {{%}}, overhead {{...}}
**Recommendation:** {{cut / add / extend}}
```
Always state assumptions — capacity numbers are only as good as the overhead estimate behind them.
