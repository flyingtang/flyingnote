# Release artifacts (installers)

Put build outputs here before uploading to **Gitee** / **GitHub** Releases.

```
open/releases/
  latest.json
  latest.json.example
  FlyingNote_*_x64-setup.exe
  *.dmg / *.AppImage / *.deb
```

Large binaries are **gitignored**. Only `latest.json` (and docs) should be committed so clones stay small. Upload installers as **Release assets**.

FlyingNote desktop currently **does not** ship a Tauri auto-updater. `latest.json` is still useful as a download index for the website and mirrors.

Helper (from `cloudnote/desktop`):

```bash
npm run release -- --version 0.1.2
```

See `../PUBLISH.md`.
