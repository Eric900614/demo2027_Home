# 契约:figurine ↔ harness — VPA 形象槽(VPA seam)

> 🚧 **骨架占位 / 待迁入。** 此契约的真相目前仍散在 **harness `CONTEXT.md` + ADR 0070** 与 figurine 仓。本文件是它在项目集 home 的**发布位**;内容待大总工从源头收拢、owner 拍定后转正。

- **producer**:harness —— 座舱 / CID 决策胶囊里提供一个「默认 VPA 形象槽」(当前 = 星云粒子 orb)。
- **consumer**:figurine —— 个性化形象,将来替换 orb、占据这个槽。
- **POC 现状**:只做静态 orb;figurine 个性化形象是后续。

## 迁移待办

1. 把 harness ADR0070 + figurine 侧对这个槽的接口约定,收拢成**一份已发布契约**(槽的形状 / 数据 / 替换时机)。
2. consumer(figurine)改为**引用本文件**,不再各自仓里拷贝一份。
3. 转正后删掉本警示块。
