# Codex Reset Radar

> **Codex 今天 Reset 了吗？下一次什么时候可能 Reset？**

Codex Reset Radar 持续跟踪 **Codex Global Reset、Banked Reset、公开 Reset Signal、历史记录和下一次 Reset Forecast**，并逐步提供开放 JSON 数据，方便用户查看，也方便开发者构建自己的提醒、Bot、Extension 和 Dashboard。

🌐 **实时 Radar**：https://codex-reset.aiplanwatch.com/

📱 **微信小程序**：微信搜索 **徐公 AI 雷达**

> 独立社区项目，与 OpenAI 没有官方隶属或合作关系。Forecast 不是 OpenAI 官方公布的 Reset 时间。

---

## Codex 今天 Reset 了吗？

<!-- LIVE_STATUS_START -->

> **GitHub 状态快照：2026-09-20**  
> 当前 GitHub 自动同步尚未上线，实时状态请以 [Codex Reset Radar](https://codex-reset.aiplanwatch.com/) 为准。

**今天暂未记录新的 Verified Global Reset。**

- **最近一次已确认 Global Reset**：2026-09-12 08:09 UTC
- **来源**：Tibo · @thsottiaux
- **状态**：Verified
- **当前监控状态**：Monitoring

<!-- LIVE_STATUS_END -->

👉 [查看实时 Codex Reset 状态与原始来源](https://codex-reset.aiplanwatch.com/)

---

## 下一次 Codex Reset 什么时候？

<!-- FORECAST_START -->

当前网站基于已记录的公开 Global Reset 间隔给出的历史概率：

| 时间窗口 | 累计概率 |
| --- | ---: |
| 未来 24 小时 | 50% |
| 未来 48 小时 | 50% |
| 未来 72 小时 | 60% |

当前样本基于 **42 个已记录公开 Global Reset 间隔**，其中包含 10 个可比较样本。

<!-- FORECAST_END -->

> **Forecast ≠ Official Reset Time**  
> 这些结果用于辅助判断可能的时间窗口，不代表 OpenAI 官方 Reset Schedule。

👉 [查看实时 Forecast、图表与方法说明](https://codex-reset.aiplanwatch.com/)

👉 [了解 Forecast 如何理解](./docs/reset-forecast.md)

---

## 最近有什么 Reset 信号？

<!-- LATEST_SIGNALS_START -->

| 日期 | 类型 | 状态 | 摘要 |
| --- | --- | --- | --- |
| 2026-09-12 | Global Reset | 🟢 Verified | 已记录公开 Global Reset 完成信号 |
| 2026-09-05 | Banked Reset | 🟢 Recorded | Banked Reset 公开信号 |
| 2026-09-04 | Banked Reset | 🟢 Recorded | 部分用户 Banked Reset 公开信号 |

<!-- LATEST_SIGNALS_END -->

这里会明确区分：

- **Verified Reset**：已经有足够公开证据确认发生
- **Public Signal**：存在公开信号，但不能证明 Reset 已完成
- **Forecast**：根据历史数据和公开信息形成的预测

不会因为一条公开讨论提到 “reset”，就直接把它写成 Verified Reset。

👉 [查看完整 Timeline 与原始来源](https://codex-reset.aiplanwatch.com/)

---

## Codex Reset Radar 能帮你做什么？

### 如果你只是想知道“现在发生了什么”

你可以快速查看：

- ✅ Codex 今天有没有新的 Reset
- ✅ 最近一次 Global Reset 是什么时候
- ✅ 下一次 Reset 的 24h / 48h / 72h Forecast
- ✅ 最近有哪些 Tibo / Public Reset Signals
- ✅ Global Reset 与 Banked Reset 历史
- ✅ Codex Usage Limit / Reset Window 相关规则

最简单的使用方式：

🌐 https://codex-reset.aiplanwatch.com/

### 如果你习惯用微信

微信搜索：

**徐公 AI 雷达**

适合移动端快速查看 Reset 状态、历史、预测、提醒和相关指南。

### 如果你是开发者

本仓库会逐步提供机器可读的开放数据：

```text
data/
├── latest.json
├── resets.json
├── signals.json
└── forecast.json
```

未来可用于构建：

- Codex Reset Notification Bot
- Chrome Extension
- VS Code / Cursor Extension
- CLI
- GitHub Badge
- Status Dashboard
- Telegram / Discord / Slack Bot
- MCP / AI Agent

---

## 我应该怎么使用？

| 你的需求 | 推荐入口 |
| --- | --- |
| 看今天是否 Reset | [Live Radar](https://codex-reset.aiplanwatch.com/) |
| 看下一次 Reset Forecast | [Live Forecast](https://codex-reset.aiplanwatch.com/) |
| 看历史 Reset / Banked Reset | [Reset History](./docs/codex-reset-history.md) |
| 了解 Codex Reset 是什么 | [What is Codex Reset](./docs/what-is-codex-reset.md) |
| 了解 Usage Limit / Quota | [Codex Usage Limits](./docs/codex-usage-limits.md) |
| 微信里查看和接收相关提醒 | 微信搜索 **徐公 AI 雷达** |
| 获取机器可读数据 | Open Data（建设中） |
| 了解数据为什么这样分类 | [Methodology](./docs/methodology.md) |

---

## Open Data

Codex Reset Radar 不只是一个展示页面，我们希望逐步把 Reset History、Signal 和 Forecast 变成可引用、可复用的数据。

计划提供：

### `data/latest.json`

当前最新的 Reset 状态，适合 Dashboard、Bot、Extension、CLI 和 Widget。

### `data/resets.json`

Global Reset / Banked Reset 历史，适合 Timeline、数据分析和 Reset Interval 统计。

### `data/signals.json`

公开 Reset Signal，并与 Verified Reset 分开。

### `data/forecast.json`

未来 24h / 48h / 72h 等时间窗口的参考 Forecast。

> 这些 JSON 文件尚未正式接入自动同步；未上线前不会把规划中的接口写成已经可用。

---

## 为什么可以相信这些数据？

我们不会把所有 “Reset” 信息混成一种状态。

核心分类：

```text
Verified Reset
Public Signal
Forecast
Historical
Unconfirmed
```

处理原则很简单：

> **事实就是事实，信号就是信号，预测就是预测。**

例如：

- “Reset 已经完成”需要有可验证的公开证据
- “可能快 Reset”只能算 Public Signal
- “未来 24h 概率 60%”只能算 Forecast
- Forecast 不会包装成 OpenAI 官方时间

详细规则：

- [Methodology](./docs/methodology.md)
- [Data Sources](./docs/data-sources.md)

---

## Learn

如果你想进一步了解，而不是只看当前状态：

- [什么是 Codex Reset？什么时候 Reset？](./docs/what-is-codex-reset.md)
- [Codex Reset History](./docs/codex-reset-history.md)
- [Codex Usage Limits / Weekly Limit / Quota](./docs/codex-usage-limits.md)
- [Codex Reset Forecast](./docs/reset-forecast.md)
- [Methodology](./docs/methodology.md)
- [Data Sources](./docs/data-sources.md)

README 负责回答“现在发生了什么”。

Docs 负责解释“为什么、怎么算、历史是什么”。

---

## Roadmap

当前优先级：

- [x] Live Codex Reset Radar
- [x] Reset History
- [x] Global / Banked Reset 区分
- [x] Reset Forecast
- [x] Public Reset Signals
- [x] 微信小程序入口
- [x] GitHub 文档拆分
- [ ] Open JSON Data
- [ ] GitHub 自动数据同步
- [ ] README Live Status 自动更新
- [ ] Reset Status Badge
- [ ] ICS Calendar Feed
- [ ] Chrome Extension
- [ ] CLI / Webhook / MCP
- [ ] Telegram / Discord Notification
- [ ] Usage Limit Rule Change Log

---

## Star / Share

如果你经常会问：

> Codex 今天 Reset 了吗？  
> 下一次什么时候 Reset？

可以 ⭐ Star 这个仓库，或者直接分享实时页面：

https://codex-reset.aiplanwatch.com/

国内微信用户：

**微信搜索「徐公 AI 雷达」**

---

## Disclaimer

Codex Reset Radar 是独立社区项目。

- 不是 OpenAI 官方产品
- 不代表 OpenAI 发布 Reset 时间
- Forecast 不是官方 Reset Schedule
- Public Signal 不等于 Verified Reset
- Usage Limit、Quota 和 Reset 机制可能随产品规则变化

涉及具体产品规则时，应优先以相关产品官方最新信息为准。

OpenAI、Codex 及其他相关名称和商标归各自权利人所有。
