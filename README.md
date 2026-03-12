# Install Release Tools

This repository contains the `install-release-tools` agent skill.

## Purpose

Install or update ElegantChaos ReleaseTools so the `rt` command is available via Mint. Use when a user asks to install, reinstall, refresh, or update ReleaseTools/`rt`, or when release automation depends on `rt` being present.

## Compatibility

- Agent hosts: Codex-compatible skill hosts
- Publication class: `portable-with-prereqs`

## Prerequisites

Mint and access to the ReleaseTools package

## Shared Baseline

This skill does not require the shared agents baseline.

## Relationship To `agents`

On machines using the shared agents control-plane repository, this skill is typically checked out under `~/.local/share/skills/` and linked into `~/.agents/skills` or `~/.codex/skills`.
This repository is the public repo-per-skill source used for sharing, maintenance, and refresh workflows.

## Contents

- `SKILL.md`
- `agents/openai.yaml` when host metadata is needed
- optional support folders such as `references/`, `assets/`, or `scripts/`

## Local Notes

Environment-coupled through Mint and ReleaseTools.
