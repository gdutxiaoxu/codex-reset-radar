# Data Sources

> Codex Reset Radar 的数据来源、来源分级、引用和修正规则。

[← 返回项目首页](../README.md)

## 数据来源原则

项目尽量使用能够公开验证的信息。

可能的数据来源包括：

- 官方公开信息
- 官方帮助中心
- 产品界面公开信息
- 公开社交媒体信号
- 已验证的 Reset 历史记录
- 社区公开讨论

不同来源的可靠程度并不相同，因此不会把所有来源当成同一等级。

## Official Sources

如果存在官方文档、帮助中心、产品界面或官方公开说明，应优先使用这些信息描述产品规则。

对于容易变化的 Usage Limit、Quota、Reset Rule，应尽量记录来源日期。

## Public Social Signals

公开社交平台中的 Reset 信号可以作为：

```text
public_signal
```

但不会因为某个公开账号提到 “reset” 就自动成为：

```text
verified_reset
```

## Community Sources

社区讨论可以帮助发现：

- 新规则变化
- 用户共同遇到的问题
- 潜在 Reset 事件
- Usage Limit 差异

但社区观察需要与 Verified 数据保持区分。

## Source Reliability

数据记录可以根据实际实现维护类似状态：

```text
verified
public_signal
forecast
historical
unconfirmed
```

这些状态描述的是本项目对事件的处理阶段，不代表来源主体的官方身份。

## Attribution

对于外部公开来源，应尽量保留：

- Source name
- Source URL
- Published time
- Retrieved / observed time
- Necessary structured summary

原则上优先保存结构化信息和链接，不长期镜像第三方完整正文。

## Copyright

项目不应把第三方帖子、文章或文档全文复制到仓库作为自己的内容。

如果需要引用，应保留必要的结构化摘要并链接回原始公开来源。

## Correction Requests

如果发现：

- 来源错误
- 时间错误
- 分类错误
- 事件重复
- 内容归属错误

可以通过 GitHub Issue 或 Pull Request 提交修正，并尽量提供可公开验证的依据。

## 数据与 Forecast

来源数据可以成为 Forecast 的输入，但：

> **来源中的预测 ≠ 本项目 Forecast**

> **本项目 Forecast ≠ 官方 Reset Schedule**

详细分类规则：

[Methodology](./methodology.md)

---

**相关文档**

- [什么是 Codex Reset？](./what-is-codex-reset.md)
- [Codex Reset History](./codex-reset-history.md)
- [Codex Usage Limits](./codex-usage-limits.md)
- [Codex Reset Forecast](./reset-forecast.md)
