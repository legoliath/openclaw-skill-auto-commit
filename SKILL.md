---
name: auto-commit
description: Auto-commit untracked files and regenerate INVENTORY.md
version: 1.0.0
triggers:
  - auto-commit
  - commit workspace
  - inventory update
---

# Auto-Commit & Inventory

Commits all untracked and modified files in the OpenClaw workspace, then regenerates the inventory.

## Steps

1. Run: `bash ~/.openclaw/workspace/scripts/auto_commit.sh`
2. Check exit code
3. If errors, attempt to resolve (fix git conflicts, retry)
4. Report: number of files committed, push status, inventory updated or not

## Error Handling
- If git push fails (auth, conflict): report the error, do NOT retry indefinitely
- If inventory_generator.py fails: still report commit results

## Output
- On success: "✅ N files committed, inventory updated, pushed to origin"
- On failure: describe what failed
- If nothing to commit: "No changes to commit"