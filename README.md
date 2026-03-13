<p align="center"><img src="https://assets.khoj.dev/khoj-logo-sideways-1200x540.png" width="230" alt="Khoj Logo"></p>

<div align="center">

[![test](https://github.com/khoj-ai/khoj/actions/workflows/test.yml/badge.svg)](https://github.com/khoj-ai/khoj/actions/workflows/test.yml)
[![docker](https://github.com/khoj-ai/khoj/actions/workflows/dockerize.yml/badge.svg)](https://github.com/khoj-ai/khoj/pkgs/container/khoj)
[![pypi](https://github.com/khoj-ai/khoj/actions/workflows/pypi.yml/badge.svg)](https://pypi.org/project/khoj/)
[![discord](https://img.shields.io/discord/1112065956647284756?style=plastic&label=discord)](https://discord.gg/BDgyabRM6e)

</div>

<div align="center">
<b>Your AI second brain</b>
</div>

<br />

<div align="center">

[📑 Docs](https://docs.khoj.dev)
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
[🌐 Web](https://khoj.dev)
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
[🔥 App](https://app.khoj.dev)
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
[💬 Discord](https://discord.gg/BDgyabRM6e)
<span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
[✍🏽 Blog](https://blog.khoj.dev)

<a href="https://trendshift.io/repositories/10318" target="_blank"><img src="https://trendshift.io/api/badge/repositories/10318" alt="khoj-ai%2Fkhoj | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

</div>

***

### 🎁 New
* Meet 🌶️ **[Pipali](https://pipali.ai)** - our [open-source](https://github.com/khoj-ai/pipali) AI coworker that runs on your computer.
* [Read](https://blog.khoj.dev/posts/evaluate-khoj-quality/) about Khoj's excellent performance on modern retrieval and reasoning benchmarks.

***

## Overview

[Khoj](https://khoj.dev) is a personal AI app to extend your capabilities. It smoothly scales up from an on-device personal AI to a cloud-scale enterprise AI.

- Chat with any local or online LLM (e.g llama3, qwen, gemma, mistral, gpt, claude, gemini, deepseek).
- Get answers from the internet and your docs (including image, pdf, markdown, org-mode, word, notion files).
- Access it from your Browser, Obsidian, Emacs, Desktop, Phone or Whatsapp.
- Create agents with custom knowledge, persona, chat model and tools to take on any role.
- Automate away repetitive research. Get personal newsletters and smart notifications delivered to your inbox.
- Find relevant docs quickly and easily using our advanced semantic search.
- Generate images, talk out loud, play your messages.
- Khoj is open-source, self-hostable. Always.
- Run it privately on [your computer](https://docs.khoj.dev/get-started/setup) or try it on our [cloud app](https://app.khoj.dev).

***

## See it in action

![demo_chat](https://github.com/khoj-ai/khoj/blob/master/documentation/assets/img/quadratic_equation_khoj_web.gif?raw=true)

Go to https://app.khoj.dev to see Khoj live.

## Full feature list
You can see the full feature list [here](https://docs.khoj.dev/category/features).

## Self-Host

To get started with self-hosting Khoj, [read the docs](https://docs.khoj.dev/get-started/setup).

## Enterprise

Khoj is available as a cloud service, on-premises, or as a hybrid solution. To learn more about Khoj Enterprise, [visit our website](https://khoj.dev/teams).

## Frequently Asked Questions (FAQ)

Q: Can I use Khoj without self-hosting?

Yes! You can use Khoj right away at [https://app.khoj.dev](https://app.khoj.dev) — no setup required.

Q: What kinds of documents can Khoj read?

Khoj supports a wide variety: PDFs, Markdown, Notion, Word docs, org-mode files, and more.

Q: How can I make my own agent?

Check out [this blog post](https://blog.khoj.dev/posts/create-agents-on-khoj/) for a step-by-step guide to custom agents.
For more questions, head over to our [Discord](https://discord.gg/BDgyabRM6e)!


## Contributors
Cheers to our awesome contributors! 🎉

<a href="https://github.com/khoj-ai/khoj/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=khoj-ai/khoj" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

### Interested in Contributing?
Khoj is open source. It is sustained by the community and we’d love for you to join it! Whether you’re a coder, designer, writer, or enthusiast, there’s a place for you.

Why Contribute?
- Make an Impact: Help build, test and improve a tool used by thousands to boost productivity.
- Learn & Grow: Work on cutting-edge AI, LLMs, and semantic search technologies.

You can help us build new features, improve the project documentation, report issues and fix bugs. If you're a developer, please see our [Contributing Guidelines](https://docs.khoj.dev/contributing/development) and check out [good first issues](https://github.com/khoj-ai/khoj/contribute) to work on.

## Local Customization Tracking
- Local machine-specific integration details are tracked outside repo in canonical external data roots.
- External meta path: `/Volumes/Data/_ai/_tool/tools-data/<name>/meta`
- Repo contains only sanitized capability/contract docs under `docs/local-capability/`.
- Secret values are never stored in repo docs.

## Local Operator Runbook (Codex/Claude)

This section documents the local setup used to run Khoj natively with `khoj-mcp` autostart on macOS.

### Local Paths
- Repo: `/Volumes/Data/_ai/_tool/tools_stuff/khoj`
- Persistent data root: `/Volumes/Data/_ai/_tool/tools-data/khoj`
- Runtime artifacts: `/Volumes/Data/_ai/_tool/tools-runtime/khoj`
- Native venv used by autostart: `/Volumes/Data/_ai/_tool/tools-working-cache/khoj/venv`

### Required Local Env File
Create/update: `/Volumes/Data/_ai/_tool/tools-data/khoj/config/.env`

Minimum keys:
- `KHOJ_BASE_URL=http://127.0.0.1:42110`
- `KHOJ_ADMIN_EMAIL=<admin-email>`
- `KHOJ_ADMIN_PASSWORD=<admin-password>`
- `KHOJ_NATIVE_REPO_DIR=/Volumes/Data/_ai/_tool/tools_stuff/khoj`
- `KHOJ_NATIVE_PYTHON_BIN=/Volumes/Data/_ai/_tool/tools-working-cache/khoj/venv/bin/python`
- `KHOJ_NATIVE_WORK_DIR=/Volumes/Data/_ai/_tool/tools-runtime/khoj/workdir`
- `KHOJ_NATIVE_ARTIFACTS_DIR=/Volumes/Data/_ai/_tool/tools-runtime/khoj`
- `KHOJ_NATIVE_PGSERVER_DATA_DIR=/Volumes/Data/_ai/_tool/tools-data/khoj/pgserver_data`
- `KHOJ_NATIVE_USE_EMBEDDED_DB=true`

### Native Venv Prerequisites
Install dependencies in the native venv used by autostart:

```bash
/Volumes/Data/_ai/_tool/tools-working-cache/khoj/venv/bin/python -m pip install "mcp>=1.23.0" "pgserver==0.1.4" "uvicorn==0.41.0"
```

### CSRF/Admin Login Notes
- Login failures with `Forbidden (403)` and `CSRF verification failed` were caused by local cookie domain/secure mismatches during HTTP localhost usage.
- Local cookie behavior is now hardened for local development in `src/khoj/app/settings.py`:
  - local domain defaults now disable HTTPS cookie mode for `localhost`/`127.0.0.1`
  - host-only cookie behavior is used when `KHOJ_DOMAIN` is unset
- Admin URL: `http://127.0.0.1:42110/server/admin/login/` (also works with `localhost`)

### Ready/Healthy Criteria
- `GET /api/health` returns HTTP `200`
- Admin login page opens without CSRF 403
- Search and ingest operations succeed through `khoj-mcp`

See detailed timeline and change log in `REVISION_HISTORY.md`.

### Known Local Incident: Internal Server Error on `/chat`, `/home`, `/search` (2026-03-13)
- Symptom:
  - `http://127.0.0.1:42110/chat` returned internal server error
  - `http://127.0.0.1:42110/home` returned internal server error
  - `http://127.0.0.1:42110/search` returned internal server error
- Root cause:
  - missing built web assets under:
    - `src/khoj/interface/built`
    - `src/khoj/interface/compiled`
    - `src/khoj/interface/home`
- Recovery steps:
  - rebuild web UI in `src/interface/web`
  - sync generated `out/` artifacts into `src/khoj/interface/built/`
  - create `src/khoj/interface/home/index.html` from built `index.html`
  - restart Khoj service on `127.0.0.1:42110`

### UI Asset Recovery Commands
```bash
cd /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/interface/web
npm install
npm run build

mkdir -p /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/khoj/interface/built
cp -R /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/interface/web/out/. \
  /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/khoj/interface/built/

mkdir -p /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/khoj/interface/home
cp /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/interface/web/out/index.html \
  /Volumes/Data/_ai/_tool/tools_stuff/khoj/src/khoj/interface/home/index.html
```

### Route/Template Verification
- `GET /api/health` returns `200`
- `index.html`, `chat/index.html`, `search/index.html`, `home/index.html` resolve from local templates
- `/server/` returning `404 Not Found` is expected in this deployment shape; use app routes such as `/chat`, `/home`, `/search`, and `/server/admin/login/`

## Local Enhancements Capture (2026-03-13)
- Captured current local changes, configuration updates, and operational enhancements for GitHub publication.
- Includes synchronization with sub-repo link updates where applicable.
- Cross-reference local docs and capability notes added in this repository.
