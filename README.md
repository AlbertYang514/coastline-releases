# Coastline Releases

Current release: **Coastline 2.0.0**

Coastline is a local-first writing studio for long-form narrative projects.

## Download

### macOS

- File: `Coastline-2.0.0-macOS.dmg`
- Path: `releases/2.0.0/Coastline-2.0.0-macOS.dmg`
- Size: `198968697` bytes
- SHA256: `1b39fafe63f1aba4092d90d163030870da6c2369952e01e8d6ab0bf5b859e336`

### Windows

- File: `CoastlineSetup-2.0.0-win-x64.exe`
- Path: `releases/2.0.0/CoastlineSetup-2.0.0-win-x64.exe`
- Size: `246130830` bytes
- SHA256: `4d4a3dc5abcf98486c3cbae06afa837b743540c030508ec10eb3ef1eef11787d`

## What is new in 2.0.0

- Streaming chapter analysis and batch analysis flow.
- Bundled local ONNX reranker for context ranking.
- Local SQLite index/cache layer for faster project context access.
- Project archive management, trash restore, and permanent delete.
- Guided update check.
- Packaged LICENSE, EULA, PRIVACY, CHANGELOG, and third-party notices.

## Privacy and local-first design

Coastline stores projects locally. The bundled local reranker runs on device and does not send project text to Coastline servers. If you configure a third-party model provider, selected context may be sent to that provider when you explicitly run analysis.

See `PRIVACY.md`, `EULA.txt`, `LICENSE.txt`, `THIRD-PARTY-NOTICES.txt`, and `THIRD-PARTY-LICENSES.json` for details.

## Verification

Expected SHA256 hashes are listed in the `.sha256` files next to each release asset.

Run:

shasum -a 256 Coastline-2.0.0-macOS.dmg
shasum -a 256 CoastlineSetup-2.0.0-win-x64.exe

---

Protect the coastline.
