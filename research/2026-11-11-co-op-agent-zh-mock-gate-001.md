# Co-op Translator 中文模拟翻译验证 001

日期：2026-11-11

## 实验结果

- 阶段：CO_OP_AGENT_ZH_MOCK_TRANSLATION_GATE
- Co-op Translator：0.24.0
- 结果：PASS
- 分块数量：2
- 模型 API 调用：0
- Codex 调用：0

## 测试范围

使用自编历史 Markdown 样本。

通过固定字符串替换模拟英文到简体中文的翻译。

验证：
- 中文标题与正文还原
- Markdown 链接文字翻译与 URL 保留
- 行内代码与代码块保留
- 脚注标记保留
- Frontmatter 元数据保留
- 原始英文标题替换

## 证据

- SOURCE_SHA256=b252430fc7ad5e21ded59a5f37437091648e1c1b183e28a523d8660b9680fcf0
- TRANSLATED_SHA256=02096594af9caf528ec5307cd49f333755609e9e1fb684c0c7d087376ab12f5c
- EVIDENCE=/tmp/mpr-coop-zh-mock-lHXrTs

## 局限

本实验不验证：
- 真实 AI 翻译质量
- 历史知识准确性
- 66 locale 全量支持
- 人工审核译文的增量保留
- PDF/XML/EPUB 正文提取

本轮未启动世界历史正式翻译，
未修改 go-dev，未 Fork Co-op Translator。

## 来源

https://github.com/Azure/co-op-translator/blob/main/docs/api.md

RESULT=PASS
STAGE=CO_OP_AGENT_ZH_MOCK_TRANSLATION_GATE
RESEARCH_ONLY=YES
IMPLEMENTATION_AUTHORIZED=NO
