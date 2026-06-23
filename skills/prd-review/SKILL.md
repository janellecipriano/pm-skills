---
name: prd-review
argument-hint: [paste PRD or file path]
description: Review a product requirements document (PRD) or spec against a quality checklist and surface gaps, ambiguities, and risks before engineering starts. Use when the user says "review this PRD", "is this spec ready", "critique my requirements", "PRD checklist", or shares a doc and wants it pressure-tested before build.
---

# PRD Review

Pressure-test a PRD so problems are caught on the page, not in code. Be a constructive but skeptical reviewer.

## When to use
- A PRD/spec exists and the user wants feedback or a readiness check before build/estimation.

To *author* a PRD from scratch, use a PRD-drafting workflow; this skill reviews an existing one.

## Review checklist
Assess the doc against each dimension. Quote or reference specifics; don't be generic.
1. **Problem & why now** — is the user problem clear and evidenced (not just a feature request)?
2. **Audience** — are target users/segments and their context defined?
3. **Goals & success metrics** — measurable outcomes, baseline → target? Anti-goals stated?
4. **Scope** — explicit in/out? MVP vs. later cuts clear?
5. **Requirements** — unambiguous, testable, prioritized (must/should/could)? No solution disguised as requirement.
6. **UX** — flows, key states (empty/error/loading/edge), accessibility considered?
7. **Edge cases & failure modes** — what happens when things go wrong?
8. **Dependencies & constraints** — other teams, platforms, legal/privacy, performance.
9. **Risks & open questions** — named, with owners.
10. **Measurement** — instrumentation/analytics plan to know if it worked.

## Process
1. Read the PRD fully first.
2. Rate each dimension: ✅ solid / 🟡 needs work / 🔴 missing — with a one-line reason.
3. List the **top gaps to fix before build**, most important first.
4. Pose the **open questions** the author must answer to be buildable.
5. End with a **verdict**: Ready / Ready with fixes / Not ready.

## Output format
A checklist table (dimension · rating · note), then **Top gaps**, **Open questions**, and the **verdict**. Be specific and kind; the goal is a better doc, not a teardown.
