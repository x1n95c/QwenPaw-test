# QwenPaw-test-bench

Reconstructed pull requests from `agentscope-ai/QwenPaw`, rebuilt in this fresh
repository for **grading AI code-review quality**.

Each original PR is recreated as a triple of branches sharing a common base:

| branch            | meaning                                                        |
|-------------------|----------------------------------------------------------------|
| `pr-<N>-base`     | the base the PR branched from (state of `main` at branch point)|
| `pr-<N>-flawed`   | the code **as the reviewer saw it, before the fix** — review this |
| `pr-<N>-fixed`    | the **pre-merge** code — the reference "answer"                |

Two PRs are opened per original PR:

- **`pr-<N>-flawed` → `pr-<N>-base`** — point the AI reviewer here.
- **`pr-<N>-fixed` → `pr-<N>-base`** — the reference solution.

## Why a separate repo?

The source PRs are already merged. Pointed at the real PR, an agent could cheat by
reading the existing review comments, the follow-up commits, and the merge outcome.
Here none of that is present: the flawed PR carries no links, review text, or fix
messages. Ground truth (real review comments + fix diff) is kept **outside** this repo.

> Please do not add comments that leak the intended answer onto the flawed PRs.
