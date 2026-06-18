# demo2027_Home

**demo2027 项目集(Program)的协调 home —— 三层架构里的 L1。**

- **是什么**:demo2027(harness + scenario + figurine 三个黑盒)的**协调层**。只装跨黑盒**契约**、[context-map](CONTEXT-MAP.md)、程序级 ADR,与大总工([CLAUDE.md](CLAUDE.md))。
- **不是什么**:不装任何黑盒的内部实现(那在各自仓 / L2),不装编排工作流(那在 EKStation / L0)。
- **为什么这么分层**:协作模型见 EKStation `docs/adr/0005-collaboration-3layer-multi-orchestrator.md`。

## 结构

| 路径 | 装什么 |
|---|---|
| [`CONTEXT-MAP.md`](CONTEXT-MAP.md) | 项目集边界地图 + 契约清单 |
| [`contracts/`](contracts/) | 跨黑盒契约(一契约一文件) |
| [`docs/adr/`](docs/adr/) | 程序级(跨黑盒)架构决策 |
| [`CLAUDE.md`](CLAUDE.md) | 大总工会话指令(= 大总工的冷启动 prompt) |

## 总工 prompt 落点约定

总工的会话冷启动 prompt **跟着它治理的边界走**,不集中堆放:

| 层 | 总工 | prompt 落点 |
|---|---|---|
| L1 项目集 | 大总工(本协调层) | 本仓 [`CLAUDE.md`](CLAUDE.md) |
| L2 黑盒 | 各黑盒项目总工 | **该黑盒仓**自己的 `docs/agents/orchestrator-kickoff.md` |

- **为什么不集中**:prompt 引用的深度文档(CONTEXT-MAP / context / ADR)都在各自仓里;prompt 与其引用就近 = 不漂移。大总工治协调层就住 home、项目总工治某黑盒就住该黑盒仓,对称。
- **现状**:harness 已落地(`docs/agents/orchestrator-kickoff.md`);scenario / figurine 照此模板补。
- 角色契约与分层源头见 EKStation `docs/adr/0005-collaboration-3layer-multi-orchestrator.md`。
