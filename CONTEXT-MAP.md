# demo2027 — 项目集 Context Map

> 本仓是 demo2027 **项目集(Program)的协调 home(L1)**。它不装任何黑盒的内部,只画**边界**:跨黑盒契约、本张地图、程序级 ADR。三层模型见 EKStation `docs/adr/0005`。

## 项目集 = 三个黑盒(各自独立仓 / bounded context)

| 黑盒 | 仓短名 | 边界职责(对外可见的那一面) |
|---|---|---|
| **harness** | `harness` | 座舱 / CID 决策胶囊;对 figurine 暴露「默认 VPA 形象槽」(orb)。其余内部职责 → 去 harness 仓 grill |
| **scenario** | `scenario` | 🚧 边界职责待大总工补(只填对外可见部分) |
| **figurine** | `figurine-poc-phase1` | VPA 个性化形象;将来替换 harness 的 orb 槽 |

> 仓地址以 EKStation **项目集注册表**(`ops/agents.conf`)为准。
> 黑盒**内部**的 spec / 决策**不在这**——去各自仓 grill。这里只画边界。

## 契约清单(边界层)

详见 [`contracts/`](contracts/)。规矩:一契约一文件;**producer 起草、大总工独占改权、consumer 只读引用绝不拷贝**。

| 契约 | producer | consumer | 状态 |
|---|---|---|---|
| [figurine ↔ harness VPA 形象槽](contracts/figurine-harness-vpa-seam.md) | harness | figurine | 🚧 待从 harness `CONTEXT`+ADR0070 / figurine 迁入 |

## 怎么改契约

A 要 B 改契约 → 在**本仓**开「契约变更请求」issue/PR → 大总工整理 + 起草 → **owner 裁决** → 两边项目总工各自在黑盒内跟进。跨黑盒沟通只走「契约变更」这一种事件,谁都不碰对方内部。
