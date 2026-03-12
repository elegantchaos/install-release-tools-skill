<p align="center">
    <img src="assets/logo.svg" alt="Install Release Tools - Agent Skill" height="100" />
</p>

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

## Contents

- `SKILL.md`
- `agents/openai.yaml` when host metadata is needed
- optional support folders such as `references/`, `assets/`, or `scripts/`

