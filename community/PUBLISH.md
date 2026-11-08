# 发布状态 / Publishing status

## 发布渠道

- **Open Plugin Market（dshopen.org）**：收录申请 Issue：https://github.com/polang233/dsh-plugin-index/issues/326
- **awesome-dsh-plugin（dsh-market 目录）**：单文件 PR：https://github.com/awesome-dsh-plugin/awesome-dsh-plugin/pull/13198

## 已完成

- 公开源码仓库：https://github.com/feiniao1933/dsh-whale-icon（`main` 已推送）
- 发布用包：`dsh-whale-icon@1.2.0`，MIT，`repository` / `engines.dsh` / `dsh.bundle.patch` 齐全
- `npm pack` 校验通过
- GitHub 安装验证通过：临时 profile 中 `dsh plugin --profile whale-test add github:feiniao1933/dsh-whale-icon` 安装 `dsh-whale-icon 1.2.0`，`--dump-config` 中出现 `whale-send-icon` 行
- 当前 profile 已从 `@deepseek-ai/dsh-session-whale-icon` 迁移到 `dsh-whale-icon`，Client 插槽已验证可用
- 真实使用截图：`screenshots/composer-send-button.png`，通过 `screenshots.json` 声明

## 待办

- [ ] awesome-dsh-plugin 的仓库年龄门槛（创建满 1 天）自动重跑通过
- [ ] 可选：npm 登录后 `npm publish --access public`
- [x] 补充真实使用截图到 `screenshots.json`
