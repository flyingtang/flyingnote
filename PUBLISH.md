# Publishing FlyingNote to public mirrors

Public user-facing repos (docs + release staging live under `open/`):

- https://github.com/flyingtang/flyingnote
- https://gitee.com/flyingtang/flyingnote

The development tree stays in the private/monorepo (`cloudnote/desktop`).  
`open/` is what end users should see as the repository root.

Official website pages live in the shared static site: `flyingterm/website/flyingnote.html` (deployed as flyingtang.com).

---

## 中文：一条命令发布

### 1. 首次配置（token **不要**提交）

```powershell
cd cloudnote/desktop
npm run release -- --init
```

编辑生成的 `publish-open.local.env`：

| 项 | 含义 |
|---|---|
| `OPEN_PUBLIC_DIR` | 公开仓本机克隆路径（相对当前目录；默认 `./flyingnote-public`，不存在会自动 clone） |
| `GITHUB_REPO_URL` / `GITEE_REPO_URL` | 公开仓库地址 |
| `GH_TOKEN` 或 `GH_TOKEN_FILE` | GitHub token（`repo` 权限，上传 Release） |
| `GITEE_TOKEN` 或 `GITEE_TOKEN_FILE` | Gitee token（上传 Release，可选） |

也可把同一份 token 放在 **mycap 仓库根** 的 `publish-open.local.env`，飞笺与 FlyingTerm 共用。

自动更新签名私钥在 `src-tauri/.updater/flyingnote.key`（勿提交）。首次生成：`npm run keys:refresh`。没有私钥时 `publish-open` 会拒绝打包。

### 2. 日常发布

```powershell
cd cloudnote/desktop
npm run release
```

可选：`npm run release -- --version 0.1.2`

| 本机系统 | 默认产物 |
|---------|---------|
| Windows | NSIS |
| macOS | universal `.app` / `.dmg` |
| Linux | deb + AppImage |

流程：打包 → 暂存 `open/releases/` → **增量**同步公开仓文档 → 上传 GitHub / Gitee Releases（小文件先传）。  
git push 超时会自动重试。安装包**不进 git**。

只要同步文档：`npm run open:publish -- --sync`  
已打好包：`npm run release -- --skip-build`

### 3. 和 FlyingTerm 一起发（先发飞笺）

安装包体积飞笺更小，远端超时更少。在 **mycap 根目录**：

```powershell
./tools/publish-public.sh --all
# 或只发飞笺
./tools/publish-public.sh --only flyingnote
```

会先跑 FlyingNote，成功后再跑 FlyingTerm。

### 4. Token

- GitHub：https://github.com/settings/tokens （classic，勾选 `repo`）
- Gitee：https://gitee.com/profile/personal_access_tokens

---

## English

```bash
cd cloudnote/desktop
npm run release -- --init   # once
# edit publish-open.local.env
npm run release             # or: npm run release -- --version 0.1.2
```

From the mycap repo root, publish **FlyingNote first** (smaller) then FlyingTerm:

```bash
./tools/publish-public.sh --all
```

Never commit `publish-open.local.env` / `secrets/` / `*.token`.
