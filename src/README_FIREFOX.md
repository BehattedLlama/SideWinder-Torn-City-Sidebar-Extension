# SideWinder — Firefox Build

This folder contains a Firefox‑ready MV3 build.

Changes from upstream:
- Added `browser_specific_settings.gecko` with an explicit add‑on ID and `strict_min_version` 109.
- Ensured `host_permissions` explicitly include `https://www.torn.com/*`.
- Prepended a tiny namespace shim to JS files so both `chrome.*` and `browser.*` work.

## Testing
1) Open `about:debugging` in Firefox.
2) Click **This Firefox** → **Load Temporary Add-on…**.
3) Select this folder's `manifest.json`.
4) Visit https://www.torn.com/ and use the extension.

## AMO Submission
- Keep the add‑on ID stable (`sidewinder@novreske.dev`) so updates install cleanly.
- If you prefer another ID, edit it in `manifest.json` before building the ZIP.

