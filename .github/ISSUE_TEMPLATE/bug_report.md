---
name: Bug report
about: Scannable ticket for broken behavior (outcome-focused, not a dump of logs)
title: ""
labels: bug
assignees: ""
---

## **Problem**

One or two sentences: what breaks for the operator/user, and what they see instead of the expected outcome. Link a related `#issue` if this is a follow-up.

…

## **Where**

Bullet the code paths, commands, or surfaces involved. Prefer enough for an agent to open the right files—not a full architecture recap already in `AGENTS.md` / `README.md`.

- …

## **Fix**

Numbered steps when order matters (`1.`, `2.`, …)—one sentence each. Prefer the intended outcome (fix + verify) over speculative refactors.

1. …
2. Add a regression test (or equivalent proof) that fails before and passes after.

Optional at end: **Out of scope:** …

## **How Do We Know We Are Done? (Acceptance Criteria)**

Three to six checkboxes; one verifiable outcome each. Do not copy Fix steps verbatim.

- [ ] Repro from Problem no longer occurs (or is clearly mitigated as described)
- [ ] Regression coverage at the right layer
- [ ] Docs updated if operator- or user-facing behavior changed

---

<details>
<summary><strong>Examples (delete before submitting)</strong></summary>

**Fix** — Problem: one sentence on broken behavior. Where: file/command. Fix: `1. Fix …` `2. Add regression test`. AC: repro gone; test green.

**Follow-up** — Problem: link prior `#issue`. Fix: only the remaining slice. AC: that slice verified.

</details>
