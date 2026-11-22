# 更新日志

## v1.0.1（2026-11-23）

- **贵重衬线字体**：`font.ui` 换成 `Constantia / Palatino Linotype + Noto Serif SC / 思源宋体` 衬线栈——整个 UI 走书卷气贵感，代码/等宽面仍走 Cascadia / Consolas（主题机制只有 ui / mono 两个字体键，不做逐组件字体）。
- **玻璃参数按实机可读性重调**：`blur 36` · `saturate 1.35` · `tint rgba(255,247,230,.62)` · `opacity 0.46` · `specular 0.92` / `#FFEFC0`——彩窗仍从玻璃后透上来，文字底更稳。
- **文字对比提升**：主文字 `#1F160D`、次级 `#4A3823`、弱文字 `#55422B`；内容面 `surface-reading` 提到 `.94` / `.97`——玻璃面上主文字 ≥10:1、次级 ≥6:1、弱文字 ≥4.5:1。
- **新增场景封面** `resources/cover.jpg`（主题截图 + 标题字），README 顶部与市场目录封面同源。
- **三张场景截图**已放进官方目录仓 `media/theme-rose-window/`（工作区 / 设置页 / 分屏+浮层，三种配色各一张）。
- 工程标准补强：新增 `@linkdesk/marketplace-kit` 校验腿（`npm run validate:catalog`，CI 同跑）。

## v1.0.0（2026-11-23）

- **首发**：教堂彩窗主题「玫瑰窗」——亮色磨砂玻璃表面（标题栏 / 工具栏 / 图标栏 / 侧栏 / 主区 / 面板区 / 状态栏全部玻璃化）＋ 全窗巴黎圣母院玫瑰窗背景（公有领域，2560×1200 日光提亮与暖光合成）＋ 金色受光边（`specular 0.90` / `#FFF0C4`）。
- **三组彩窗配色**：午后圣光（金箔 `#A6771B`）· 青金石（`#2F5D9E`）· 晚祷紫（`#6B3F8E`）；共用同一亮色玻璃基座与暖墨文字。
- 内容面可读性 token（`surface-reading` / `surface-reading-strong` / `surface-media-scrim` / `surface-ink`）随首发写入，玻璃再透正文也不糊。
