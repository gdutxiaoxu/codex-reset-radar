# Open Data JSON 快照

> Codex Reset Radar 公开 JSON 快照的文件、字段边界、时效与兼容规则。

[← 返回项目首页](../README.md)

## 定位与时效

[`data/`](../data/) 中的 JSON 是随 Git 提交发布的版本化数据快照。它们是供引用、分析和构建客户端使用的公开数据镜像：

- 不是实时 API；实时状态请查看 [Codex Reset Radar](https://codex-reset.aiplanwatch.com/)。
- 不承诺固定刷新频率；应以文件内的 `generated_at` 和所在 Git 提交判断时效。
- 不代表 OpenAI 官方状态、额度或 Reset 时间。
- Forecast 是参考预测，不是官方 Reset Schedule。

当前仓库没有公开的自动同步工作流。只有业务数据出现变化时，快照才应产生新的 Git 提交，避免仅因检查时间变化制造无意义更新。

## 公共约定

每个 JSON 文件都包含：

- `schema_version`：当前数据结构版本。消费者应读取其支持的版本，并忽略未知字段，以便兼容新增字段。
- `generated_at`：ISO 8601 UTC 时间，表示本快照生成时间，不是所有事件发生时间。

事件时间、信号记录时间与预测时间窗口各自保留在对应对象中；消费者不得将 `generated_at` 当成 Reset 发生时间。字段缺失、`null` 或空数组表示该文件在当前快照中没有可公开提供的对应值，不能据此推断事件不存在。

## 文件

### [`latest.json`](../data/latest.json)

当前概要，包含：

- `product` 与 `monitoring_state`；
- `today`：UTC 当日是否记录到新的 Global Reset；
- `last_global_reset`：最近已记录的 Global Reset，以及可用时的来源；
- `latest_signal`：最近公开信号，以及可用时的来源；
- `forecast`：Forecast 的可用性和概要。

它适合轻量状态展示，但不能替代完整事件或信号历史。

### [`resets.json`](../data/resets.json)

`events` 数组提供已公开的 Reset 历史。Global Reset 与 Banked Reset 是不同类型，消费者应保留其事件类型、记录状态、发生时间及来源信息，而不应仅按日期合并统计。

### [`signals.json`](../data/signals.json)

`signals` 数组提供公开 Reset 信号。信号是发现和判断依据，不自动证明 Reset 已完成；有关分类与验证规则见 [Methodology](./methodology.md)。

### [`forecast.json`](../data/forecast.json)

Forecast 快照包含 `status`、`mode`、`horizons`、`watch`、`sample` 和 `disclaimer`。当 `status` 或 `mode` 表示不可用时，客户端应显示“暂无可公开展示的 Forecast”，而不是计算、插值或猜测概率。

## 使用与修正

- 展示数据时，保留来源链接和本项目的非官方免责声明。
- 将 Verified Reset、Public Signal 与 Forecast 分开呈现；不要把任一项包装为官方时间表。
- 引用时建议同时记录 Git commit、文件路径和 `generated_at`，以确保结果可复现。
- 发现来源、时间、分类或去重错误时，可通过 GitHub Issue 或 Pull Request 提供可公开验证的依据；修正规则见 [Data Sources](./data-sources.md) 与 [Methodology](./methodology.md)。
