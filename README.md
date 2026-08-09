# Scoop Bucket — Crucible

Official [Scoop](https://scoop.sh) bucket for [Crucible](https://crucibledx.dev) tools.

## Install

```powershell
scoop bucket add crucibledx https://github.com/crucibledx/scoop-bucket
scoop install forge
```

## Available Manifests

| Manifest | Description |
|----------|-------------|
| `forge`  | One source of truth for every AI tool your team uses |

## Usage

```powershell
scoop bucket add crucibledx https://github.com/crucibledx/scoop-bucket
scoop install forge
scoop update forge
```

## How it works

When a new Forge CLI version is released, the [release workflow](https://github.com/crucibledx/forge-cli/blob/main/.github/workflows/release.yml) automatically updates the manifest in this repo with the correct version, URL, and SHA256 hash.

## License

[MIT](LICENSE)
