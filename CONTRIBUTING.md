# Contributing to PM Skills

Thanks for helping make program management with Claude better. Contributions of new skills, improved templates, clearer descriptions, and bug fixes are all welcome.

## Ways to contribute

- **New skill** — a repeatable PM workflow not already covered.
- **Improve a skill** — sharper instructions, better output format, a useful template.
- **Fix triggering** — adjust a `description` so the skill activates on the right requests.
- **Docs** — clarify the README, fix typos, add examples.

## Skill format

Each skill is a folder under `skills/` containing a `SKILL.md`. Optional supporting files (templates, checklists, examples) live alongside it, typically in a `templates/` subfolder.

```
skills/<skill-name>/
├── SKILL.md
└── templates/
    └── <template>.md
```

### SKILL.md frontmatter

```markdown
---
name: skill-name
description: One or two sentences describing WHAT the skill does and WHEN to use it, written with trigger phrases a user would actually say. This is the only thing Claude sees when deciding whether to load the skill, so make it specific.
---
```

Rules:
- `name` must be lowercase, hyphen-separated, and **match the folder name**.
- `description` should name the artifact and include natural trigger phrases ("write a status report", "run a retro", "draft a charter"). Specific beats clever.
- Keep the body focused: what inputs to gather, how to do the work, and the exact output format.

### Body conventions

A good `SKILL.md` body covers:
1. **Purpose** — one line on the outcome.
2. **When to use / when not to use** — keep triggering precise.
3. **Inputs to gather** — what to ask the user for if missing (but don't over-interrogate; use sensible defaults).
4. **Process** — the steps Claude should follow.
5. **Output format** — the structure of the deliverable (link to a template if there is one).

Keep skills self-contained: a user should be able to copy one folder and have it work.

## Submitting a change

1. Fork and create a branch: `git checkout -b add-<skill-name>`.
2. Add or edit the skill. Test it by copying into `~/.claude/skills/` and trying a few realistic prompts.
3. Open a PR describing the skill and 2–3 example prompts that should trigger it.

## Conventions

- Markdown only for skill content; no external dependencies.
- Prefer prose templates teams can paste into Confluence/Notion/Docs.
- Keep output professional, concise, and decision-oriented — these are working PM artifacts.

## License

By contributing you agree your contributions are licensed under the repository's [MIT License](LICENSE).
