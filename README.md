# Celem Payloads

Public launcher manifest hosting for CelemLauncher artifact tests.

Current files:
- `package/launcher_manifest.json` points launcher self-updates to GitHub Release assets in this repository.
- `package/CelemUX.dll` is the primary public CelemUX DLL consumed by CelemLauncher.
- `package/BepInEx-BepInExPack_V_Rising-1.733.2.zip` is the primary public BepInEx V Rising pack consumed by CelemLauncher. The manifest falls back to the matching Thunderstore download.
- `package/manifest.json` is the primary CelemLauncher game payload manifest. Its CelemUX entry points to the public GitHub-hosted DLL first and uses Supabase Storage as the download fallback. Launcher update ZIP assets are intentionally not published here.
