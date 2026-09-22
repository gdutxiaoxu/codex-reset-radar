# Codex Reset Radar 公开资料与快照：代码地图

核对日期：2026-09-21。基线 HEAD：`d57d5f1`；入口按当前工作树核对，不代表全部已提交或已发布。

本地图只覆盖主要业务入口，不是全量符号索引。先从 `docs/README.md`（本地待提交） 确定范围；下表路径相对仓库根目录，符号以当前分支为准。

| 能力 | 入口与检索符号 | 关联专题 | 回归入口 |
| --- | --- | --- | --- |
| 快照字段与公开数据 | [data/latest.json](../data/latest.json) | [docs/open-data.md](../docs/open-data.md) | [data/forecast.json](../data/forecast.json) |
| 事实、信号与预测语义 | [data/resets.json](../data/resets.json) | [docs/methodology.md](../docs/methodology.md) | [data/signals.json](../data/signals.json) |
| 技能读取与数据校验 | `skills/codex-reset-radar-data/scripts/read-latest.mjs`（本地待提交）：`validateSnapshot` | `skills/codex-reset-radar-data/SKILL.md`（本地待提交） | `test/read-latest.test.mjs`（本地待提交） |
| 技能安装与打包 | `bin/codex-reset-radar-skill.mjs`（本地待提交） | [README.md](../README.md) | `test/install.test.mjs`（本地待提交） |

## 本地实现状态

技能源码、安装入口、测试和 package.json 当前尚未提交。表中的“本地待提交”路径仅用于当前工作树定位，新克隆不能假定它们存在；待实现独立提交后再改为可跳转链接。

## 排查方法

1. 用任务关键词定位上表入口，再检查该文件的 imports、调用者与测试。
2. 页面问题沿页面、服务、接口定位；后台问题沿调用入口、路由或任务、存储定位。
3. 接口字段问题先核对权威契约，再检查转换和展示。日志或监控能力必须回查实现，不从文档假定存在。
4. 路径或符号改名时同步更新本表和任务导航；分支切换后重新核对。
