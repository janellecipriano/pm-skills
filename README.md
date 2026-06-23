# PM Skills for Claude — Program Management for Product Development

A collection of open-source [Claude skills](https://docs.claude.com/en/docs/claude-code/skills) that turn Claude into a capable program management partner for product teams. Each skill encodes a repeatable PM workflow — drafting a charter, writing a status report, running a launch-readiness review — so you get consistent, well-structured output every time instead of starting from a blank page.

Built for program managers, product managers, TPMs, and team leads who want their day-to-day artifacts (charters, status updates, RAID logs, roadmaps, retros, postmortems) produced quickly and to a high standard.

> **License:** MIT — free to use, modify, and share. See [LICENSE](LICENSE). Contributions welcome; see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## What's in the box

19 skills organized into four groups.

### Core PM
| Skill | What it does |
| --- | --- |
| [`project-charter`](skills/project-charter) | Draft a kickoff charter: problem, goals, scope, success metrics, team, timeline. |
| [`status-report`](skills/status-report) | Produce a crisp status report with RAG health, progress, risks, and asks. |
| [`raid-log`](skills/raid-log) | Build and maintain a RAID log (Risks, Assumptions, Issues, Dependencies). |
| [`roadmap-planning`](skills/roadmap-planning) | Turn goals and initiatives into a now/next/later or quarterly roadmap. |
| [`launch-readiness`](skills/launch-readiness) | Run a go/no-go launch-readiness review across all functions. |
| [`retrospective`](skills/retrospective) | Facilitate and write up a retro with actionable, owned follow-ups. |
| [`decision-log`](skills/decision-log) | Capture decisions (and the reasoning) in a durable, searchable log. |

### Discovery & Planning
| Skill | What it does |
| --- | --- |
| [`prd-review`](skills/prd-review) | Review a PRD against a quality checklist and surface gaps before build. |
| [`sprint-planning`](skills/sprint-planning) | Plan a sprint/iteration: goal, capacity, committed scope, risks. |
| [`dependency-mapping`](skills/dependency-mapping) | Map cross-team dependencies, owners, dates, and the critical path. |
| [`estimation-sizing`](skills/estimation-sizing) | Facilitate estimation and turn sizes into a credible delivery range. |

### Stakeholder Communications
| Skill | What it does |
| --- | --- |
| [`exec-summary`](skills/exec-summary) | Distill a program update into a one-screen executive summary. |
| [`stakeholder-comms-plan`](skills/stakeholder-comms-plan) | Build a stakeholder map and a cadence-based communication plan. |
| [`escalation`](skills/escalation) | Draft a clear, unemotional escalation with a specific ask. |
| [`release-notes`](skills/release-notes) | Write audience-appropriate release notes from a changelog or PRs. |

### Metrics & Ops
| Skill | What it does |
| --- | --- |
| [`okr-tracking`](skills/okr-tracking) | Draft and track OKRs with measurable key results and confidence. |
| [`postmortem`](skills/postmortem) | Run a blameless postmortem with timeline, root cause, and actions. |
| [`capacity-planning`](skills/capacity-planning) | Model team capacity vs. committed demand and flag over-allocation. |
| [`program-health-dashboard`](skills/program-health-dashboard) | Assemble a one-page program health snapshot across workstreams. |

---

## Installation

These are standard Claude skills — a folder with a `SKILL.md` file. Claude loads a skill automatically when your request matches its description.

### Option A — Personal skills (use everywhere)
Copy the skills you want into your personal skills directory:

```bash
git clone https://github.com/janellecipriano/pm-skills.git
mkdir -p ~/.claude/skills
cp -R pm-skills/skills/* ~/.claude/skills/
```

### Option B — Project skills (share with a repo/team)
Copy them into a project so they ship with your repo:

```bash
mkdir -p /path/to/your-project/.claude/skills
cp -R pm-skills/skills/* /path/to/your-project/.claude/skills/
```

Commit `.claude/skills/` and everyone on the project gets them.

### Option C — Pick just what you need
Each skill is self-contained. Copy a single folder:

```bash
cp -R pm-skills/skills/status-report ~/.claude/skills/
```

> **Note on clients:** Skills work in Claude Code and the Claude apps that support skills. Personal skills live in `~/.claude/skills/`; project skills live in `<project>/.claude/skills/`.

---

## Using a skill

Just ask Claude in plain language — it picks the matching skill:

- *"Draft a project charter for our new onboarding revamp."* → `project-charter`
- *"Write this week's status report; we slipped the API work by 3 days."* → `status-report`
- *"Are we ready to launch? Run a readiness check."* → `launch-readiness`
- *"Turn these notes into a blameless postmortem."* → `postmortem`

You can also name a skill explicitly: *"Use the raid-log skill to log this new dependency on the payments team."*

---

## How these skills are structured

Every skill follows the same shape so they're easy to read, fork, and extend:

```
skills/<skill-name>/
├── SKILL.md          # The instructions Claude follows (name + description frontmatter)
└── templates/        # Optional starter templates the skill fills in
```

`SKILL.md` frontmatter (`name`, `description`) is what Claude uses to decide when to trigger the skill. The body tells Claude how to gather inputs, what to produce, and the output format.

---

## Contributing

PRs and issues are welcome — new skills, better templates, fixes to triggering. See [CONTRIBUTING.md](CONTRIBUTING.md) for the skill format and conventions. Be excellent to each other ([Code of Conduct](CODE_OF_CONDUCT.md)).

Release history lives in the [CHANGELOG](CHANGELOG.md).

## License

[MIT](LICENSE) © 2026 Janelle Cipriano. Use it, fork it, share it with your community.
