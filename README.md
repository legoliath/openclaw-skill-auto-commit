# 🚀 openclaw-skill-auto-commit

Auto-commit untracked files and regenerate INVENTORY.md

![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue) ![Status](https://img.shields.io/badge/Status-Active-green)

## Overview

The `openclaw-skill-auto-commit` is designed to automate the process of committing untracked and modified files within your OpenClaw workspace. After a successful commit, it also regenerates the `INVENTORY.md` file, ensuring your workspace documentation is always up-to-date.

## Features

- **Automated Commits**: Automatically stages and commits all untracked and modified files in the OpenClaw workspace.
- **Inventory Regeneration**: Ensures `INVENTORY.md` is regenerated after each commit, maintaining an accurate record of your project.
- **Error Handling**: Provides basic error handling for `git push` failures and issues during `inventory_generator.py` execution, reporting errors without halting the process.

## Installation

To use this skill, place the `auto-commit` directory into your OpenClaw `skills` directory:

```bash
cp -R auto-commit ~/.openclaw/workspace/skills/
```

## Usage

This skill is typically invoked via a script that runs within your OpenClaw environment. The `SKILL.md` indicates the primary script to execute is `auto_commit.sh`.

```bash
bash ~/.openclaw/workspace/scripts/auto_commit.sh
```

> [!NOTE]
> The skill expects an `auto_commit.sh` script to be present in `~/.openclaw/workspace/scripts/` to perform its actions.

## Configuration

This skill does not require specific configuration files beyond its placement in the OpenClaw skills directory. Its behavior is primarily driven by the `auto_commit.sh` script.

## File Structure

```
.
└── auto-commit/
    └── SKILL.md
```
