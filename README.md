# Celem Payloads

Public launcher manifest hosting for CelemLauncher artifact tests.

Current files:
- `package/launcher_manifest.json` points launcher self-updates to GitHub Release assets in this repository.
- `package/CelemUX.dll` is the primary public CelemUX DLL consumed by CelemLauncher.
- `package/BepInEx-BepInExPack_V_Rising-1.733.2.zip` is the primary public BepInEx V Rising pack consumed by CelemLauncher. The manifest falls back to the matching Thunderstore download.
- `package/manifest.json` is the primary CelemLauncher game payload manifest. Its CelemUX entry points to a commit-pinned GitHub raw URL so the SHA-256 and artifact cannot diverge through branch/CDN caching. Launcher update ZIP assets are intentionally not published here.

## Publishing CelemUX

Publish the DLL commit first, then update `package/manifest.json` in a separate commit to reference that immutable commit SHA and its SHA-256. Never point a new hash at `raw.githubusercontent.com/.../main/...`: a stale branch-cache response can otherwise be rejected by the launcher even though the manifest is valid.
