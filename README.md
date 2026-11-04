# template

**GitHub template** for new [danielnachumdev](https://github.com/danielnachumdev) repositories.

Use this when starting a repo so CI, agent docs, and capa are already wired — then replace the placeholder product text with the real project.

## What’s included

| Piece | Role |
| ----- | ---- |
| [`.github/workflows/ci.yml`](.github/workflows/ci.yml) | Thin CI → [`danielnachumdev/actions`](https://github.com/danielnachumdev/actions) `@latest` |
| [`.github/dependabot.yml`](.github/dependabot.yml) | Weekly pip / npm / github-actions (no `noBump` — Semver off) |
| [`.github/CODEOWNERS`](.github/CODEOWNERS) | Default owner `@danielnachumdev` |
| [`AGENTS.md`](AGENTS.md) | Orientation for coding agents |
| [`capabilities.yaml`](capabilities.yaml) | CapA source of truth ([capa.sh](https://capa.sh/)) |

**actions HOW-TO-USE already applied on this repo:** thin `ci.yml` `@latest`, CODEOWNERS + Dependabot, `dependencies` label, soft `main` protection (`CI / CI`, reviews count 0, code-owner reviews off for Dependabot merge, admin bypass), security alerts/scanning, Dependabot auto-merge + `allow_auto_merge`. Semver / `cd.yml` / bump labels omitted on purpose.

## Create a repo from this template

1. On GitHub: **Use this template** → create the new repository.
2. Clone it under `~/dev/projects/<name>/`.
3. Edit `README.md` / `AGENTS.md` for the product; add `pyproject.toml` and/or `package.json` as needed.
4. CI Detect picks up language lanes automatically (`allow-empty` can be removed once a lane exists).
5. Re-apply HOW-TO-USE steps 3–5 on the **new** repo (labels, soft branch protection, security) — GitHub does not copy those from the template.
6. Optional: `capa install` after editing `capabilities.yaml`.

## Local clone of the template itself

```bash
gh repo clone danielnachumdev/template ~/dev/projects/template
cd ~/dev/projects/template
```

## CI

Required check on `main`: **`CI / CI`**. Pin **`@latest`**. Checklist: [actions HOW-TO-USE](https://github.com/danielnachumdev/actions/blob/latest/HOW-TO-USE.md).
