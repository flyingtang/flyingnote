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

FlyingNote desktop auto-update reads `latest.json` (Gitee, then GitHub; official API hosts last). Upload installers as **Release assets**.

Helper (from `cloudnote/desktop`):

```bash
npm run release -- --version 0.1.2
```

See `../PUBLISH.md`.
