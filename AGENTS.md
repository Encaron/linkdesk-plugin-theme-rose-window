# 玫瑰窗（theme-rose-window）——LinkDesk 插件仓

> **本文件是给在这个仓里干活的 AI 看的**（Claude Code / Codex / Cursor / …）。人看 `README.md`。
> 插件身份的唯一来源 = `plugin.json` 顶层的 `pluginId`（本仓：`theme-rose-window`）。当前版本 `1.0.0`。

## 1. 这是什么

教堂彩窗主题——亮色磨砂玻璃表面 ＋ 全窗玫瑰窗背景 ＋ 三组彩窗配色（午后圣光 / 青金石 / 晚祷紫）。

**用户在哪看到它**：外观主题：在设置 → 外观里切换。

**🔴 本仓就是这只插件的真源。** 壳仓没有它的源码，只有已发布的产物（官方目录条目 / 出厂种子）。

> 这只插件**不随软件出厂**（`seed: false`）：用户从插件市场装上它。

## 2. 铁律（破了就坏插件，或者坏壳）

1. **颜色一律走 `var(--xxx)`** —— 主题是数据插件，颜色只出现在配方 `colorways[].colors` 里。
2. **UI 文案一律走 `t()`** —— 本仓是数据插件，没有 `t()`；名字一律写**中文原文**，英文译文住 `i18n/en.json`。
3. **系统能力只走 `window.linkdesk.*`** —— 本仓不 import 壳内部。
4. **资源一律相对路径**（`assets/...` / `linkdesk://<pluginId>/...`）—— 禁止绝对路径。
5. **配方只住 `themes/`**，不摊到仓根。

## 3. 本仓的结构与关键路径

```
theme-rose-window/
├── plugin.json              # 声明（contributes.themes）
├── themes/rose-window.json  # 配方：appearance + 3 colorways
├── resources/
│   ├── cathedral-bg.jpg     # 全窗背景图（21:9，CC0 合成）
│   ├── cover.svg            # README 场景封面
│   └── icon.svg             # 插件图标
├── i18n/en.json             # 本仓字典（key = 中文原文）
└── scripts/ci-verify.mjs    # 本仓严格门禁
```

## 4. 本仓的命令

```bash
npm run build      # 产出 `<pluginId>.linkdesk-plugin`
npm run validate   # 校验 plugin.json / 主题配方 / 声明的字典文件真的在
npm run lint       # SDK 规则腿（只报告、不拦）
npm run publish    # 发版到本仓自己的 GitHub Release（上架第一步）
npm run verify     # 🔴 交付前严格腿（CI 同款）
```

## 5. 发布与版本纪律

**🔴 上架两步**：`npm run publish` 只写本仓 Release；**第二步是收录进官方目录**（`Encaron/linkdesk-marketplace`）——不收录，默认设置的用户永远看不到。

**版本号**：`plugin.json` 与 `package.json` 必须同值；每次 bump 在 `CHANGELOG.md` 配 `## v<新版本>（YYYY-MM-DD）`。

## 6. 资源来源

`resources/cathedral-bg.jpg` = 巴黎圣母院北玫瑰窗（Wikimedia Commons，**公有领域**）＋ 本仓 2560×1200 取景、日光提亮与暖光合成。公有领域不要求署名，README 仍如实记录。
