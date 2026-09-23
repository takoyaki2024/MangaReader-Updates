# MangaReader Updates

Public update channel for MangaReader.

Expected layout:

```text
MangaReader-Updates/
├─ latest.json
└─ MangaReader-Patch.zip
```

Only update metadata and the packaged patch belong here.

**Never publish:**
- source code from the private development repository
- `local_adapters/`
- `data/`
- library databases
- manga/image files
- tokens, credentials, or private configuration

The MangaReader application only accepts the fixed public patch URL from this repository and verifies the expected file size and SHA-256 before applying it. Update ordering is controlled by `app_version` plus a monotonic `build_sequence` so an older build is not installed over a newer one.
