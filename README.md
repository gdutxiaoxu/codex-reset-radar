# Codex Reset Radar

> **Codex 今天 Reset 了吗？下一次什么时候可能 Reset？**

Codex Reset Radar 持续跟踪 **Codex Global Reset、Banked Reset、公开 Reset Signal、历史记录和下一次 Reset Forecast**。本仓库同时发布版本化的 JSON 数据快照，方便用户查看，也方便开发者构建自己的提醒、Bot、Extension 和 Dashboard。

🌐 **实时 Radar**：https://codex-reset.aiplanwatch.com/

📱 **微信小程序**：微信搜索 **徐公 AI 雷达**

> 独立社区项目，与 OpenAI 没有官方隶属或合作关系。Forecast 不是 OpenAI 官方公布的 Reset 时间。

---

## Codex 今天 Reset 了吗？

<!-- LIVE_STATUS_START -->

> **GitHub 状态快照：2026-09-24（UTC）**

**今天（UTC）暂未记录新的 Global Reset。**

- **最近一次已记录 Global Reset**：2026-09-12 08:09 UTC
- **来源**：[Tibo · @thsottiaux](https://x.com/thsottiaux/status/2098685367058612394)
- **状态**：已记录
- **当前监控状态**：Monitoring

<!-- LIVE_STATUS_END -->

👉 [查看实时 Codex Reset 状态与原始来源](https://codex-reset.aiplanwatch.com/)

---

## 下一次 Codex Reset 什么时候？

<!-- FORECAST_START -->

当前没有可公开展示的 Forecast。实时状态请查看 [Codex Reset Radar](https://codex-reset.aiplanwatch.com/)。

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
| 2026-09-22 | Reset Announcement | 已记录 | [GPT-6 Sol and Luna are out. Not only are they a very significant improvement across the board, but also in writing and general "you know when you try it" quality. We are also permanently reducing the API price by 50% making both of them viable for a ton of new usecases and makin…](https://x.com/thsottiaux/status/2102463847714247142) |
| 2026-09-19 | Forecast Signal | 已记录 | [推断预测：Tibo 对重置卡请求直接回复“OK fine”，因此判断为较强的重置卡暗示。结合上下文，将 Tuesday 作为预测时间参考；按美国太平洋时间计算，预计重置卡发送时间对应北京时间周二15:00至周三14:59。](https://x.com/thsottiaux/status/2101352781219258527) |
| 2026-09-12 | Reset Announcement | 已记录 | [Reset all propagated. Sweet dreams. https://t.co/VgKVUixoJG](https://x.com/thsottiaux/status/2098685367058612394) |
| 2026-09-11 | Forecast Signal | 已记录 | [@CtrlAltDwayne 当我说为现有用户提供优质服务时，这就包括偶尔的 Reset](https://x.com/thsottiaux/status/2098300424520687965) |
| 2026-09-07 | Forecast Signal | 已记录 | [永远不会放弃你 永远不会让你失望 永远不会跑开抛弃你 永远不会让你哭泣 永远不会说再见 永远不会说谎伤害你 感谢阅读。我们将对所有付费订阅的用量进行一次全局 Reset，这样你在用 Blender 做有趣的 3D 建模把额度全部用完之后，还能继续享受 Astra。工作周即将开始。 今日太平洋时间下午6点左右落地。](https://x.com/thsottiaux/status/2097043464538264003) |

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

本仓库已发布机器可读的开放数据快照：

```text
data/
├── latest.json
├── resets.json
├── signals.json
└── forecast.json
```

每份文件包含 `schema_version` 与 `generated_at`。数据是随 Git 提交更新的公开快照，不承诺实时性或固定刷新频率；使用前请读取最新提交和 [开放数据说明](./docs/open-data.md)。

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
| 获取机器可读数据 | [Open Data JSON 快照](./docs/open-data.md) |
| 了解数据为什么这样分类 | [Methodology](./docs/methodology.md) |

---

## Open Data JSON 快照

Codex Reset Radar 不只是一个展示页面。仓库中的 [`data/`](./data/) 提供可引用、可复用的版本化 JSON 快照。它们是公开数据镜像，**不是实时 API，也不是 OpenAI 官方状态接口**。

可直接读取：

### [`data/latest.json`](./data/latest.json)

当前状态：产品、监控状态、最近 Global Reset、最近公开信号和 Forecast 可用性。

### [`data/resets.json`](./data/resets.json)

Global Reset / Banked Reset 历史，适合 Timeline、数据分析和 Reset Interval 统计。

### [`data/signals.json`](./data/signals.json)

公开 Reset Signal，并与 Verified Reset 分开。

### [`data/forecast.json`](./data/forecast.json)

未来时间窗口的参考 Forecast，或明确的不可用状态。

字段、状态语义、兼容规则与使用边界见 [开放数据说明](./docs/open-data.md)。Forecast 不是 OpenAI 官方 Reset 时间；缺少可公开展示的 Forecast 时，数据会明确标为不可用，不会补造概率。

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
- [Open Data JSON 快照](./docs/open-data.md)

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
- [x] Open JSON Data 快照
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
