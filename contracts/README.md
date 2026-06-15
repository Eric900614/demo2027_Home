# contracts/ — 跨黑盒契约

每个契约一个文件。规矩(见 EKStation `docs/adr/0005`):

- **producer 起草**(拥有契约的那一侧)。
- **大总工独占改权**,owner 拍板。
- **consumer 只读引用,绝不拷贝**(拷贝 = 漂移)。
- 改契约走本仓 issue/PR:「契约变更请求」。

现有契约见 [CONTEXT-MAP 的契约清单](../CONTEXT-MAP.md#契约清单边界层)。
