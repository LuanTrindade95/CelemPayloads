# Celem Payloads

Public launcher manifest hosting for CelemLauncher artifact tests.

Current files:
- `package/launcher_manifest.json` points launcher self-updates to GitHub Release assets in this repository.
- `package/CelemUX.dll` is the primary public CelemUX DLL consumed by CelemLauncher.
- `package/manifest.json` is the primary CelemLauncher game payload manifest. Its CelemUX entry points to the public GitHub-hosted DLL first and uses Supabase Storage as the download fallback.
