# Tülay's personal GitHub profile — shared agent instructions

Read `README.md` or `profile/README.md` (whichever exists), then `HANDOFF.md` before editing. Claude Code also reads this through `CLAUDE.md`; Codex uses this file.

## Project scope
This repository contains a personal GitHub profile `README.md`, not the TestGatify product or Operations code. Preserve professional experience descriptions and links; do not present planned TestGatify work as completed or reveal private business details.

## Working rules
- Treat this repository as **public**. Do not include private Operations plans, client/employer records, financial information, secrets, unpublished materials or credentials.
- Check Git status and current remote first. Never overwrite uncommitted work; use a separate branch and PR for changes. Do not rename repositories or publish claims without verification.
- Start each session by checking `HANDOFF.md` for the most recent progress and intended next step.
- End each meaningful task by updating `HANDOFF.md` with what changed, validations performed, PR/branch reference, and exact next step; keep updates concise.
- Codex and Claude Code **do not share chat history**. Handoff files only synchronize after being committed/pushed and pulled locally; other repositories do not auto-sync.
- Do not edit other repositories from this profile workspace without explicitly switching to and inspecting that repository.
## Persistent local Git synchronization

At the start of every work session, before editing files:
1. Run `git status --short --branch` to inspect the branch and local changes, then `git fetch origin`.
2. If the worktree is clean and the tracked upstream is only ahead, run `git pull --ff-only`. Continue if it is already current.
3. If there are local changes, conflicts, divergent branches, no tracked upstream, or a fetch/pull failure, preserve everything and report the blocker to the user. Do not reset, rebase, stash, or overwrite work to force synchronization.
4. After the Git check and any safe update, read `AGENTS.md`, `CLAUDE.md`, and `HANDOFF.md`, then the repository-specific files named above.
5. At the end of each meaningful task, update `HANDOFF.md` with changes, verification, and the next step. The update reaches other local copies only after commit and push.

This routine applies to the current local repository; it does not synchronize other repositories or chat histories.
