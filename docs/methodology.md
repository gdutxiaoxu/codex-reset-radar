# Methodology

> Codex Reset Radar 的事件分类、验证、去重、修正与 Forecast 方法说明。

[← 返回项目首页](../README.md)

## 目标

本项目最重要的原则不是“尽可能多收集 Reset 内容”，而是让不同类型的信息保持可解释。

核心区分：

```text
Verified Reset
Public Signal
Forecast
Historical Pattern
Unconfirmed
```

## Event Classification

### verified

存在足够公开证据，可以确认对应事件已经发生。

### public_signal

存在公开的 Reset 相关信号，但不能证明 Reset 已经发生。

### forecast

由统计或模型方法产生的预测。

### historical

来自已经记录并确认的历史事件。

### unconfirmed

目前证据不足，不能进入 Verified 数据。

## Global Reset Classification

Global Reset 不应仅凭一条模糊消息判断。

归类时应综合考虑：

- 来源
- 时间
- 是否存在多方一致信号
- 是否存在实际额度恢复证据
- 是否与历史模式一致
- 是否可能只是个人账户事件

具体实现可以随着数据量增加持续改进。

## Banked Reset Classification

Banked Reset、额外额度、Reset Card 等事件应与 Global Reset 分开。

目的不是定义厂商官方术语，而是让数据能够区分不同类型的额度事件。

## Deduplication

不同数据源可能重复描述同一个 Reset。

去重可以参考：

- 时间窗口
- 事件类型
- 来源
- 内容指纹
- 已有 event_id

目标是避免同一次 Reset 被重复计入历史。

## Verification

推荐的处理链路：

```text
Collect
  ↓
Normalize
  ↓
Classify
  ↓
Deduplicate
  ↓
Verify
  ↓
Publish
```

## Forecast

Forecast 可以使用历史 Reset 时间、Reset 间隔和公开 Signal，但需要满足两个原则：

1. 预测结果始终明确标记为 Forecast。
2. 预测不能被表述为官方 Reset 时间。

未来如果 Forecast 算法发生明显变化，应更新本页并保留 Git 历史。

## Data Correction Policy

如果发现历史数据错误：

1. 修正结构化数据。
2. 更新对应说明文档。
3. 使用清晰的 Git commit message。
4. 尽量保留修正依据。
5. 不静默篡改已经公开的重要历史结论。

## GitHub Sync

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

数据库是主要数据源，GitHub 是公开数据镜像。

只有业务数据发生真实变化时才生成 Commit，避免因为 `last_checked_at`、heartbeat 等字段制造大量无价值提交。

## 与官方信息的关系

Codex Reset Radar 是独立社区项目。

本项目的分类和 Forecast 是为了组织公开信息，不代表 OpenAI 官方定义或官方 Reset Schedule。

---

**相关文档**

- [Data Sources](./data-sources.md)
- [Codex Reset History](./codex-reset-history.md)
- [Codex Reset Forecast](./reset-forecast.md)
