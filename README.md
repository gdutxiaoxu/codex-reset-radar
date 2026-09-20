# Codex Reset Radar

> 跟踪 Codex Reset 公开信号、历史记录、Reset 状态与预测，并为开发者提供开放数据。

**Codex Reset Radar** 是一个独立的 Codex Reset 跟踪项目，面向关注 **Codex Reset、Codex Reset Time、Codex Usage Limit、Codex Quota、Codex Reset History** 的用户与开发者。

项目会持续整理已经确认发生的 Reset、公开 Reset Signal、历史记录与 Forecast，并逐步提供机器可读的开放数据。

🌐 **实时网站**：https://codex-reset.aiplanwatch.com/

📱 **微信小程序**：微信搜索 **徐公 AI 雷达**

> Codex Reset Radar 是独立社区项目，与 OpenAI 没有官方隶属或合作关系。Forecast 不是 OpenAI 官方公布的 Reset 时间。

---

## 当前 Codex Reset 状态

<!-- RESET_STATUS_START -->

> 当前区域后续将由数据同步脚本自动更新。

| 项目 | 状态 |
| --- | --- |
| Last Verified Reset | 待自动同步 |
| Reset Type | 待自动同步 |
| Current Status | Monitoring |
| Latest Public Signal | 待自动同步 |
| 24h Forecast | 待自动同步 |
| Last Updated | 待自动同步 |

<!-- RESET_STATUS_END -->

👉 查看完整 Reset Timeline、历史记录、公开信号与 Forecast：

https://codex-reset.aiplanwatch.com/

---

## 这个项目解决什么问题？

围绕 Codex 使用额度，用户经常会搜索：

- `codex reset`
- `codex reset time`
- `when does codex reset`
- `codex usage limit`
- `codex quota reset`
- `codex reset history`
- `codex next reset`

但这些问题背后其实包含不同类型的信息：

```text
Verified Reset
Public Signal
Historical Pattern
Forecast
Usage Limit / Rule Change
```

Codex Reset Radar 的核心原则是：

> **尽可能把“已经发生的事实”、“公开信号”和“统计预测”分开。**

因此：

> **Forecast ≠ Official Reset Time**

> **Public Signal ≠ Verified Reset**

如果你想进一步了解 Reset、Global Reset、Banked Reset 以及 Reset Time：

👉 [什么是 Codex Reset？](./docs/what-is-codex-reset.md)

---

## 主要能力

### Reset Status

查看最近一次已经确认的 Codex Reset，以及当前监控状态。

### Reset History

记录 Global Reset、Banked Reset 等不同类型的历史事件。

👉 [Codex Reset History](./docs/codex-reset-history.md)

### Reset Forecast

根据历史 Reset 时间、间隔与公开 Signal，展示未来不同时间窗口的参考 Forecast。

👉 [Codex Reset Forecast](./docs/reset-forecast.md)

### Usage Limit Reference

整理 Codex Usage Limit、Weekly Limit、Quota、Reset Window 等规则与历史变化。

👉 [Codex Usage Limits](./docs/codex-usage-limits.md)

### Open Data

项目计划持续提供机器可读的数据，方便开发者构建：

- Reset Tracker
- Notification Bot
- Chrome Extension
- VS Code / Cursor Extension
- CLI
- GitHub Badge
- Dashboard
- MCP / AI Agent

---

## Open Data

计划提供：

```text
data/
├── latest.json
├── resets.json
├── signals.json
└── forecast.json
```

### latest.json

用于读取当前最新状态，适合 Dashboard、Bot、Extension、CLI 和 Widget。

### resets.json

用于读取 Codex Reset History、构建 Timeline、统计 Reset Interval。

### signals.json

用于保存公开 Reset Signal，并与 Verified Reset 分开。

### forecast.json

用于提供未来 24h / 48h / 72h 等时间窗口的参考 Forecast。

> Open Data 仍在建设中；未实际创建的数据文件不会在 README 中宣称已经可用。

---

## Documentation

| 文档 | 主要内容 |
| --- | --- |
| [什么是 Codex Reset？](./docs/what-is-codex-reset.md) | Reset、Reset Time、Global Reset、Banked Reset、Verified / Signal / Forecast |
| [Codex Reset History](./docs/codex-reset-history.md) | 历史 Reset、事件字段、Timeline 与历史修正 |
| [Codex Usage Limits](./docs/codex-usage-limits.md) | Usage Limit、Weekly Limit、Quota、Reset Window |
| [Codex Reset Forecast](./docs/reset-forecast.md) | 下一次 Reset Forecast、24h / 48h / 72h 与限制 |
| [Methodology](./docs/methodology.md) | 事件分类、验证、去重、修正与数据同步方法 |
| [Data Sources](./docs/data-sources.md) | 官方来源、公开 Signal、社区来源与引用策略 |

后续 Open Data 稳定后，会再增加：

```text
docs/api.md
```

用于说明 JSON Schema、调用方式与 JavaScript / Python 示例。

---

## 数据与可信度

本项目会尽量把每条信息归入清晰的状态：

```text
verified
public_signal
forecast
historical
unconfirmed
```

我们不会因为一条公开讨论提到 “reset”，就直接把它写成 Verified Reset。

也不会把 Forecast 表述成 OpenAI 官方承诺的 Reset 时间。

详细分类与验证规则：

👉 [Methodology](./docs/methodology.md)

数据来源与引用原则：

👉 [Data Sources](./docs/data-sources.md)

---

## 数据更新机制

计划的数据链路：

```text
Public Sources
      ↓
AIPlanWatch Collector
      ↓
Parse / Classify / Verify
      ↓
Database
      ↓
GitHub Exporter
      ↓
codex-reset-radar
```

数据库作为主要数据源，GitHub 作为公开数据镜像。

只有真实业务数据变化时才生成新的 Commit，例如：

- New Global Reset
- New Banked Reset
- Verified Status Changed
- Important Public Signal
- Historical Data Correction
- Meaningful Forecast Change

不会因为 `last_checked_at`、Collector heartbeat 等字段不断制造无意义 Commit。

---

## Live Codex Reset Radar

如果你只是想快速查看：

- 最近一次 Codex Reset
- Reset Timeline
- Reset History
- 最新 Public Signal
- 下一次 Reset Forecast
- 相关来源与方法说明

推荐直接使用网页版：

### 🌐 Codex Reset Radar

https://codex-reset.aiplanwatch.com/

---

## 微信小程序：徐公 AI 雷达

国内微信用户可以直接搜索：

### 📱 徐公 AI 雷达

小程序用于移动端查看与 Codex Reset 相关的信息，包括：

- Reset 状态
- Reset 历史
- Reset 预测
- Reset 公开信号
- Reset 提醒
- 相关使用指南

如果你正在手机上浏览 GitHub，可以直接打开微信搜索：

**徐公 AI 雷达**

后续仓库会补充小程序二维码资源。

---

## Website / GitHub / Mini Program

三个入口承担不同角色：

| 入口 | 适合 |
| --- | --- |
| [Codex Reset Radar Website](https://codex-reset.aiplanwatch.com/) | 普通用户、Google Search 用户、Timeline / Forecast |
| GitHub | 开发者、Open Data、历史数据、Bot / Extension 开发者 |
| 徐公 AI 雷达 | 国内微信用户、移动端查看、提醒与分享 |

三端会尽量使用一致的数据逻辑与分类标准。

---

## Roadmap

- [x] Codex Reset History
- [x] Reset 状态展示
- [x] Reset Forecast
- [x] Public Reset Signals
- [x] Web Dashboard
- [x] 微信小程序入口
- [x] 文档结构拆分
- [ ] Open JSON Data
- [ ] JSON Schema
- [ ] GitHub 自动数据同步
- [ ] README 自动状态更新
- [ ] Reset Badge
- [ ] ICS Calendar Feed
- [ ] CLI
- [ ] Chrome Extension
- [ ] VS Code / Cursor Extension
- [ ] Telegram / Discord Notification
- [ ] Webhook
- [ ] MCP Tool
- [ ] Usage Limit History
- [ ] Rule Change Log

Roadmap 会根据真实用户需求和数据使用情况调整。

---

## Repository Structure

```text
codex-reset-radar/
│
├── README.md
├── README.zh-CN.md
│
├── docs/
│   ├── what-is-codex-reset.md
│   ├── codex-reset-history.md
│   ├── codex-usage-limits.md
│   ├── reset-forecast.md
│   ├── methodology.md
│   └── data-sources.md
│
├── data/
├── schema/
├── examples/
└── assets/
```

---

## Contributing

欢迎提交：

- Reset 历史修正
- 数据来源补充
- 新 Reset Signal
- Bug Report
- Usage Limit 规则变化
- 文档改进

如果提交 Reset 相关数据，请尽量提供公开可验证的来源。

单独的“我的账号好像 Reset 了”可以作为线索，但不会直接成为 Verified Reset。

---

## Star

如果这个项目对你有帮助，可以给仓库一个 ⭐ Star。

这能帮助更多正在寻找：

`codex reset` · `codex reset time` · `when does codex reset` · `codex usage limit` · `codex reset history`

的开发者发现这个项目。

---

## Disclaimer

Codex Reset Radar 是独立社区项目。

本项目：

- 不是 OpenAI 官方产品
- 不代表 OpenAI 发布 Reset 时间
- 不保证 Forecast 一定发生
- 不保证 Public Signal 最终一定对应 Reset
- 不应将预测数据理解为官方承诺

产品规则、Usage Limit、Quota 和 Reset 机制可能随时变化，涉及具体产品规则时，应优先以相关产品官方最新信息为准。

OpenAI、Codex 及其他相关名称和商标归各自权利人所有。

---

## Links

🌐 **Live Codex Reset Radar**  
https://codex-reset.aiplanwatch.com/

📱 **WeChat Mini Program**  
微信搜索：**徐公 AI 雷达**

📚 **Documentation**  
[查看全部文档](./docs/what-is-codex-reset.md)
