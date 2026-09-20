# Codex Reset Forecast

> 说明 Codex Reset Radar 如何展示下一次 Reset 的参考时间窗口，以及 Forecast 与官方 Reset 时间的区别。

[← 返回项目首页](../README.md) · [查看实时 Forecast](https://codex-reset.aiplanwatch.com/)

## Forecast 想解决什么问题？

除了查询最近一次 Reset，用户最常问的是：

> **When will Codex reset?**

也就是：

> 下一次 Codex Reset 可能什么时候发生？

Codex Reset Radar 会尝试基于历史 Reset 时间、Reset 间隔和公开信号，形成未来不同时间窗口的参考预测。

例如：

```text
Within 24h
Within 48h
Within 72h
```

## Forecast 不是官方时间

必须明确：

> **Codex Reset Forecast 是统计预测，不是 OpenAI 官方公布的 Reset 时间。**

因此：

```text
Forecast ≠ Official Reset Schedule
```

任何概率都不应被解释为：

> “OpenAI 已经确认会在这个时间 Reset。”

## 可能使用的信息

Forecast 可以参考：

- 已验证 Reset 历史
- Reset 间隔
- 最近公开 Signal
- 历史时间分布
- 已知规则变化

具体使用哪些字段，应以实际实现和 Methodology 为准。

## 为什么 Forecast 会变化？

预测可能因为以下原因发生变化：

- 新的公开 Signal 出现
- 新 Reset 被确认
- 历史数据被修正
- 官方策略变化
- 临时额度调整
- 新套餐上线
- Reset 机制变化
- 数据样本不足

因此 Forecast 应被理解为动态结果，而不是固定承诺。

## 24h / 48h / 72h

未来可以通过：

```text
data/forecast.json
```

提供机器可读的 Forecast。

示例：

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

这些值仅表示模型或统计方法给出的参考概率。

## Forecast 与 Public Signal 的区别

### Public Signal

公开渠道中出现与 Reset 有关的信息。

### Forecast

根据数据计算得到的预测。

一条 Signal 可以成为 Forecast 的输入，但：

```text
Signal ≠ Forecast
Signal ≠ Verified Reset
Forecast ≠ Verified Reset
```

## Forecast 与 Reset History 的关系

历史数据是 Forecast 的基础之一。

完整历史说明：

[Codex Reset History](./codex-reset-history.md)

方法论：

[Methodology](./methodology.md)

## 实时 Forecast

图表、时间线和最新结果：

https://codex-reset.aiplanwatch.com/

---

**继续阅读**

- [Codex Reset History](./codex-reset-history.md)
- [Methodology](./methodology.md)
- [Data Sources](./data-sources.md)
