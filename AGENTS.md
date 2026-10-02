# AGENTS.md — status

The Upptime status page at `status.pacestreak.com` (MIT). Branch: `master`.

Workspace-wide rules (CSP, cookies, privacy, commit conventions, what is
already decided) live in the root
[`AGENTS.md`](https://github.com/PaceStreak/pacestreak/blob/main/AGENTS.md).
Read it first; this file only adds what is specific to this repository.

## Rules for this repo

- **`git pull` first.** Upptime commits here every few minutes; a stale clone
  once made a healthy pipeline look dead.
- Edit only `.upptimerc.yml` and the hand-written parts of `README.md`
  (outside the `start`/`end` markers). `.github/workflows` is generated;
  workflow changes must be pushed over SSH because `GITHUB_TOKEN` cannot
  write there.
- Pin `slug` on every monitor, or renaming it orphans its history.
- Add a monitor only once the host actually responds, or the page shows a
  permanent outage.
- SSL checks take a bare hostname, not a URL.

## Commits

Conventional commits, subject says what, body says why. Commit as
`AlzyWelzy <welzyalzy@gmail.com>`. **Never credit an AI tool**: no
`Co-Authored-By` trailer and no "Generated with" line, in commits or PRs.
This repository is public, so never commit a secret.
