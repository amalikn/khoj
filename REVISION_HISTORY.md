# Revision History

## 2026-03-13

### Summary
- Resolved local internal server errors on key UI routes after startup hardening work.
- Captured repeatable UI asset rebuild + sync workflow.

### Incident
- Affected routes:
  - `/chat`
  - `/home`
  - `/search`
- Browser-visible behavior:
  - internal server error pages while `GET /api/health` could still be healthy

### Root Cause
- Missing local built template assets:
  - `src/khoj/interface/built`
  - `src/khoj/interface/compiled`
  - `src/khoj/interface/home`

### Fix Applied
- Rebuilt frontend from `src/interface/web` (`npm install`, `npm run build`)
- Synced `src/interface/web/out/.` into `src/khoj/interface/built/`
- Added `src/khoj/interface/home/index.html` from built `index.html`
- Restarted local Khoj listener on `127.0.0.1:42110`

### Verification
- `GET /api/health` returned `200`
- Runtime template checks resolved:
  - `index.html`
  - `chat/index.html`
  - `search/index.html`
  - `home/index.html`
- `/chat`, `/home`, `/search` no longer failed due to missing templates
- `/server/` returns `404` by design in this local shape (admin remains at `/server/admin/login/`)

## 2026-03-12

### Summary
- Stabilized local native Khoj startup for MCP-driven autostart on macOS.
- Resolved admin login CSRF failures in local HTTP usage.

### Changes
- Added/validated native runtime dependency in autostart venv:
  - installed `mcp>=1.23.0` in `/Volumes/Data/_ai/_tool/tools-working-cache/khoj/venv`
- Standardized runtime dependency used in local environment:
  - `uvicorn==0.41.0`
- Updated `src/khoj/app/settings.py` local behavior:
  - local (`localhost`/`127.0.0.1`) now forces non-HTTPS cookie mode by default
  - host-only cookie domain behavior when `KHOJ_DOMAIN` is unset

### Verification
- `http://127.0.0.1:42110/api/health` returns `200`
- Admin login is reachable and usable
- `khoj-mcp` smoke tests pass:
  - `khoj_health` `READY`
  - `khoj_search` successful
  - ingest/get note round-trip successful

### Operational Notes
- Local data/runtime directories:
  - `/Volumes/Data/_ai/_tool/tools-data/khoj`
  - `/Volumes/Data/_ai/_tool/tools-runtime/khoj`
  - `/Volumes/Data/_ai/_tool/tools-working-cache/khoj/venv`
