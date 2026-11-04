# AGENTS.md

Implementation guide for coding agents working in repos **created from** [`danielnachumdev/template`](https://github.com/danielnachumdev/template), or editing the template itself.

Product pitch for humans: [`README.md`](README.md).

---

## Orientation

| Question | Answer |
| -------- | ------ |
| What is this? | Starter scaffold: Actions CI + Dependabot + CODEOWNERS + CapA + this file |
| CI hub | [`danielnachumdev/actions`](https://github.com/danielnachumdev/actions) pinned `@latest` |
| Thin orchestrator | [`.github/workflows/ci.yml`](.github/workflows/ci.yml) |
| CapA | [`capabilities.yaml`](capabilities.yaml) — run `capa install` (do not hand-edit generated `.cursor/` / `.claude/`) |
| Semver | **Omitted** until the repo publishes releases/wheels — then copy Semver jobs from actions templates |
| Secrets | Never commit tokens, keys, or live operator inventory; use dummy data in fixtures/PRs |

## After “Use this template”

1. Rename the product in `README.md` and rewrite this orientation table for the real codebase.
2. Add the language layout (`pyproject.toml` / `package.json` / etc.). Detect turns on the matching CI lanes.
3. Drop `allow-empty: true` from `ci.yml` once at least one lane is real (empty-layout success is only for the bare template).
4. Extend Dependabot (`pip` / `uv` / `npm`) when those ecosystems exist; keep `github-actions`.
5. Create label `dependencies` before Dependabot runs. Add Semver bump labels **only** if adopting Semver.
6. Protect `main` with required check **`CI / CI`** (and **`Semver / Semver`** only if Semver is wired).

Shared adopt docs: [actions HOW-TO-USE](https://github.com/danielnachumdev/actions/blob/latest/HOW-TO-USE.md).

## Editing the template repo itself

Keep the scaffold **language-agnostic**. Prefer `allow-empty: true` so CI stays green without inventing a dummy `pyproject.toml`. Do not add Semver here.
