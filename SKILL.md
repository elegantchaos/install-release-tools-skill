---
name: install-release-tools
description: Install or update ElegantChaos ReleaseTools so the `rt` command is available via Mint. Use when a user asks to install, reinstall, refresh, or update ReleaseTools/`rt`, or when release automation depends on `rt` being present.
---

# Install Release Tools

Install or update ReleaseTools via Mint and confirm that `rt` is available.

Read `references/workflow.md` before running commands.

## Use This Skill When

- the user asks to install, reinstall, refresh, or update ReleaseTools or `rt`
- a workflow depends on `rt` and the command is missing

## Workflow

1. Check whether `mint` exists.
2. If `mint` is missing, use the `install-mint` skill first.
3. Follow the install/update workflow in `references/workflow.md`.
4. Emit exactly one final status line using the wording rules in `references/workflow.md`.

## References

- `references/workflow.md`: full ReleaseTools install/update workflow, Mint dependency handling, status-line rules, and failure handling
