# AI 开放学习资料：三来源许可与同源竞争初筛 001

核实日期：2026-11-07  
阶段：`AI_OPEN_SOURCE_LEARNING_CORPUS_SCREEN`  
状态：`RESEARCH_ONLY`  
主项目：go-dev v2  
第二项目：`WORLD_HISTORY / SELECTED_NOT_LAUNCHED`  
新 AI 正式项目：`NO`

## 一、研究问题

Ragas 直接翻译缺少明确增量之后，不循环检索泛 RAG 文章，转为三项**明确可定位原始文档**的 AI 开源项目，检查来源、实际内容、多语言同源竞争及后续维护风险。该调查不是流量或收益排名，不因 GitHub Star、语言菜单或页面数量而直接立项。

## 二、来源与初步证据

| 源项目 | 具体原始内容 | 权利与边界 | 实际同源译文证据 | 本轮判断 |
| --- | --- | --- | --- | --- |
| Hugging Face Agents Course | `units/en/` 下的 Agent 基础、框架、Agentic RAG 和结业项目（README 列示 4 units + bonus） | 根 `LICENSE` 为 Apache 2.0；仓库之外的视频/图片/第三方素材另审 | `units/zh-CN/unit1/README.md` 有实质中文，`units/fr/unit1/README.md`、`units/es/unit1/README.md` 等真实存在 | `RETAINED_BUT_SOURCE_EQUIVALENT_COMPETITION_VERIFIED` |
| Hugging Face smol-course | `units/` 讲解指令微调、模型评估、偏好对齐、多模态和训练方法；README 声称 v2 已上线 | 根 `LICENSE` 为 Apache 2.0；模型权重、数据集、图片与 notebook 引用资源须按各自许可证处理 | `units/ja/unit1/2.md` 有完整日文正文，`units/es/unit1/1.md` 有西文正文（另发现 ko、vi、pt-br 路径） | `RETAINED_BUT_SOURCE_EQUIVALENT_COMPETITION_VERIFIED` |
| NVIDIA NeMo Guardrails | 仓库的 `docs/getting-started/`、`docs/configure-rails/` 等实际 MDX 源；Colang、RAG/Agent guardrails、安全与评测 | `pyproject.toml` 声明项目 `Apache-2.0`，README 同样声明；具体 `docs/` 是否存在额外条款或第三方资产尚未完整核查，暂标 `UNCLEAR` | 本轮未取得准确的指定 MDX 文件跨 locale **完整同源**翻译证据；这不是证明不存在 | `RESEARCH_CONTINUE / LICENSE_AND_COVERAGE_GATE` |

核实源（仓库文件本身）：
- https://github.com/huggingface/agents-course/blob/main/LICENSE
- https://github.com/huggingface/agents-course/blob/main/README.md
- https://github.com/huggingface/agents-course/blob/main/units/zh-CN/unit1/README.md
- https://github.com/huggingface/agents-course/blob/main/units/fr/unit1/README.md
- https://github.com/huggingface/agents-course/blob/main/units/es/unit1/README.md
- https://github.com/huggingface/smol-course/blob/main/LICENSE
- https://github.com/huggingface/smol-course/blob/main/README.md
- https://github.com/huggingface/smol-course/blob/main/units/ja/unit1/2.md
- https://github.com/huggingface/smol-course/blob/main/units/es/unit1/1.md
- https://github.com/NVIDIA-NeMo/Guardrails/blob/develop/README.md
- https://github.com/NVIDIA-NeMo/Guardrails/blob/develop/pyproject.toml
- https://github.com/NVIDIA-NeMo/Guardrails/blob/develop/docs/getting-started/installation-guide.mdx
- https://docs.nvidia.com/nemo/guardrails/latest/home

## 三、竞争、维护与商业解释

1. **Hugging Face Agents Course**：已有多种真实同源译文，继续增加译文语言可能仍有价值，但需要先证实某些具体 locale 的有效全章覆盖缺口。不得将首页可选语言直接当全课完成。框架更新及代理能力变化会增加更新审校。
2. **Hugging Face smol-course**：已有日/西文实际课程内容；内容更加专业，可能有稳定学习需求，但它是计算密集型训练/后训练课程，API、硬件门槛与下游库更新会削弱可独立获取的广告阅读流量。未进行任何实际市场流量验证。
3. **NVIDIA NeMo Guardrails**：源内容包括可独立使用的文档、配置、安全指南与参考，专业查询任务清楚；缺点是明确的厂商官方站竞争、版本变化、源站内容可能调整。其根项目 Apache2 声明不自动豁免外部版权与商标问题，须先核查具体 MDX 权利边界和本地化竞争。
4. **Microsoft AI Agents for Beginners**：作为参考竞品而非本轮重新深挖的来源。公开 README 显示其已由 Co-op Translator 维护数十种语言的课程译文；泛“Agent 入门教材”面临强同源/同任务竞争。
5. **市场/广告证据**：三个候选的可获取自然点击、搜索量、Page RPM、年度维护成本、长期广告净收益均为 `UNKNOWN`。不能把官方站有文档、课程有译文、GitHub 热度当作 SEO 或广告回报。

## 四、下一轮唯一研究门槛

仅对 **NeMo Guardrails** 做一次小范围 `NVIDIA_GUARDRAILS_DOC_LICENSE_AND_LOCALE_GAP_PILOT`：
- 在一个固定源版本下抽取 3—5 个用户任务明确的 MDX 页面（安装/Colang/rails/evaluation 等），核对每个文件的许可证和内嵌素材边界；
- 核实 zh-CN、ja-JP、de-DE、es-ES、id-ID 有无指定原文的官方/社区完整译本；将“未查到”标 `NOT_FOUND_IN_SAMPLE`，不是 `VERIFIED_ABSENT`；
- 对照 NVIDIA 官方网页及各语言主要同任务教程，说明站外用户价值与版本维护差异；
- 若现成官方/社区覆盖较多、文档权利不清或不存在明显内容增量，则 `PAUSE`，转其他候选，不继续扩大范围。

没有授权开展翻译、独立站开发、批量语言调查、模型 API 购买或 go-dev 主项目变更。

`RESULT=PASS`  
`STAGE=AI_OPEN_SOURCE_LEARNING_CORPUS_SCREEN`  
`SCREENED=3`  
`HF_AGENTS_SOURCE_EQUIVALENT_TRANSLATION=VERIFIED_SAMPLE`  
`HF_SMOL_SOURCE_EQUIVALENT_TRANSLATION=VERIFIED_SAMPLE`  
`NVIDIA_DOC_REUSE_RIGHTS=UNCLEAR_PENDING_FILE_SCOPE`  
`NVIDIA_TRANSLATION_COVERAGE=UNKNOWN`  
`SEARCH_VOLUME=UNKNOWN`  
`ORGANIC_TRAFFIC=UNKNOWN`  
`AD_PAGE_RPM=UNKNOWN`  
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`  
`FORMAL_AI_PROJECT_SELECTED=NO`  
`SECOND_PROJECT=WORLD_HISTORY`  
`RESEARCH_ONLY=YES`  
`NEXT=NVIDIA_GUARDRAILS_DOC_LICENSE_AND_LOCALE_GAP_PILOT`
