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
| [`CLAUDE.md`](CLAUDE.md) | 大总工会话指令 |
