# Codex Reset Radar

> 跟踪 Codex Reset 公开信号、历史重置记录、重置状态与预测，并提供可供开发者使用的开放数据。

**Codex Reset Radar** 是一个独立的 Codex Reset 跟踪项目，面向关注 **Codex Reset、Codex Reset Time、Codex Usage Limit、Codex Quota、Codex Reset History** 的用户与开发者。

项目会持续整理已经确认发生的 Codex Reset、公开 Reset 信号、历史重置记录，并基于历史数据与公开信息提供下一次 Reset 时间窗口的参考预测。

如果你只想快速查看当前最新的 Codex Reset 状态、Reset Timeline、历史记录和预测，可以直接访问：

**🌐 Codex Reset Radar 网站**

https://codex-reset.aiplanwatch.com/

国内微信用户也可以直接搜索：

**📱 微信小程序：徐公 AI 雷达**

用于查看 Codex Reset 状态、历史记录、预测、提醒以及相关使用指南。

> Codex Reset Radar 是独立社区项目，与 OpenAI 没有官方隶属或合作关系。预测结果不是 OpenAI 官方公布的 Reset 时间。

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

查看实时状态、完整 Reset Timeline、历史记录与预测：

👉 https://codex-reset.aiplanwatch.com/

---

## 什么是 Codex Reset？

当 Codex 用户达到某些使用额度、时间窗口或产品限制后，通常需要等待相应额度恢复。

因此，用户经常会搜索：

- `codex reset`
- `codex reset time`
- `when does codex reset`
- `when will codex reset`
- `codex usage limit`
- `codex quota reset`
- `codex weekly reset`
- `codex next reset`

但实际使用过程中，“Reset”并不总是一个单一概念。

公开信息可能分别属于：

1. 已经确认发生的 Reset
2. 即将发生 Reset 的公开信号
3. 额度补充或 Banked Reset
4. 根据历史规律计算出的 Forecast
5. Codex Usage Limit 或产品规则变化
6. 用户个人账号的额度恢复

因此，Codex Reset Radar 的一个核心原则是：

> **尽可能把“已经发生的事实”、“公开信号”和“统计预测”分开。**

避免把 Forecast 误认为官方 Reset 时间，也避免把一条公开讨论直接判断为已经发生 Reset。

---

## Codex 什么时候 Reset？

这是 Codex 用户最常问的问题之一：

> **When does Codex reset?**

Codex 的 Reset 时间不应被简单理解为“每周固定星期几、固定几点一定 Reset”。

实际情况可能受到多种因素影响，例如：

- 当前产品规则
- 用户套餐
- 使用窗口
- Weekly Limit
- 临时活动或额外额度
- Banked Reset
- 产品策略变化
- 官方临时调整

因此，Codex Reset Radar 不会简单给出未经验证的固定 Reset 时间，而是将信息区分为以下几个层级。

### Verified Reset

已经有公开证据可以确认发生的 Reset。

### Public Reset Signal

公开渠道出现与 Reset 相关的信号，但不能证明 Reset 已经完成。

### Historical Pattern

根据历史 Reset 记录观察到的时间规律。

### Forecast

根据历史数据、时间分布和公开信号生成的统计预测。

因此：

> **Forecast ≠ Official Reset Time**

> **Public Signal ≠ Verified Reset**

查看当前 Codex Reset 状态：

👉 https://codex-reset.aiplanwatch.com/

---

## Codex Global Reset

`Global Reset` 是本项目重点跟踪的事件类型之一。

在本项目的数据定义中，Global Reset 用于描述有足够公开信息表明发生了较广泛 Codex 使用额度恢复的事件。

对于 Global Reset，我们计划尽量记录：

- Reset 时间
- 首次公开信号时间
- 确认时间
- 信息来源
- 来源 URL
- Reset 类型
- 验证状态
- 与上一次 Reset 的时间间隔

结构化历史数据将逐步维护在：

```text
data/resets.json
```

同时可以通过网页版查看更加直观的 Reset Timeline：

https://codex-reset.aiplanwatch.com/

---

## Codex Banked Reset

除了 Global Reset，本项目也会记录部分与 **Banked Reset、额外额度、Reset Card** 等相关的事件。

为了避免不同类型的数据混在一起，数据层会明确区分不同事件类型，例如：

```text
global_reset
banked_reset
```

如果某个事件只是公开讨论、额度补充、Reset Card 或其他相关机制，也不会因为出现 “reset” 关键词就自动归类为 Global Reset。

这样做的目的，是让历史数据尽可能保持可解释性。

---

## Codex Usage Limit

除了 Reset Time，本项目也会持续整理与 **Codex Usage Limit** 相关的信息。

常见问题包括：

- Codex 有多少额度？
- Codex Usage Limit 怎么计算？
- Codex Weekly Limit 是多少？
- Codex 什么时候恢复额度？
- 5-hour window 如何计算？
- Weekly Reset 如何计算？
- 不同模型是否消耗相同额度？
- Agent / Subagent 是否计入额度？
- Cache 是否影响 Usage？
- `/usage` 显示的内容是什么意思？

这些规则可能随着产品调整发生变化，因此本项目不会把某一次观察结果永久当成固定规则。

未来相关规则会尽量记录：

- 规则内容
- 更新时间
- 来源
- 历史版本
- 是否为官方信息
- 是否为社区观察

计划维护在：

```text
docs/codex-usage-limits.md
```

---

## Codex Reset History

Reset History 是 Codex Reset Radar 最重要的数据资产之一。

项目希望逐步形成一个结构化的 Codex Reset 历史数据集，包括：

- Reset Date
- Reset Type
- Published Signal
- Verified Time
- Source
- Source URL
- Previous Reset Interval

完整历史数据计划提供：

```text
data/resets.json
```

可视化 Reset Timeline：

👉 https://codex-reset.aiplanwatch.com/

---

## Codex Reset Forecast

除了记录历史数据，Codex Reset Radar 也尝试回答另一个高频问题：

> **When will Codex reset?**

也就是：

> 下一次 Codex Reset 可能什么时候发生？

项目会基于历史 Reset 时间、Reset 间隔，以及可以公开获取的信号，计算不同时间窗口可能发生 Reset 的参考概率。

例如：

```text
Within 24h
Within 48h
Within 72h
```

但必须特别说明：

> **Codex Reset Forecast 是统计预测，不是 OpenAI 官方公布的 Reset 时间。**

预测可能因为以下情况发生较大偏差：

- 官方策略变化
- 临时额度调整
- 新套餐上线
- Reset 机制变化
- 数据样本不足
- 公开信号突然变化

因此请将 Forecast 理解为辅助判断 Reset 时间窗口的工具，而不是官方承诺的 Reset 时间。

完整预测与图表：

👉 https://codex-reset.aiplanwatch.com/

---

## Public Reset Signals

Codex Reset Radar 还会记录公开渠道出现的 Reset Signal。

Signal 可能包括：

- Reset 相关公开消息
- Reset Forecast
- Usage / Quota 变化
- Banked Reset 相关信息
- 产品额度规则变化
- 其他可以帮助判断 Reset 状态的公开信号

结构化数据计划保存在：

```text
data/signals.json
```

Signal 数据主要保存：

- 发布时间
- 来源
- 来源 URL
- 事件类型
- 结构化摘要
- 验证状态

一条普通公开讨论不会被直接标记为 Verified Reset。

---

## Open Codex Reset Data

Codex Reset Radar 不只是一个 Reset 网站。

我们希望它同时成为一个：

> **Codex Reset Open Data Project**

本仓库将逐步提供机器可读的公开数据：

```text
data/
├── latest.json
├── resets.json
├── signals.json
└── forecast.json
```

### latest.json

提供当前最新 Codex Reset 状态，适合：

- Dashboard
- Chrome Extension
- Bot
- CLI
- Widget
- Status Badge
- MCP / AI Agent

示例结构：

```json
{
  "product": "codex",
  "status": "monitoring",
  "last_verified_reset": {
    "type": "global_reset",
    "effective_at": "2026-09-12T08:09:00Z",
    "source_url": "https://..."
  },
  "forecast": {
    "24h": 0.5,
    "48h": 0.5,
    "72h": 0.6
  }
}
```

### resets.json

用于记录 Codex Reset History。

```json
{
  "events": [
    {
      "date": "2026-09-12",
      "type": "global_reset",
      "verified": true,
      "source_url": "https://..."
    }
  ]
}
```

适合用于：

- Reset History
- Timeline
- 数据分析
- Reset 间隔统计
- Forecast Model

### signals.json

用于保存公开 Reset Signal。

```json
{
  "signals": [
    {
      "type": "reset_forecast",
      "published_at": "2026-09-20T00:00:00Z",
      "source_url": "https://...",
      "status": "public_signal"
    }
  ]
}
```

### forecast.json

用于提供 Reset Forecast。

```json
{
  "generated_at": "2026-09-20T00:00:00Z",
  "forecast": {
    "24h": 0.5,
    "48h": 0.6,
    "72h": 0.7
  }
}
```

Forecast 数据不代表官方 Reset Schedule。

---

## 开发者可以用这些数据做什么？

本仓库的目标之一，是让 Codex Reset 数据可以被其他开发者真正使用，而不仅仅是展示。

### Reset Tracker

实时展示最新 Codex Reset。

### Reset Notification Bot

可以基于数据构建：

- Telegram Bot
- Discord Bot
- Slack Bot
- 飞书机器人
- 企业微信机器人

### Chrome Extension

在浏览器中查看：

```text
Last Reset
Next Reset Forecast
Usage Status
```

### VS Code / Cursor Extension

在编辑器状态栏中展示 Reset 信息。

### CLI

例如：

```bash
codex-reset
```

输出：

```text
Codex Reset Radar

Last verified reset:
2026-09-12

Current status:
Monitoring

24h forecast:
50%
```

### README Badge

未来可以提供类似：

```text
Codex Reset · Last Reset: Sep 12
```

的状态 Badge，让其他项目直接引用。

### MCP / AI Agent

让 AI Agent 可以查询：

- 最近一次 Codex Reset 是什么时候？
- 未来 24 小时 Reset 概率是多少？
- 最近有哪些 Reset Signals？
- 最近 Codex Usage Limit 规则是否变化？

---

## 数据更新机制

本仓库的数据计划由现有数据服务自动同步，而不是长期人工维护。

整体流程：

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

只有真实业务数据发生变化时，才产生新的 Git commit。

### 可能触发 GitHub 更新的事件

例如：

- New Global Reset
- New Banked Reset
- Verified Status Changed
- Important Public Signal
- Historical Data Correction
- Meaningful Forecast Change

不会因为单纯的：

- `last_checked_at`
- Collector heartbeat
- API 请求
- 无意义时间戳变化

不断制造 Commit。

这样 Git History 本身也可以成为一份：

> **Codex Reset Changelog**

---

## 数据来源与验证

Codex Reset Radar 尽量只使用能够公开验证的信息。

数据来源可能包括：

- 官方公开信息
- 官方帮助中心
- 产品界面公开信息
- 公开社交媒体信号
- 已验证的 Reset 历史记录
- 社区公开讨论

不同来源的可靠程度并不相同，因此项目会尽可能区分：

```text
verified
public_signal
forecast
historical
unconfirmed
```

未来详细方法说明将放在：

```text
docs/methodology.md
```

数据来源说明：

```text
docs/data-sources.md
```

---

## 为什么区分 Verified、Signal 和 Forecast？

这是整个项目最重要的原则之一。

假设有人公开表示：

> “Reset 可能快来了。”

这最多只能被记录为：

```text
Public Signal
```

不能直接写成：

```text
Codex Reset 已经发生
```

类似地，如果历史模型计算：

```text
未来 24h 概率 60%
```

也只能作为：

```text
Forecast
```

而不是：

```text
OpenAI 将在未来 24h Reset
```

因此：

```text
Verified Reset
        ≠
Public Signal
        ≠
Forecast
```

这三个概念在数据和页面中会尽量保持独立。

---

## Live Codex Reset Radar

如果你不需要 JSON 数据，只想快速查看：

- Codex 是否刚刚 Reset
- 最近一次 Reset 时间
- Reset History
- 最新 Public Signal
- 下一次 Reset Forecast
- Reset Timeline
- 相关规则

可以直接使用网页版：

### 🌐 Codex Reset Radar

https://codex-reset.aiplanwatch.com/

网页版会提供更加完整的 Timeline、Charts、Forecast、History、Sources 与 Methodology。

---

## 微信小程序：徐公 AI 雷达

国内用户也可以通过微信小程序查看 Codex Reset 信息。

### 📱 徐公 AI 雷达

在微信中搜索：

```text
徐公 AI 雷达
```

小程序主要用于提供：

- Codex Reset 状态
- 最近 Reset
- Reset 历史
- Reset 预测
- Reset 公开信号
- Reset 提醒
- 相关使用指南

后续可以在仓库中加入小程序二维码：

```text
assets/wechat-miniapp-qrcode.png
```

如果你正在手机上浏览 GitHub，可以直接打开微信搜索：

**徐公 AI 雷达**

---

## 网站、GitHub 与小程序的关系

Codex Reset Radar 目前主要由三个入口组成。

### Website

适合：

- Google Search 用户
- 普通 Codex 用户
- 希望查看图表和 Timeline 的用户
- 希望快速了解当前 Reset 状态的用户

访问：

https://codex-reset.aiplanwatch.com/

### GitHub

适合：

- 开发者
- Open Data 使用者
- Bot / Extension 开发者
- 研究 Reset History 的用户
- 想基于公开数据构建工具的用户

仓库：

https://github.com/gdutxiaoxu/codex-reset-radar

### 微信小程序

适合：

- 国内微信用户
- 移动端快速查看
- Reset 提醒
- 分享 Reset 状态

微信搜索：

```text
徐公 AI 雷达
```

三个入口会尽量使用一致的数据逻辑与 Reset 分类标准。

---

## FAQ

### Codex Reset 是什么？

Codex Reset 一般用于描述 Codex 使用额度、Quota 或某个限制窗口恢复，使用户可以继续使用相关能力。

具体 Reset 机制可能随着套餐与产品规则变化。

### Codex 什么时候 Reset？

Codex Reset 不应该被假设为长期固定星期和固定时间。

Codex Reset Radar 会根据已经确认的历史 Reset、公开信号与历史规律展示当前状态以及可能的 Reset 时间窗口。

查看实时状态：

https://codex-reset.aiplanwatch.com/

### Codex Reset Time 是官方公布的吗？

不一定。

本项目会明确区分：

```text
Verified Reset
Public Signal
Forecast
```

只有能够确认已经发生的事件才会标记为 Verified Reset。

### Codex Reset Forecast 是 OpenAI 官方预测吗？

不是。

Forecast 是 Codex Reset Radar 根据历史数据与公开信息生成的统计结果，不是 OpenAI 官方 Reset Schedule。

### 什么是 Global Reset？

Global Reset 是本项目用于分类较广泛 Reset 事件的数据类型。

具体事件是否归类为 Global Reset，需要结合公开证据判断。

### 什么是 Banked Reset？

Banked Reset 用于描述部分与额外额度、额度补充或类似 Reset 机制相关的事件。

它不会与 Global Reset 混为一类。

### 怎么查看最新 Codex Reset？

可以通过三个入口：

1. Web：  
   https://codex-reset.aiplanwatch.com/

2. GitHub：  
   后续查看 `data/latest.json`

3. 微信：  
   搜索 **徐公 AI 雷达**

### 有 Codex Reset History 吗？

有。

后续 GitHub 会提供：

```text
data/resets.json
```

网页版也会持续展示 Reset Timeline：

https://codex-reset.aiplanwatch.com/

### 可以获取 Codex Reset JSON 数据吗？

可以。

本仓库计划持续提供：

```text
data/latest.json
data/resets.json
data/signals.json
data/forecast.json
```

### 可以用这些数据做自己的工具吗？

项目目标就是让公开数据能够被开发者用于构建：

- Codex Reset Bot
- Chrome Extension
- VS Code / Cursor Extension
- Status Dashboard
- CLI
- MCP
- GitHub Badge

具体授权方式以后续 License 为准。

### 有 Codex Reset Notification 吗？

网页版与 **徐公 AI 雷达** 会逐步完善 Reset 提醒能力。

GitHub 开放数据未来也可以用于开发自己的 Notification Bot。

### Codex Reset Radar 是 OpenAI 官方项目吗？

不是。

Codex Reset Radar 是独立社区项目，与 OpenAI 没有官方隶属或合作关系。

OpenAI、Codex 以及相关名称和商标归各自权利人所有。

---

## Roadmap

当前规划包括：

- [x] Codex Reset History
- [x] Reset 状态展示
- [x] Reset Forecast
- [x] Public Reset Signals
- [x] Web Dashboard
- [x] 微信小程序入口
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

计划目录：

```text
codex-reset-radar/
│
├── README.md
├── README.zh-CN.md
│
├── data/
│   ├── latest.json
│   ├── resets.json
│   ├── signals.json
│   └── forecast.json
│
├── schema/
│   ├── reset.schema.json
│   └── signal.schema.json
│
├── docs/
│   ├── methodology.md
│   ├── data-sources.md
│   ├── codex-reset-history.md
│   ├── codex-usage-limits.md
│   └── api.md
│
├── examples/
│   ├── javascript.js
│   └── python.py
│
├── assets/
│   ├── logo.png
│   ├── social-preview.png
│   ├── web-screenshot.png
│   └── wechat-miniapp-qrcode.png
│
└── .github/
    └── workflows/
```

---

## Contributing

欢迎提交：

- Reset 历史修正
- 数据来源补充
- 新 Reset Signal
- Bug Report
- JSON Schema 建议
- 文档改进
- Usage Limit 规则变化

如果提交 Reset 相关数据，请尽量提供公开可验证的来源。

单独的“我的账号好像 Reset 了”可以作为线索，但不会直接成为 Verified Reset。

---

## Star

如果这个项目对你有帮助，可以给仓库一个 ⭐ Star。

这能帮助更多正在搜索：

- `codex reset`
- `codex reset time`
- `when does codex reset`
- `codex usage limit`
- `codex quota`
- `codex reset history`

的开发者发现这个项目。

你也可以直接使用：

🌐 https://codex-reset.aiplanwatch.com/

或者在微信中搜索：

📱 **徐公 AI 雷达**

---

## Disclaimer

Codex Reset Radar 是独立社区项目。

本项目：

- 不是 OpenAI 官方产品
- 不代表 OpenAI 发布 Reset 时间
- 不保证 Forecast 一定发生
- 不保证公开 Signal 最终一定对应 Reset
- 不应将预测数据理解为官方承诺

Reset Forecast 仅用于信息参考。

产品规则、Usage Limit、Quota 和 Reset 机制可能随时发生变化。

涉及具体产品规则时，应优先以相关产品官方最新信息为准。

OpenAI、Codex 及其他相关名称和商标归各自权利人所有。

---

## Links

### Live Codex Reset Radar

https://codex-reset.aiplanwatch.com/

### GitHub

https://github.com/gdutxiaoxu/codex-reset-radar

### WeChat Mini Program

微信搜索：

```text
徐公 AI 雷达
```

---

如果你正在等待下一次 Codex Reset，可以从这里开始：

👉 https://codex-reset.aiplanwatch.com/

国内微信用户：

👉 **微信搜索「徐公 AI 雷达」**

开发者：

👉 **Star 本仓库，并关注后续开放 JSON 数据、Badge、CLI、Chrome Extension 与更多开发者能力。**
