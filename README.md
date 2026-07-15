# QwenPaw-test-bench

Reconstructed pull requests from `agentscope-ai/QwenPaw`, rebuilt in this fresh
repository for **grading AI code-review quality**.

Each original PR `N` is recreated as three branches that share a single base:

| branch          | meaning                                                             |
|-----------------|---------------------------------------------------------------------|
| `pr-N-base`     | the base the PR branched from (state of `main` at the branch point) |
| `pr-N-flawed`   | the code **as the reviewer first saw it, before the fix**           |
| `pr-N-fixed`    | the **corrected, pre-merge** code                                   |

Two pull requests are opened, **both targeting `pr-N-base`**:

- **`pr-N-flawed` → `pr-N-base`**
- **`pr-N-fixed` → `pr-N-base`**

The two PRs are deliberately alike from the outside: they carry the **same title and
description** (the original PR's) and each is a **single commit** on top of the shared
base. Only the code differs — one still contains the issue review caught, the other has
it resolved. A merge of `main` that happened partway through the original PR is squashed
out, so each PR's diff shows only the author's own changes.

## Why a separate repo?

The source PRs are already merged. Pointed at the real PR, a reviewer agent could cheat
off the existing review comments, the follow-up commits, and the merge outcome. Those
are absent here — the reconstructed PRs carry no links, review text, or fix-commit
messages. The ground truth (the real review comments and the fix) is kept **outside**
this repository.

> Please do not add comments that leak the intended answer onto the flawed PRs.
