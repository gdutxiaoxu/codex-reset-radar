# 什么是 Codex Reset？

> 本文解释 Codex Reset、Reset Time、Global Reset、Banked Reset，以及如何区分已确认的 Reset、公开信号和预测。

[← 返回项目首页](../README.md) · [查看实时 Codex Reset Radar](https://codex-reset.aiplanwatch.com/)

## Codex Reset 是什么？

当 Codex 用户达到某些使用额度、时间窗口或产品限制后，通常需要等待相应额度恢复。用户因此经常会关注：

- Codex 什么时候 Reset？
- Codex Reset Time 是否固定？
- Codex Weekly Reset 怎么计算？
- Codex Quota 什么时候恢复？
- Global Reset 和 Banked Reset 有什么区别？

“Reset”并不总是一个单一事件。不同公开信息可能分别属于已经确认发生的 Reset、公开 Reset 信号、额外额度或 Banked Reset、历史规律，以及统计预测。

Codex Reset Radar 的核心原则是：

> **尽可能把“已经发生的事实”、“公开信号”和“统计预测”分开。**

## Codex 什么时候 Reset？

这是最常见的问题之一：

> **When does Codex reset?**

Codex 的 Reset 时间不应简单理解为“每周固定星期几、固定几点一定 Reset”。

实际情况可能受到以下因素影响：

- 当前产品规则
- 用户套餐
- 使用窗口
- Weekly Limit
- 临时活动或额外额度
- Banked Reset
- 产品策略变化
- 官方临时调整

因此，Codex Reset Radar 不会把未经验证的固定时间当成事实。

## Verified Reset

**Verified Reset** 表示已经有足够公开证据，可以确认一次 Reset 事件已经发生。

记录时会尽量保存：

- Reset 时间
- Reset 类型
- 首次公开信号时间
- 确认时间
- 来源
- 来源 URL
- 验证状态

## Public Reset Signal

**Public Reset Signal** 指公开渠道出现了与 Reset 相关的信号，但这些信息本身不能证明 Reset 已经完成。

例如，“Reset 可能快来了”应当记录为 Signal，而不是直接写成 Verified Reset。

## Historical Pattern

**Historical Pattern** 是从历史 Reset 记录中观察到的时间规律。

它可以辅助理解 Reset 的周期，但历史规律不代表未来一定继续保持。

## Forecast

**Forecast** 是根据历史数据、时间分布和公开信号形成的统计预测。

因此：

> **Forecast ≠ Official Reset Time**

> **Public Signal ≠ Verified Reset**

## Codex Global Reset

在本项目的数据定义中，**Global Reset** 用于描述有足够公开信息表明发生了较广泛 Codex 使用额度恢复的事件。

对于 Global Reset，我们尽量记录：

- Reset 时间
- 首次公开信号
- 确认时间
- Reset 类型
- 来源 URL
- 与上一次 Reset 的间隔

## Codex Banked Reset

**Banked Reset** 用于描述部分与额外额度、额度补充、Reset Card 或类似机制相关的事件。

数据层会明确区分：

```text
global_reset
banked_reset
```

出现 “reset” 关键词的公开讨论不会自动被归类为 Global Reset。

## 如何查看最新 Codex Reset？

你可以通过三个入口查看：

### Web

实时状态、Timeline、Forecast 与来源：

https://codex-reset.aiplanwatch.com/

### GitHub

本仓库将逐步提供：

```text
data/latest.json
data/resets.json
```

### 微信小程序

微信搜索：

```text
徐公 AI 雷达
```

## FAQ

### Codex Reset Time 是官方公布的吗？

不一定。本项目会区分 Verified Reset、Public Signal 和 Forecast。

### Codex Reset Forecast 是 OpenAI 官方预测吗？

不是。Forecast 是基于历史数据和公开信息形成的统计结果，不是 OpenAI 官方 Reset Schedule。

### Codex Reset Radar 是 OpenAI 官方项目吗？

不是。Codex Reset Radar 是独立社区项目，与 OpenAI 没有官方隶属或合作关系。

---

**继续阅读**

- [Codex Reset History](./codex-reset-history.md)
- [Codex Usage Limits](./codex-usage-limits.md)
- [Codex Reset Forecast](./reset-forecast.md)
- [Methodology](./methodology.md)
- [Data Sources](./data-sources.md)
