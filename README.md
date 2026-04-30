# Pactor PMO · Public State Hub

This repository serves as the **public publishing endpoint** for the Pactor PMO Live Artifact state file.

## What is this?

A single JSON file (`pactor-state.json`) representing the consolidated state of the Pactor product management dashboard. The actual product code lives in a private repository — this repo only mirrors the derived state for the PMO HTML's "Sync from repo" feature to fetch.

## What is NOT here

- Product source code
- Database schemas
- Extraction prompts
- Customer data
- API keys, secrets, or credentials

## Live URL

Fetch the latest state at:

```
https://raw.githubusercontent.com/pactor-app/pactor-pmo-state/main/pactor-state.json
```

## Update mechanism

This file is auto-published by a GitHub Action in the private `pactor-app/pactor-app` repository. Every push to `data/snapshots/` or `data/patches/` in the private repo triggers:

1. Consolidation of snapshots + patches into `pactor-state.json`
2. Commit to the private repo
3. Cross-repo push to this public repo

Last updated: 2026-04-30T16:23:31Z

## Manual contributions

Direct edits to this repo are **not accepted** — all changes flow from the private source. PRs against this repo will be closed.

---

Maintained by the Pactor PMO automation pipeline.
