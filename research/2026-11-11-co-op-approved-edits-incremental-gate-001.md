# Co-op Translator 人工修订保留与增量翻译验证 001

日期：2026-11-11

## 实验结果

- STAGE=CO_OP_APPROVED_EDITS_INCREMENTAL_GATE
- RESULT=PASS
- Co-op Translator=0.24.0
- PRESERVED_BLOCKS=2
- TRANSLATED_BLOCKS=1
- MODEL_API_CALLS=0
- CODEX_CALLS=0

## 验证内容

通过 Co-op Translator 的实际增量翻译管理器
及模拟 TranslationStateProvider 验证：

1. 保留未变化段落中的人工校订。
2. 仅重新翻译发生变化的英文段落。
3. 增量翻译候选被记录。
4. 已批准的原文和译文基线不自动更新。

本次使用内部 TranslationManager 作为无模型
测试入口；正式集成应优先使用公开 Python API。

## 研究局限

未验证真实模型翻译、跨进程持久化、
复杂章节调整、歧义回退或正式独立 QC。

未修改 go-dev，未启动历史项目正式翻译，
未 Fork，也未购买模型 API。

## 证据

EVIDENCE=/tmp/mpr-coop-incremental-VeVKXv

## 官方资料

https://github.com/Azure/co-op-translator/blob/main/docs/api.md

RESULT=PASS
STAGE=CO_OP_APPROVED_EDITS_INCREMENTAL_GATE
RESEARCH_ONLY=YES
IMPLEMENTATION_AUTHORIZED=NO
