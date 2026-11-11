# Co-op Translator 外层候选隔离与批准提升验证 001

日期：2026-11-11

## 验证结果

- RESULT=PASS
- STAGE=CO_OP_CANDIDATE_PROMOTION_ISOLATION_PILOT
- RESEARCH_ONLY=YES
- CODEX_CALLS=0
- MODEL_API_CALLS=0

## 通过的检查

- candidate_isolated: PASS
- approval_required: PASS
- source_stale_rejected: PASS
- candidate_stale_rejected: PASS
- accepted_stale_rejected: PASS
- explicit_promotion: PASS

## 方案结论

外层使用三个明确的逻辑区域：

- Source：已验证的原始版本。
- Candidate：尚未审核通过的新译文。
- Accepted：已批准译文。

候选生成不得修改 Accepted。
提升时要求明确批准，并核对 Source、Candidate、
Accepted 三方版本哈希。

本实验仅验证 Python 标准库实现的轻量隔离契约。
不证明 Co-op Translator 已经集成此方案。

## 尚未验证

- Co-op Translator 指定候选输出目录后的端到端行为。
- 独立 Reviewer 与批准记录的真实持久化。
- 并发批准、崩溃恢复和正式生产部署。
- 历史教材与 66 locale 的完整生产流程。

本轮不修改 go-dev，不启动正式历史项目。

## 证据

EVIDENCE=/tmp/mpr-coop-promotion-t2ulUw
SOURCE_SHA256=d9fd904f68aa109d8a6940031dfd0bec9650a7b70f5b06b9e836010ce5cb1fe0
CANDIDATE_SHA256=38c38ba010700b2b1c4f02b0c6adb3596ed5ef1ca759d1652c8d8f56253aa8b8

IMPLEMENTATION_AUTHORIZED=NO
CO_OP_INTEGRATION=NOT_TESTED
NEXT=CO_OP_EXTERNAL_OUTPUT_ADAPTER_VALIDATION
