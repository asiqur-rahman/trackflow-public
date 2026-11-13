# TrackFlow (public)

Public assets for [TrackFlow](https://github.com/asiqur-rahman/plane-to-trackflow) self-hosted installs.

TrackFlow is open-source project management that unlocks customer value. The main application source and Docker images are published separately; this repository holds files that **must be reachable without authentication** — especially the Version Manifest used by Instance Admin “update available” checks.

## Version Manifest

Self-hosted Instances poll this JSON to learn the latest **stable** release (detect only — no remote Docker apply).

| | |
| --- | --- |
| File | [`version-manifest.json`](./version-manifest.json) |
| Raw URL | `https://raw.githubusercontent.com/asiqur-rahman/trackflow-public/main/version-manifest.json` |

Shape:

```json
{
  "channels": {
    "stable": {
      "version": "1.0.0",
      "released": "2026-11-13",
      "images": {
        "aio": "asiqurrahman/trackflow:production",
        "mcp": "asiqurrahman/trackflow-mcp:production",
        "db": "asiqurrahman/trackflow-db:production"
      }
    }
  }
}
```

Point your Instance at the raw URL:

```bash
TRACKFLOW_VERSION_MANIFEST_URL=https://raw.githubusercontent.com/asiqur-rahman/trackflow-public/main/version-manifest.json
```

This file is updated automatically by the TrackFlow release pipeline after each Docker Hub publish.

## Docker images

| Image | Hub |
| --- | --- |
| All-in-one app | `asiqurrahman/trackflow:production` |
| MCP edge | `asiqurrahman/trackflow-mcp:production` |
| Postgres | `asiqurrahman/trackflow-db:production` |

## License

TrackFlow application code is AGPL-3.0. See the main repository for terms.
