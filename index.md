---
title: Tabokay Privacy Policy
---

# Tabokay Privacy Policy

**Last updated: May 24, 2026**

Tabokay (“the Extension”) is a Chrome extension that customizes the new tab page, helps manage tabs, and provides local tools. This policy explains how the Extension handles information.

**简体中文：** [Tabokay 隐私政策](#tabokay-隐私政策) · Standalone: [PRIVACY_cn.md](./PRIVACY_cn.md) · [PRIVACY.md](./PRIVACY.md)

---

## What We Collect

The Extension **does not require an account** and **does not include third-party analytics or advertising SDKs**. Except for feedback you voluntarily submit via GitHub Issues, we **do not upload your data to Tabokay-operated servers**.

Data is stored locally in your browser using `chrome.storage.local` (legacy data may have existed in `localStorage` and is migrated on first run), including:

| Data | Purpose |
|------|---------|
| New tab background, tint, and wallpaper choices | Personalization |
| Desktop widget layout and visibility | Desktop editing and Settings |
| Quick links (Quicks) | Bottom quick panel |
| Todo, countdown, and pomodoro state | Corresponding widgets |
| Weather widget city or coordinates cache | Weather display |
| Schedule widget ICS subscription URL | Calendar feed you configure |
| UI language preference | Localization |
| Command Cheatsheet selected folder name | Remember authorized directory |
| **Stash list** | URLs, titles, icons, and timestamps for tabs you explicitly stash |

When you use the following features, the Extension **reads tab information locally** in your browser (not sent to our servers):

- **Left Actions panel**: list windows and tabs; switch or close tabs
- **Stash** (popup / side panel): read the active tab and save it to the local stash list
- **`sessions` permission**: supplementary access to window/tab information in some environments

If you enable the **Weather widget**, the browser may request location via `navigator.geolocation` (a browser API, not an extra extension permission). Location is used only to query weather services and may be cached locally.

If you use **Command Cheatsheet** and authorize a local folder, the Extension reads `*.cmds.json` and related files only after your explicit action; content is used for display and copy only.

---

## What We Do Not Collect

- No account sign-in required
- We do not upload your full browsing history to Tabokay servers
- We do not sell your personal data
- No embedded analytics (e.g. Google Analytics) in the Extension

---

## Network Requests and Third Parties

Some features request **public third-party endpoints**. Requests are made directly by your browser or the Extension background worker and are governed by each provider’s terms and privacy policy:

| Service / domain | Purpose |
|------------------|---------|
| `api.open-meteo.com` | Weather widget |
| `weibo.com` | Weibo hot topics widget (if enabled) |
| `www.iesdouyin.com` / `www.douyin.com` | Douyin hot list widget (if enabled) |
| `icons.duckduckgo.com` / `www.google.com` | Tab favicon detection |
| **ICS URL you paste** | Schedule widget (domain varies by user) |

The Extension declares `<all_urls>` host permission in its manifest primarily to support user-provided ICS subscription URLs (domains cannot be enumerated in advance). Aside from the services above and your configured ICS feed, the Extension does not bulk-send data to arbitrary websites.

Built-in wallpaper assets are sourced from [Unsplash](https://unsplash.com) under their license; see `res/wallpapers/descriptions.json` in the extension repository.

---

## Chrome Permissions

| Permission | Purpose |
|------------|---------|
| `storage` | Save settings and stash list locally |
| `tabs` | List, switch, close, and stash tabs |
| `sessions` | Supplementary window/tab access in some cases |
| `sidePanel` | Open the stash list side panel |
| `host_permissions` (`<all_urls>`) | Widget data fetches and user-configured ICS URLs |
| New tab override | Provide the Tabokay new tab page |

The manifest sets `incognito: spanning`, so the Extension can run in incognito. Actions such as stashing or viewing tabs in incognito apply only within your browser session and local storage rules.

---

## Retention and Deletion

- Data remains in your browser until you clear extension data, clear site data, or uninstall the Extension
- Uninstalling the Extension typically removes locally stored extension data
- You can delete individual stash entries in the stash list

---

## Children’s Privacy

The Extension is not directed at children under 13, and we do not knowingly collect personal information from children.

---

## Changes to This Policy

We may update this policy. The revised version will be posted at the same URL with an updated “Last updated” date. Material changes may be noted in the Extension or GitHub repository.

---

## Contact Us

- **Feedback and feature requests**: [GitHub Issues](https://github.com/fallending/tabokay/issues)
- **Privacy inquiries** (optional): YOUR_EMAIL@example.com

---

# Tabokay 隐私政策

**最后更新：2026 年 5 月 24 日**

Tabokay（「本扩展」）是一款 Chrome 浏览器扩展，用于自定义新标签页、管理标签与本地工具。本政策说明本扩展如何处理信息。

**English:** [Tabokay Privacy Policy](#tabokay-privacy-policy) · 独立文件：[PRIVACY_cn.md](./PRIVACY_cn.md) · [PRIVACY.md](./PRIVACY.md)

---

## 我们收集什么

本扩展**不要求注册账号**，也**未集成第三方统计或广告 SDK**。除您主动通过 GitHub Issues 提交的反馈外，我们**不会将您的数据上传到 Tabokay 自有服务器**。

本扩展主要将数据保存在您浏览器本地的 `chrome.storage.local`（部分历史数据可能曾存在于 `localStorage`，扩展会在首次运行时迁移），包括：

| 数据类型 | 用途 |
|----------|------|
| 新标签页背景、混色与壁纸选择 | 个性化外观 |
| 桌面 Widget 布局与显示开关 | 桌面编辑与 Settings |
| 快捷入口（Quicks） | 底部快捷面板 |
| 待办、倒计时、番茄钟状态 | 对应 Widget |
| 天气 Widget 的城市或坐标缓存 | 展示天气 |
| 日程 Widget 的 ICS 订阅链接 | 拉取您配置的日历 |
| 界面语言偏好 | 多语言显示 |
| Command Cheatsheet 所选本地目录名称 | 记住您授权的文件夹 |
| **贮藏（Stash）列表** | 保存您主动贮藏的标签页 URL、标题、图标与时间 |

当您使用以下功能时，本扩展会**在本地读取**浏览器中的标签页信息（不会上传至我们的服务器）：

- **左侧 Actions 面板**：列出窗口与标签页，支持切换与关闭
- **贮藏功能**（Popup / 侧边栏）：读取当前标签页信息并保存到本地贮藏列表
- **sessions 权限**：在部分环境下作为获取窗口/标签信息的补充手段

若您启用 **天气 Widget**，浏览器会通过 `navigator.geolocation` 请求定位（属于浏览器定位 API，非扩展额外权限）；定位结果仅用于向天气服务查询，并可在本地缓存。

若您使用 **Command Cheatsheet** 并授权本地文件夹，扩展会在您明确操作后读取该目录中的 `*.cmds.json` 等文件，内容仅用于展示与复制命令。

---

## 我们不收集什么

- 我们不要求账号登录
- 我们不上传您的完整浏览历史至 Tabokay 服务器
- 我们不出售您的个人数据
- 我们不在扩展内嵌入 Google Analytics 等分析工具

---

## 网络请求与第三方服务

部分功能会向**第三方公开接口**发起网络请求，以便展示内容。请求由您的浏览器或扩展后台直接发出，受各第三方服务条款与隐私政策约束：

| 服务 / 域名 | 用途 |
|-------------|------|
| `api.open-meteo.com` | 天气 Widget |
| `weibo.com` | 微博热搜 Widget（若启用） |
| `www.iesdouyin.com` / `www.douyin.com` | 抖音热榜 Widget（若启用） |
| `icons.duckduckgo.com` / `www.google.com` | 标签页图标探测 |
| **您自行粘贴的 ICS 订阅 URL** | 日程 Widget（域名因用户而异） |

本扩展在 manifest 中使用 `<all_urls>` 主机权限，主要目的是支持用户自填的 ICS 订阅链接（无法预先枚举域名）。除上述已知服务与您配置的 ICS 外，扩展不会主动向任意网站批量发送数据。

内置壁纸资源来自 [Unsplash](https://unsplash.com)，遵循其许可条款；图源记录见扩展仓库内 `res/wallpapers/descriptions.json`。

---

## Chrome 权限说明

| 权限 | 目的 |
|------|------|
| `storage` | 本地保存设置与贮藏列表 |
| `tabs` | 标签页列表、切换、关闭、贮藏 |
| `sessions` | 在部分环境下辅助获取窗口/标签信息 |
| `sidePanel` | 打开贮藏列表侧边栏 |
| `host_permissions`（`<all_urls>`） | Widget 数据请求与用户配置的 ICS 链接 |
| 新标签页覆盖 | 提供 Tabokay 新标签页 |

本扩展在 manifest 中声明 `incognito: spanning`，在无痕模式下也可运行；您在无痕模式下的操作（如贮藏、查看标签）仅作用于当前浏览器会话与本地存储策略所允许的范围。

---

## 数据保留与删除

- 数据保留在您的浏览器中，直到您清除扩展数据、清除站点数据或卸载扩展
- 卸载扩展后，Chrome 通常会一并删除扩展本地存储的数据
- 您可在贮藏列表中删除单条贮藏记录

---

## 儿童隐私

本扩展不面向 13 岁以下儿童，也不会故意收集儿童个人信息。

---

## 政策变更

我们可能更新本政策。更新版本将发布在同一 URL，并修改文首「最后更新」日期。重大变更时，我们可能在扩展或 GitHub 仓库中另行说明。

---

## 联系我们

- **问题反馈与功能建议**：[GitHub Issues](https://github.com/fallending/tabokay/issues)
- **隐私相关邮件**（可选）：YOUR_EMAIL@example.com
