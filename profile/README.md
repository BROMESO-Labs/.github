# BROMESO Labs

Software products built with precision. We build vertical SaaS for regulated and high-complexity industries.

---

## Active Projects

| Repo | Description | Stack | Status |
|------|-------------|-------|--------|
| [automotive-crm](https://github.com/BROMESO-Labs/automotive-crm) | CRM for automotive dealerships and service networks | — | Active |
| [occupational-health](https://github.com/BROMESO-Labs/occupational-health) | Occupational health management platform | Next.js | Active |
| [md-library](https://github.com/BROMESO-Labs/md-library) | Team knowledge base — projects, features, fixes, plans | Obsidian/Markdown | Active |

---

## Team Knowledge Base

All projects share a central KB at [`BROMESO-Labs/md-library`](https://github.com/BROMESO-Labs/md-library).

**What lives there:**

- `projects/{slug}/overview.md` — stack, repo, team, current milestone
- `projects/{slug}/backlog.md` — feature backlog with status tracking, ready for any dev to pick up
- `changes/{slug}/{features|fixes|refactors}/` — chronological record of every significant change
- `plans/{slug}/` — implementation plans and SDD documents produced by Claude Code

**What does NOT live there:** secrets, credentials, internal URLs. Those go in `_private/` which is gitignored.

---

## Dev Conventions

### Branching
Default working branch is `develop`. PRs target `develop`; `main` is for releases.

### Commits
[Conventional Commits](https://www.conventionalcommits.org/) strictly. No AI attributions.

### Claude Code
Every project repo includes a `CLAUDE.md` (or references one via `@AGENTS.md`) that instructs Claude Code on project-specific rules. All BROMESO repos include a **Knowledge Base Sync** section that tells Claude to update `md-library` after every significant change — feature, fix, refactor, or plan.

The KB sync is scoped: it only fires within BROMESO Labs repos. Claude Code working on external or personal projects does not touch `md-library`.

### Onboarding a new project

1. Clone `md-library` locally.
2. Create `projects/{your-slug}/overview.md` and `projects/{your-slug}/backlog.md` from the templates in `_templates/`.
3. Update `_index.md` with the new project row.
4. Add the KB Sync block from `_templates/claude-md-snippet.md` to your repo's `CLAUDE.md`, replacing `{project-slug}` with your actual slug.
5. Push.

### Adding a backlog item

Edit `projects/{slug}/backlog.md` directly. Copy the snippet from `_templates/backlog-item.md`. Status flow:

```
idea → planned → in-progress → review → done
                                       → cancelled
```

Any dev can claim an item by setting `Assignee` and moving it to `in-progress`.

---

## Contact

BROMESO Labs — private organization. Internal use only.
