# dshopen.org 收录申请

打开 https://github.com/polang233/dsh-plugin-index/issues/new?template=plugin-add.yml

## 标题

```text
[plugin-add] dsh-whale-icon
```

## 插件地址 / Plugin link

Git 来源（npm 暂未发布）：

```text
仓库：https://github.com/feiniao1933/dsh-whale-icon
版本：1.2.0
提交：<COMMIT_SHA>
路径：仓库根目录
```

## 简短说明 / Summary

中文：

```text
把 DSH 输入框的发送 / 停止生成主按钮换成 DeepSeek 官方鲸鱼标识，并给按钮加上渐变、高光和投影的立体质感。空闲时鲸鱼静止，悬停轻摆、按下回弹；Agent 运行或消息发送中鲸鱼游动并带声呐光晕，本轮结束恢复静止。只影响发送 / 停止按钮，模型选择器等其他控件保持默认；支持深色模式和 prefers-reduced-motion。数据全部在浏览器端本地处理，没有网络请求或存储。
```

English:

```text
Replaces the DSH composer's primary send/stop button with the official DeepSeek whale mark, raised with a glossy gradient, top highlight and layered shadows. The whale is static at rest, bobs on hover, compresses on press, and swims with a soft sonar halo while the agent runs or a message is being sent, then settles again when the turn ends. Only the send/stop button changes; the model selector and other composer controls keep their default styling. Dark theme and prefers-reduced-motion are supported. Everything runs locally in the browser with no network requests or stored data.
```

## 截图 / Screenshots

暂不提供（本机无法对已登录页面截图）。提交前如有截图，附 1–2 张发送按钮静止与运行中的画面，并遮住账号信息。

## 补充信息 / Additional details

```text
Logo: 包内 icon.svg（也通过 ./icon 导出）
测试版本：DSH 0.2.2-rc.1，macOS
许可证：MIT
安装（固定提交）：dsh plugin --profile web add git+https://github.com/feiniao1933/dsh-whale-icon.git#<COMMIT_SHA>
```
