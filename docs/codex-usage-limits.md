# Codex Usage Limits

> 整理 Codex Usage Limit、Quota、Weekly Limit、Reset Window 等相关规则与变化。

[← 返回项目首页](../README.md) · [查看 Codex Reset Radar](https://codex-reset.aiplanwatch.com/)

## 为什么单独维护 Usage Limit 文档？

用户等待 Reset 的根本原因通常是使用额度或限制窗口。

因此，除了 “Codex 什么时候 Reset”，用户还会关心：

- Codex Usage Limit 怎么计算？
- Codex Weekly Limit 是多少？
- 5-hour window 如何计算？
- Codex Quota 什么时候恢复？
- `/usage` 显示的内容是什么意思？
- 不同模型是否消耗相同额度？
- Agent / Subagent 是否计入额度？
- Cache 是否影响 Usage？

这些问题与 Reset 高度相关，但属于独立的规则型搜索意图，因此不适合全部堆在 README。

## Usage Limit 会变化

Codex 的额度、套餐和限制机制可能随产品策略变化。

因此，本项目不会把某一次观察结果永久写成固定规则。

后续每条重要规则尽量记录：

- 规则内容
- 生效时间
- 更新时间
- 官方来源
- 社区观察
- 历史版本
- 是否仍然有效

## 5-hour Window

如果 Codex 产品存在时间窗口型额度，需要区分：

- 窗口起点
- 窗口长度
- 是滚动窗口还是固定时间窗口
- Reset 后是否重新计算
- 不同套餐是否一致

只有存在可验证依据时，才会将规则写成确定事实。

## Weekly Limit

Weekly Limit 同样需要区分：

- 周期如何起算
- 是否所有套餐一致
- 是否存在额外额度
- 是否存在临时规则调整
- 与其它时间窗口的关系

## /usage

如果产品提供 `/usage` 或类似 Usage 页面，本项目会优先记录官方界面实际表达的字段，而不是自行推断含义。

未来会逐步整理：

- 剩余额度
- 已使用额度
- 时间窗口
- Reset 时间
- 不同模型消耗

## Rule Change Log

后续计划维护 Usage / Limit 规则变化历史，例如：

| Date | Rule | Change | Source |
| --- | --- | --- | --- |
| YYYY-MM-DD | Weekly Limit | Updated | Official Source |

这能避免一篇老文章长期保留已经失效的规则。

## 与 Reset Radar 的关系

Usage Limit 回答：

> “我的额度为什么不可用了？”

Reset Radar 回答：

> “额度什么时候可能恢复，以及最近发生了什么？”

两者应该互相链接，但不混成一篇文档。

## 数据原则

如果某条规则只是社区观察，我们会尽量标注为社区信息。

如果规则来自官方文档，会保留对应来源。

具体来源策略：

[Data Sources](./data-sources.md)

---

**继续阅读**

- [什么是 Codex Reset？](./what-is-codex-reset.md)
- [Codex Reset History](./codex-reset-history.md)
- [Codex Reset Forecast](./reset-forecast.md)
- [Data Sources](./data-sources.md)
