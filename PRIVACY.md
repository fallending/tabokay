# Tabokay Privacy Policy

> **GitHub Pages:** [index.md](./index.md) · **Chinese:** [PRIVACY_cn.md](./PRIVACY_cn.md)  
> **Public URL:** https://fallending.github.io/tabokay/

**Last updated: May 24, 2026**

Tabokay (“the Extension”) is a Chrome extension that customizes the new tab page, helps manage tabs, and provides local tools. This policy explains how the Extension handles information.

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

## Contact Us

- **Feedback and feature requests**: [GitHub Issues](https://github.com/fallending/tabokay/issues)
- **Privacy inquiries** (optional): asusual.cn@gmail.com