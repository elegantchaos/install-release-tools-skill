# Install ReleaseTools Workflow

## Commands

Check whether `mint` exists:

```bash
which mint
```

Check whether `rt` is already installed and capture its version and path:

```bash
which rt
rt --version
```

Install or update ReleaseTools:

```bash
mint install ReleaseTools
```

Capture the resolved executable path and post-install version:

```bash
which rt
rt --version
```

## Decision Rules

- If `mint` is missing, use the `install-mint` skill first, then continue only after `which mint` succeeds.
- If `which rt` resolves outside `$HOME/.mint/bin`, treat it as a non-Mint install and stop with:
  `ReleaseTools <version> installed (not via Mint).`

## Status Line Rules

Emit exactly one final status line:

- If ReleaseTools was not installed before install and is installed after:
  `ReleaseTools <version> installed.`
- If ReleaseTools was installed before install from `$HOME/.mint/bin` and the version changed:
  `ReleaseTools <old_version> updated to <new_version>.`
- If ReleaseTools was installed before install from `$HOME/.mint/bin` and the version is unchanged:
  `ReleaseTools <version> already installed.`
- If ReleaseTools was installed before install from outside `$HOME/.mint/bin`:
  `ReleaseTools <version> installed (not via Mint).`

If installation fails, report actionable Mint error details and do not emit one of the success status lines.

## Notes

- `mint install ReleaseTools` is the canonical command for both install and update.
- Use `which rt` rather than `mint which rt` to detect whether `rt` is installed at all.
- Parse `<version>` from `rt --version` output. For example, from `ReleaseTools 4.0.1 (1)` use `4.0.1`.
- Determine "via Mint" by checking whether the resolved `rt` path is within `$HOME/.mint/bin`.
- Do not modify shell startup files in this skill. If PATH issues appear, report them and ask the user before making environment changes.
