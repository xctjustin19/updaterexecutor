# Vertex Executor updates

This repo is the update channel for Vertex Executor.

Players never clone this. The app reads `version.json` and downloads the matching GitHub Release zip.

## Publish a new required build

1. Bump `<Version>` in `quorum-ui/QuorumUI.csproj` (example `1.0.1`).
2. From `Roblox executor` run:

```powershell
.\pack-release.ps1 -Publish
```

That builds the dist folder, zips it, creates GitHub release `v1.0.1`, and updates `version.json`.

Older executors then show **Update required** and will not run until the player updates.
