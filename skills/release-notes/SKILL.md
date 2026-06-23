---
name: release-notes
argument-hint: [changelog/PRs + audience]
description: Write audience-appropriate release notes from a changelog, list of merged PRs, or feature list — grouped by type, in user-benefit language. Use when the user says "write release notes", "changelog", "what's new", "announce this release", or wants to turn a list of changes into customer- or internal-facing notes.
---

# Release Notes

Turn a list of changes into release notes written for the reader — what they can now do, not what you merged.

## When to use
- Announcing a release (customer-facing or internal).
- Converting a changelog / PR list into readable notes.

## Inputs to gather
- Source of truth: changelog, merged PRs, ticket list, or feature summary.
- **Audience** — end users, customers/admins, or internal team (this drives tone and detail).
- Version/date and any highlights to feature.

## Process
1. Group changes into: **✨ New / 🔧 Improved / 🐛 Fixed**, plus **⚠️ Breaking changes** and **🗑️ Deprecated** when relevant.
2. Rewrite each in **benefit language** — lead with what the user can now do; drop internal jargon, ticket IDs (or move to an appendix), and implementation detail.
3. **Lead with highlights** — the 1–3 changes most people care about, optionally with a short intro.
4. Match **tone** to audience: warm and benefit-led for customers; precise and complete for internal/technical.
5. Call out **breaking changes** prominently with required actions and migration steps.
6. Be honest and complete on fixes that affected users; don't bury security/data fixes.

## Output format
```
# {{Product}} {{version}} — {{date}}

{{1–2 sentence highlight intro, optional}}

## ✨ New
- **{{Feature}}** — {{what you can now do}}.

## 🔧 Improvements
- {{benefit}}

## 🐛 Fixes
- {{what's fixed, from the user's view}}

## ⚠️ Breaking changes
- **{{change}}** — {{required action / migration}}.
```
Omit empty sections. Keep entries short and skimmable.
