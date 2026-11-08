<p align="center"><img src="icon.svg" width="96" height="71" alt="dsh-whale-icon"></p>

# dsh-whale-icon

[English](#english) | [中文](#中文)

> The DeepSeek blue whale on the DSH composer send/stop button, swimming while the agent works.
> 把 DSH 输入框的发送 / 停止生成按钮换成 DeepSeek 品牌蓝色鲸鱼，Agent 运行时游动起来。

---

## English

### What it does

`dsh-whale-icon` restyles the resident composer's **primary send / stop button** in the DSH Web UI:

- The default arrow is replaced by the official DeepSeek whale mark (`FISH_LOGO_PATH` from the harness primitives), drawn in the theme's DeepSeek blue.
- The button keeps a raised, glossy 3D look: a vertical blue gradient, a top highlight, layered drop shadows, and inset bevels.
- Hover: the whale bobs gently and the button lifts. Press: it compresses with an inner shadow.
- While the agent is running (or a message is being sent), the whale swims with a soft sonar halo and the button glows. It returns to rest when the turn finishes.
- Dark theme gets its own gradient, shadows, and a lighter blue whale.
- `prefers-reduced-motion` disables the swimming.

Only the send/stop button is touched. The model selector, permission control, plan control, and other composer buttons keep their default styling.

### Install

Install from the public Git repository:

```sh
dsh plugin --profile web add github:feiniao1933/dsh-whale-icon
```

Or pin a commit (recommended for reproducible installs):

```sh
dsh plugin --profile web add git+https://github.com/feiniao1933/dsh-whale-icon.git#<commit>
```

Replace `web` with your profile name. The plugin ships no install script and no dependencies beyond the host Web client.

### Compatibility

- Built and tested with DSH `0.2.2-rc.1` on macOS.
- Requires a Web client (`dsh web` / the desktop Web surface) with the conversation UI installed.

### How it works

The shipped composer renders its send/stop button inside the `conversation.composer.bar` slot, with no dedicated icon slot. The Client half therefore:

1. targets the primary button through the stable `data-slot` anchor and its `_primary` class, and swaps the glyph for the official whale path;
2. registers a tiny invisible occupant in `conversation.composer.dock` that reads `useSessionStatus` and mirrors the current session's running state onto the document;
3. lets CSS drive the static, hover, pressed, sending, and running states from that attribute.

Everything is Client-side and local: no HTTP route, no network request, no stored data, and no change to model selection.

### License

MIT. The whale path is taken from the DeepSeek Harness brand primitives; the DeepSeek name and whale mark belong to DeepSeek.

---

## 中文

### 这个插件做什么

`dsh-whale-icon` 只改 DSH Web 输入框里的**发送 / 停止生成主按钮**：

- 默认的箭头换成 DeepSeek 官方鲸鱼标识（取自 Harness primitives 的 `FISH_LOGO_PATH`），使用主题的 DeepSeek 蓝。
- 按钮有轻微的立体质感：纵向蓝色渐变、顶部高光、多层投影、内高光与内阴影。
- 悬停时鲸鱼轻轻摆动、按钮上浮；按下时回弹并出现内凹阴影。
- Agent 运行中（或消息发送中）鲸鱼游动，带柔和的声呐光晕和按钮外发光；本轮结束自动恢复静止。
- 深色模式使用单独的渐变、阴影和更亮的蓝色鲸鱼。
- 尊重 `prefers-reduced-motion`，系统要求减弱动态时停止游动。

只影响发送 / 停止按钮；模型选择器、权限、Plan 和其他输入框控件保持默认样式。

### 安装

从公开仓库安装：

```sh
dsh plugin --profile web add github:feiniao1933/dsh-whale-icon
```

或固定提交（推荐，安装可复现）：

```sh
dsh plugin --profile web add git+https://github.com/feiniao1933/dsh-whale-icon.git#<commit>
```

把 `web` 换成你的 profile 名称。插件没有安装脚本，也没有宿主端额外依赖。

### 兼容性

- 在 DSH `0.2.2-rc.1`、macOS 上开发与验证。
- 需要 Web 客户端（`dsh web` 或桌面端 Web 界面）并已安装会话 UI。

### 实现方式

发送按钮由 `ui-conversation` 在 `conversation.composer.bar` 插槽内渲染，没有单独的图标插槽。因此 Client 端：

1. 通过稳定的 `data-slot` 锚点和 `_primary` 类定位主按钮，把图形换成官方鲸鱼路径；
2. 在 `conversation.composer.dock` 注册一个不可见的小组件，用 `useSessionStatus` 读取当前会话的运行状态并同步到文档；
3. 由 CSS 根据该状态驱动静止、悬停、按下、发送和运行几种外观。

全部在浏览器端本地完成：没有 HTTP 路由、没有网络请求、不保存数据，也不改变模型选择。

### 许可证

MIT。鲸鱼路径来自 DeepSeek Harness 品牌 primitives；DeepSeek 名称与鲸鱼标识归 DeepSeek 所有。
