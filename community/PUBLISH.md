# 发布状态 / Publishing status

## 发布渠道

- **Open Plugin Market（dshopen.org）**：✅ 已收录（2026-11-09），插件页 https://dshopen.org/zh/plugins/dsh-whale-icon/ ，版本 1.2.0，固定提交 `198230d57b0424dd8dfadcbee6adc1325d050e9f`，标签 `verified` / `updated-recent`；申请 Issue：https://github.com/polang233/dsh-plugin-index/issues/326
- **awesome-dsh-plugin（dsh-market 目录）**：单文件 PR：https://github.com/awesome-dsh-plugin/awesome-dsh-plugin/pull/13198

## 已完成

- 公开源码仓库：https://github.com/feiniao1933/dsh-whale-icon（`main` 已推送）
- 发布用包：`dsh-whale-icon@1.2.0`，MIT，`repository` / `engines.dsh` / `dsh.bundle.patch` 齐全
- `npm pack` 校验通过
- GitHub 安装验证通过：临时 profile 中 `dsh plugin --profile whale-test add github:feiniao1933/dsh-whale-icon` 安装 `dsh-whale-icon 1.2.0`，`--dump-config` 中出现 `whale-send-icon` 行
- 当前 profile 已从 `@deepseek-ai/dsh-session-whale-icon` 迁移到 `dsh-whale-icon`，Client 插槽已验证可用
- 真实使用截图：`screenshots/composer-send-button.png`，通过 `screenshots.json` 声明；已补充到 dshopen Issue 评论 https://github.com/polang233/dsh-plugin-index/issues/326#issuecomment-6719802212

## 待办

- [ ] awesome-dsh-plugin 合并。首次 gate 仅因仓库年龄 0.0 天失败；仓库已满 1 天，已推送空提交重新触发 gate，CI 进行中
- [ ] 可选：npm 登录后 `npm publish --access public`
- [x] 补充真实使用截图到 `screenshots.json`
