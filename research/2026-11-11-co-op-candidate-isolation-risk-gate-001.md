# Co-op Translator 候选译文隔离风险验证 001

核实日期：2026-11-11

## 结论

- RESULT=PASS
- STAGE=CO_OP_CANDIDATE_ISOLATION_RISK_GATE
- DEFAULT_TARGET_ISOLATION=FAIL
- RISK=UNREVIEWED_CANDIDATE_REPLACES_TARGET_FILE
- RESEARCH_ONLY=YES

## 已验证事实

1. 上轮实验保留了 2 个未变化 Markdown 块。
2. 仅对 1 个变化块执行模拟翻译。
3. 已批准基线对象未更新。
4. 磁盘上的目标 Markdown 文件已被新候选覆盖。
5. 官方管理器先写入译文，再记录候选。

因此，基线记录与目标文件隔离属于两个不同问题。

当前实验没有单独的、受到保护的正式发布目录。
不能据此认定 Co-op Translator 默认提供候选和已批准
译文之间的发布隔离。

## 推荐边界

未来世界历史项目应采用：

- Accepted：已批准译文，只允许明确的批准操作修改。
- Candidate：新生成译文，独立存放。
- Review：独立质量审核。
- Promotion：审核 PASS 且版本匹配后才允许提升候选。

优先通过外层目录、Git 或轻量状态记录实现。
不得预先建立 go-dev 的复杂授权状态机。

## 上轮证据

- Evidence：/tmp/mpr-coop-incremental-VeVKXv
- 目标译文 SHA256：bd80448264cef7846c23849571b80de16cab6e0f0eb71e41ad46b608f15371f9
- 保留块数：2
- 翻译块数：1
- 候选记录：YES
- 已批准基线对象未变化：YES

## 官方源码

https://raw.githubusercontent.com/Azure/co-op-translator/ae61ab7918ba6654352b45fad35cea2d42370e3b/src/co_op_translator/core/project/translation/project_markdown_translation.py

源代码 SHA256：
23176ad2b0cd44b78a0c42016fb4850d82ddfc5a067598b060f81730d90792fc

该源码引用固定 Git 提交；本轮未核实其与
PyPI 0.24.0 安装包所有内部代码逐字一致。
磁盘覆盖行为另有上轮本地实验直接支持。

## 研究边界

未执行正式翻译，未修改 go-dev。
未安装依赖，未调用模型，未 Fork。
未建设世界历史网站。

IMPLEMENTATION_AUTHORIZED=NO
CODEX_CALLS=0
MODEL_API_CALLS=0

NEXT=ISOLATED_CANDIDATE_PUBLICATION_BOUNDARY_DESIGN
