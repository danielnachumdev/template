# template

**GitHub template** for new [danielnachumdev](https://github.com/danielnachumdev) repositories.

Use this when starting a repo so CI, agent docs, and capa are already wired — then replace the placeholder product text with the real project.

## What’s included

| Piece | Role |
| ----- | ---- |
| [`.github/workflows/ci.yml`](.github/workflows/ci.yml) | Thin CI → [`danielnachumdev/actions`](https://github.com/danielnachumdev/actions) `@latest` |
| [`.github/dependabot.yml`](.github/dependabot.yml) | Weekly GitHub Actions updates |
| [`.github/CODEOWNERS`](.github/CODEOWNERS) | Default code owner |
| [`AGENTS.md`](AGENTS.md) | Orientation for coding agents |
| [`capabilities.yaml`](capabilities.yaml) | CapA source of truth ([capa.sh](https://capa.sh/)) |

Semver CD is **not** included. Add it only when the new repo publishes versioned artifacts (see [actions HOW-TO-USE](https://github.com/danielnachumdev/actions/blob/latest/HOW-TO-USE.md)).

## Create a repo from this template

1. On GitHub: **Use this template** → create the new repository.
2. Clone it under `~/dev/projects/<name>/`.
3. Edit `README.md` / `AGENTS.md` for the product; add `pyproject.toml` and/or `package.json` as needed.
4. CI Detect picks up language lanes automatically (`allow-empty` can be removed once a lane exists).
5. Optional: `capa install` after editing `capabilities.yaml`.

## Local clone of the template itself

```bash
gh repo clone danielnachumdev/template ~/dev/projects/template
cd ~/dev/projects/template
```

## CI

Required check to protect `main`: **`CI / CI`**.

Pin stays **`@latest`**. Full adopt checklist: [actions HOW-TO-USE](https://github.com/danielnachumdev/actions/blob/latest/HOW-TO-USE.md).
