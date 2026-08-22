# FlyingNote (飞笺)

[English](README.md) | [中文](README.zh-CN.md)

Cross-platform **local-first notes** for Windows, macOS, and Linux. Write offline, sync to the cloud when you are online.  
Personal and educational use — see [LICENSE](LICENSE).

| Download | Docs |
|---|---|
| [Gitee Releases](https://gitee.com/flyingtang/flyingnote/releases) (recommended in mainland China) | This README |
| [GitHub Releases](https://github.com/flyingtang/flyingnote/releases) | [中文说明](README.zh-CN.md) |
| [Website](https://flyingtang.com/flyingnote.html) | [User manual](https://flyingtang.com/flyingnote-manual.html) |

Sync cloud: **https://note.flyingtang.cn** (built into the packaged app).

---

## Feature list

### Notes
- Notebooks, notes, tags, starred, recent, trash
- Rich text (TipTap) and Markdown live preview
- Full-text search in the current note and across notes
- Local SQLite — the machine is the source of truth while you type

### Sync
- Offline-first: keep writing with no network
- Login to https://note.flyingtang.cn (email + password, TOTP 2FA)
- Push dirty rows / pull since last sync; attachments upload separately
- Packaged builds always use the official cloud; no server URL to configure

### Tools
- Screenshot (region), color picker, ruler, pin image
- Global shortcuts (work even when the app is in the background)
- Themes and editor font size

### Account & privacy
- Optional cloud account; local-only mode if you never sign in
- Usage telemetry is anonymous (install id / OS version / timezone). **Never** note bodies, titles, or file contents

### Not included (by design)
- In-app custom sync server (official cloud only)
- Built-in auto-update plugin (download a new installer from Gitee/GitHub)
- Evernote-style web clipper / shared team workspaces as a first-class product

---

## Install

### Windows
1. Download `FlyingNote_*_x64-setup.exe` from [Gitee](https://gitee.com/flyingtang/flyingnote/releases) or [GitHub](https://github.com/flyingtang/flyingnote/releases).
2. Run the installer (Windows 10 1809+ / 11; needs [WebView2](https://go.microsoft.com/fwlink/p/?LinkId=2124703) — Edge usually already has it).
3. Start **FlyingNote** / **飞笺** from the Start menu.

### macOS
1. Download the `.dmg`.
2. Drag FlyingNote to Applications (macOS 10.15+).

### Linux
1. Prefer **AppImage**, or install `.deb` on Ubuntu 22.04+ / Debian 12+ (WebKitGTK).

---

## Quick start

1. Create a notebook, then **Ctrl+N** for a note (or **Ctrl+Shift+N** for Markdown).
2. Type. Notes save locally as you go.
3. Sign in (logo → account) to sync with https://note.flyingtang.cn.
4. **Ctrl+,** opens Settings (theme, font, shortcuts). Use **Sync now** when you want an immediate push/pull.

Data directory:
- Windows: `%APPDATA%\com.cloudnote.desktop\`
- macOS: `~/Library/Application Support/com.cloudnote.desktop/`
- Linux: `~/.local/share/com.cloudnote.desktop/`

---

## Support & mirrors

| Channel | URL |
|---|---|
| Gitee (CN) | https://gitee.com/flyingtang/flyingnote |
| GitHub | https://github.com/flyingtang/flyingnote |
| Cloud | https://note.flyingtang.cn |

**Maintainers:** how to sync `open/` and one-command release → [PUBLISH.md](PUBLISH.md).

---

## License

Non-commercial — see [LICENSE](LICENSE). Commercial use requires a separate license.
