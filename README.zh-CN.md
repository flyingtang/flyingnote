# 飞笺 FlyingNote

[English](README.md) | [中文](README.zh-CN.md)

跨平台 **本地优先笔记**：Windows / macOS / Linux。断网可写，联网再同步到云端。  
个人与学习用途 — 详见 [LICENSE](LICENSE)。

| 下载 | 文档 |
|---|---|
| [Gitee Releases](https://gitee.com/flyingtang/flyingnote/releases)（国内推荐） | 本页 |
| [GitHub Releases](https://github.com/flyingtang/flyingnote/releases) | [English](README.md) |
| [官网](https://flyingtang.com/flyingnote.html) | [用户手册](https://flyingtang.com/flyingnote-manual.html) |

同步云端：**https://note.flyingtang.cn**（安装包已写死，无需配置服务器地址）。

---

## 功能清单

### 笔记
- 笔记本、笔记、标签、收藏、最近、回收站
- 富文本（TipTap）与 Markdown 实时预览
- 当前笔记内查找与全局搜索
- 本地 SQLite：打字时以本机为真相

### 同步
- 离线优先：没网也能写
- 登录 https://note.flyingtang.cn（邮箱 + 密码，TOTP 二次认证）
- 推送脏数据 / 按时间拉取；附件单独上传
- 正式安装包固定官方云，设置里没有「同步服务器」

### 工具
- 截图（框选）、取色、尺子、钉图
- 全局快捷键（应用在后台也生效）
- 主题、编辑器字号

### 账户与隐私
- 可以不登录，纯本地使用
- 用量统计仅匿名安装 ID / 系统版本 / 时区，**不含**笔记正文、标题、附件内容

### 有意不做
- 在设置里自定义同步服务器（只用官方云）
- 应用内自动升级插件（请从 Gitee / GitHub 下新安装包）
- 网页剪藏 / 团队空间作为主产品能力

---

## 安装

### Windows
1. 从 [Gitee](https://gitee.com/flyingtang/flyingnote/releases) 或 [GitHub](https://github.com/flyingtang/flyingnote/releases) 下载 `FlyingNote_*_x64-setup.exe`。
2. 运行安装程序（需 Windows 10 1809+ / 11；需要 [WebView2](https://go.microsoft.com/fwlink/p/?LinkId=2124703)，装了 Edge 一般已有）。
3. 从开始菜单启动 **飞笺** / **FlyingNote**。

### macOS
1. 下载 `.dmg`。
2. 拖到「应用程序」（需 macOS 10.15+）。

### Linux
1. 优先 **AppImage**；Ubuntu 22.04+ / Debian 12+ 也可装 `.deb`（需 WebKitGTK）。

---

## 快速上手

1. 新建笔记本，再 **Ctrl+N** 新建笔记（**Ctrl+Shift+N** 为 Markdown）。
2. 直接打字，内容会落到本机。
3. 点左上角图标打开账户，登录后与 https://note.flyingtang.cn 同步。
4. **Ctrl+,** 打开设置（主题、字号、快捷键）。需要立刻对齐云端时点 **立即同步**。

数据目录：
- Windows：`%APPDATA%\com.cloudnote.desktop\`
- macOS：`~/Library/Application Support/com.cloudnote.desktop/`
- Linux：`~/.local/share/com.cloudnote.desktop/`

---

## 支持与镜像

| 渠道 | 地址 |
|---|---|
| Gitee（国内） | https://gitee.com/flyingtang/flyingnote |
| GitHub | https://github.com/flyingtang/flyingnote |
| 云端 | https://note.flyingtang.cn |

**维护者：** 同步 `open/`、一条命令发版 → 见 [PUBLISH.md](PUBLISH.md)。

---

## 许可证

非商业用途 — 见 [LICENSE](LICENSE)。商业使用需另行授权。
