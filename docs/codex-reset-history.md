# Codex Reset History

> 记录已经确认的 Codex Reset 历史、事件类型、公开来源和 Reset 间隔。

[← 返回项目首页](../README.md) · [查看实时 Timeline](https://codex-reset.aiplanwatch.com/)

## 为什么记录 Reset History？

Reset History 是 Codex Reset Radar 最重要的数据资产之一。

单独记录历史数据，可以帮助：

- 查询最近一次 Codex Reset
- 观察不同 Reset 之间的时间间隔
- 区分 Global Reset 与 Banked Reset
- 追踪产品规则变化
- 为 Reset Forecast 提供历史样本
- 为开发者提供机器可读的数据

## 计划记录的字段

每个 Reset Event 会尽量包含：

```text
event_id
date
effective_at
type
status
first_signal_at
verified_at
source
source_url
previous_reset_interval
```

其中：

- `type`：例如 `global_reset`、`banked_reset`
- `status`：例如 `verified`、`unconfirmed`
- `source_url`：公开可验证来源
- `previous_reset_interval`：与上一条相同类型 Reset 的时间间隔

## Reset 类型

### Global Reset

用于描述有足够公开信息表明发生了较广泛额度恢复的事件。

### Banked Reset

用于描述部分与额外额度、额度补充或类似机制相关的事件。

不同类型不会因为都包含 “reset” 而合并为同一种事件。

## 历史数据

结构化历史数据计划维护在：

```text
data/resets.json
```

示例：

```json
{
  "events": [
    {
      "date": "2026-09-12",
      "type": "global_reset",
      "status": "verified",
      "source_url": "https://..."
    }
  ]
}
```

## 数据如何进入历史记录？

一条公开消息不会自动成为历史 Reset。

通常会经历：

```text
Public Signal
    ↓
Collect
    ↓
Classify
    ↓
Verify
    ↓
Reset History
```

具体规则请查看：

[Methodology](./methodology.md)

## 历史修正

如果后续发现：

- 时间记录错误
- Reset 类型分类错误
- 来源失效或错误
- Signal 被误认为 Verified Reset

项目会修正历史数据，并保留相应 Git commit。

因此 Git History 本身也可以作为 Reset 数据变更记录。

## 可视化 Timeline

如果只想看图表和时间线，可以直接访问：

https://codex-reset.aiplanwatch.com/

## 开放数据

计划提供：

```text
data/latest.json
data/resets.json
```

开发者可以用于：

- Reset Timeline
- 数据分析
- Reset 间隔统计
- Forecast Model
- Bot / Extension
- Dashboard

---

**继续阅读**

- [什么是 Codex Reset？](./what-is-codex-reset.md)
- [Codex Reset Forecast](./reset-forecast.md)
- [Methodology](./methodology.md)
- [Data Sources](./data-sources.md)
