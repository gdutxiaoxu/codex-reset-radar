# Codex Reset Radar 公开资料与快照：工程知识导航

核对日期：2026-09-21。基线 HEAD：`d57d5f1`；入口按当前工作树核对，不代表全部已提交或已发布。

## 职责与边界

负责对外说明、方法论与版本化 JSON 快照，并包含技能分发实现。它是独立外部仓库，不属于五个产品仓库的共享发布流程。快照生成和同步实现归 Collector 仓库；这里的数据不是实时 API。

开发规则见 `AGENTS.md`（本地待提交），产品介绍见 [仓库 README](../README.md)。工程知识由本仓库维护，不依赖外部知识库或软链。

## 任务路由

先查下表，再查 `docs/CODEMAP.md`（本地待提交） 对应行。验证列是定位入口，不代表已执行或覆盖完整验收；正式要求以 AGENTS.md 为准。

| 任务 | 最小专题 | 代码入口 | 测试或检查入口 |
| --- | --- | --- | --- |
| 快照字段与公开数据 | [docs/open-data.md](../docs/open-data.md) | [data/latest.json](../data/latest.json) | [data/forecast.json](../data/forecast.json) |
| 事实、信号与预测语义 | [docs/methodology.md](../docs/methodology.md) | [data/resets.json](../data/resets.json) | [data/signals.json](../data/signals.json) |
| 技能读取与数据校验 | `skills/codex-reset-radar-data/SKILL.md`（本地待提交） | `skills/codex-reset-radar-data/scripts/read-latest.mjs`（本地待提交） | `test/read-latest.test.mjs`（本地待提交） |
| 技能安装与打包 | [README.md](../README.md) | `bin/codex-reset-radar-skill.mjs`（本地待提交） | `test/install.test.mjs`（本地待提交） |

技能源码、安装入口、测试和 package.json 当前尚未提交。“本地待提交”路径仅适用于当前工作树，待实现独立提交后再补为链接。

## 检索与维护约定

1. 先按任务路由选专题，再检索代码地图的相关行，只读命中的专题小节和当前实现；不要一次加载全部文档。
2. 代码地图记录业务入口；使用 `rg` 或当前工程可用的语言服务查询定义、引用和调用者。索引缓存按仓库、worktree、revision 隔离，不提交缓存。
3. 当前行为以当前分支代码为准；预期行为同时核对权威契约和测试。冲突必须记录并处理，不能仅改文档掩盖实现差异。
4. 路径或符号变化更新代码地图；任务入口变化更新本导航；契约和业务流程变化更新对应专题。工程知识随代码在本仓库同一次变更中维护。
5. 历史方案和实施报告只提供背景。日期、状态或已发布能力必须再次核验，不从历史报告推断当前部署。
6. 新文档使用相对链接和稳定符号，标注核对日期；未核实内容明确标注。运行日志、密钥、生产环境值和真实用户数据不进入知识文档。
7. 文档自测至少检查链接目标、代码路径和符号、package.json 中的命令及 `git diff --check`；行为改动继续遵守根 AGENTS.md 的验证要求。
