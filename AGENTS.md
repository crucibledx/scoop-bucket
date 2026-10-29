# Scoop Bucket — Agent Context

> Official Scoop bucket for Crucible tools (Windows).

## Identity

- **Repo:** `crucibledx/scoop-bucket`
- **License:** MIT

## What It Does

Provides Scoop manifests for installing Crucible tools on Windows. Currently contains only the `forge` manifest.

## Install

```powershell
scoop bucket add crucibledx https://github.com/crucibledx/scoop-bucket
scoop install forge
```

## Structure

```
bucket/
  forge.json         ← Scoop manifest for Forge CLI
LICENSE
README.md
```

## Manifest

`bucket/forge.json` covers Windows x64 only (`64bit` architecture, `forge-windows-x64.zip` from forge-cli GitHub
Releases). It has `checkver: github` and an `autoupdate` block, so Scoop can also resolve new versions on its own.

## Automation

This repo is **auto-updated** by the `scoop` job in the forge-cli release workflow (`crucibledx/forge-cli` `.github/workflows/release.yml`), which regenerates the whole manifest. When a new Forge version is tagged, CI automatically:
1. Updates `bucket/forge.json` with new version, URL, and SHA256 hash
2. Commits and pushes to this repo

**Manual edits are rare** — most changes come from the automated release pipeline.

## Adding a New Manifest

If a new Crucible CLI ships, add a new `bucket/<name>.json` following Scoop's manifest conventions.
