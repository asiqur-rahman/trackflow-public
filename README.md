# TrackFlow (public)

Public assets for self-hosted [TrackFlow](https://github.com/asiqur-rahman/plane-to-trackflow) installs.

TrackFlow is open-source project management that unlocks customer value. This repository holds files that **must be reachable without authentication** — especially the Version Manifest used by Instance Admin “update available” checks.

## Zero configuration on Instances

Self-hosted TrackFlow ships with this Manifest URL baked in. Operators do **not** set any env var. After each Docker Hub release, Jenkins updates `version-manifest.json` here automatically; Instances pick it up on the next Help check.

## Version Manifest

| | |
| --- | --- |
| File | [`version-manifest.json`](./version-manifest.json) |
| Raw URL | `https://raw.githubusercontent.com/asiqur-rahman/trackflow-public/main/version-manifest.json` |

## Docker images

| Image | Hub |
| --- | --- |
| All-in-one app | `asiqurrahman/trackflow:production` |
| MCP edge | `asiqurrahman/trackflow-mcp:production` |
| Postgres | `asiqurrahman/trackflow-db:production` |

## License

TrackFlow application code is AGPL-3.0. See the main repository for terms.
