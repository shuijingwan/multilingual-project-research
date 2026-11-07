# AI 教育与应用开发：六方向初筛

核实日期：2026-11-07  
阶段：AI_EDUCATION_SIX_SEGMENT_INITIAL_SCREEN  
状态：`RESEARCH_ONLY`  
性质：小范围来源及竞争供给初筛，**不是市场规模验证或新项目选型**  
目标：长期自然搜索、实际用户价值、合法广告净收益和可维护性

## 一、为什么拆分

“AI 教程”并非同质市场。面向普通用户的产品操作、普通开发者应用开发、Agent 工程及模型训练，用户群、搜索意图、竞争来源、授权和更新频率不同。尤其不应预设“普通开发者中间层一定比大众教程竞争小”：需要按具体关键词、来源和 locale 实测。

此前已有 Microsoft Generative AI for Beginners 的 MIT 仓库及多语言供给调查：`research/2026-11-03-cross-domain-commercial-evidence-001.md`。本报告只补充新的候选分层和代表性竞争，不覆盖原报告，更不改变 `WORLD_HISTORY` 已选决定。

## 二、六个方向（非商业排名）

| 编号 | 方向 | 典型读者任务 | 初步供给/判断 | 决策 |
| --- | --- | --- | --- | --- |
| A | 大众 AI 产品使用 | ChatGPT 入门、功能、普通人学习 | OpenAI Academy 已有系统学习资料；强供给存在，竞争强度数值 UNKNOWN | 暂不深挖 |
| B | AI 辅助工作与自动化 | 文档、表格、日常工作流 | 细分任务可能有价值；来源覆盖/自然搜索 UNKNOWN | 保留研究 |
| C | 普通开发者 AI 应用开发 | API 集成、RAG、应用构建 | Microsoft Generative AI for Beginners、OpenAI AI App Development 课程已存在 | 重点初筛 |
| D | AI Agent 开发 | 工具调用、编排、Agent 项目 | Microsoft、Hugging Face、OpenAI 均有连续课程；部分具多语言内容 | 重点初筛，但不假设低竞争 |
| E | AI 工程可靠性 | Agent 评估、测试、观测、安全、费用控制 | 现有课程已涉及评估/安全，但真实任务缺口仍未知 | 重点验证差异化 |
| F | 模型原理与训练 | 机器学习、微调、推理原理 | Dive into Deep Learning 和 Google ML Crash Course 等成熟来源已存在 | 暂不优先 |

以上“重点”仅代表下一步证据优先级，**不代表搜索需求、收入或可获取流量排名**。

## 三、已核实的代表性来源（2026-11-07）

1. **Microsoft AI Agents for Beginners**：提供覆盖 Agent 基础、工具、RAG、框架、部署与安全的章节目录，仓库根 LICENSE 为 MIT，README 列出大量翻译语言；`translations/zh-CN/README.md` 已存在并声明使用 Co-op Translator 维护。**实际各语言的全文完整性、质量、时效仍为 UNKNOWN**。  
   https://github.com/microsoft/ai-agents-for-beginners  
   https://github.com/microsoft/ai-agents-for-beginners/blob/main/translations/zh-CN/README.md  
   https://github.com/microsoft/ai-agents-for-beginners/blob/main/LICENSE
2. **Microsoft Generative AI for Beginners**：仓库根许可证为 MIT，面向开发者提供连续课程，已有多语供给；原报告已有此来源，继续沿用，不重复推断各 locale 完整。  
   https://github.com/microsoft/generative-ai-for-beginners
3. **Microsoft MCP for Beginners**：存在面向开发者的 MCP 课程，涵盖多种编程语言；根 LICENSE 为 MIT。  
   https://github.com/microsoft/mcp-for-beginners
4. **Hugging Face Agents Course**：有基础、smolagents、LlamaIndex、LangGraph、Agentic RAG、最终项目及评估等课程；已找到简体中文具体教学正文；GitHub 仓库根许可证为 Apache-2.0，**不能直接扩展到第三方图像、模型和外链素材**。  
   https://huggingface.co/learn/agents-course/en/unit1/introduction  
   https://huggingface.co/learn/agents-course/zh-CN/unit1/introduction  
   https://github.com/huggingface/agents-course/blob/main/LICENSE
5. **OpenAI Developers：Building Agents**：明确的初学者学习路线，覆盖核心概念、工具、编排、应用实例与 guardrails，证实官方已提供系统学习内容；本次**未核实**整套课程转载及商业翻译许可。  
   https://developers.openai.com/tracks/building-agents
6. **Google ADK**：官方已提供用 AI 辅助开发 Agent 的步骤和入门教程；其网站课程版权与开源 ADK 代码许可需分别调查。  
   https://google.github.io/adk-docs/tutorials/coding-with-ai/
7. **Google Search**：大量未经增值的翻译/自动生成页面可能属于规模化内容滥用，不能以许可证和语言数量直接推出可获得自然搜索流量。  
   https://developers.google.com/search/docs/essentials/spam-policies

## 四、商业与授权状态

- `VERIFIED`：各方向均存在可定位的真实学习资源；C/D/E 并非无竞争市场；Microsoft 与 Hugging Face 示例仓库均有清晰的**仓库根许可证**。
- `UNCLEAR`：具体课程页面、第三方图片/视频、示例数据、模型及平台条款能否整体商业翻译及独立广告托管。开源仓库与官网服务条款不互相推导。
- `UNKNOWN`：六方向的搜索量、搜索竞争强度对比、独立站可获得的点击、66 locale 的**有效全文**供给缺口、不同来源维护频率、RPM 和长期广告净收益。
- `ESTIMATE`：依赖快速变化的 SDK、模型名称、收费与第三方服务接口的实操教程，可能比稳定历史教材需要更频繁验证；具体成本未实测。

## 五、后续最值得做的一个小型验证

只围绕 **C（AI 应用开发）、D（Agent 开发）、E（可靠性与评估）** 做同口径样本。对每个方向先取一个明确的用户任务，检查 `zh-CN`、`ja-JP`、`de-DE`、`es-ES`、`id-ID` 的**来源级完整性、内容质量与更新频率**，再抽样核实搜索意图和现有第三方排名页面。

停止线：先判定是否存在真实独立内容增量；如果主要原始资料已经在目标 locale 有完整、持续维护的高质量翻译，或所需商业权利不清，降低优先级。不要扩展到全 66 locale、不要批量翻译、不要启动生产网站。

`AI_EDUCATION_RESEARCH=CONTINUE_LIGHTWEIGHT`  
`PREFERRED_PILOT=C_D_E_TASK_SPECIFIC`  
`SEARCH_VOLUME=UNKNOWN`  
`ORGANIC_TRAFFIC=UNKNOWN`  
`AD_PAGE_RPM=UNKNOWN`  
`COMMERCIAL_RANKING=NOT_READY`  
`SECOND_PROJECT=WORLD_HISTORY`  
`SECOND_PROJECT_SELECTION=UNCHANGED`  
`GO_DEV_V2_PRIORITY=UNCHANGED`  
`IMPLEMENTATION_AUTHORIZED=NO`  
`RESEARCH_ONLY=YES`


## 七、2026-11-07 后续供给试点补充

新增方向 **G：AI Security & Governance（AI 应用安全与治理）**。新增理由：OWASP GenAI LLM Top 10 2026 有权威专家来源、明确 CC BY-SA 4.0 商业改编许可、10 个风险类别，并有首 48 小时下载超过 10,000 次的公开关注信号；但独立网站的搜索流量、广告收益和官方翻译缺口仍未证明。

本轮结论：
- C 普通开发者 AI 应用入门：Microsoft Generative AI for Beginners 已有 21 课、50+ 翻译语言。五个 locale 的文件路径样本完整，但 RAG lesson 的 source hash 样本已 stale。泛化入门方向暂停深挖。
- D AI Agent 入门：Microsoft AI Agents for Beginners 已有 18 课、50+ 翻译语言；Hugging Face Agents Course 有 7 个语言目录，部分译文路径不完整。泛化 Agent 入门暂停深挖，保留框架进阶和可靠性缺口。
- MCP 作为 C/D 子主题已有 Microsoft MIT 课程及 50+ 语言，且协议更新较快；不视为低竞争空白。
- E LLM Evaluation / Observability：Evidently、DeepLearning.AI、LangChain Academy 等已有完整课程；中文搜索也已出现 Hugging Face、DataCamp、MongoDB 等内容。保留继续研究，但必须先验证开放源质量与搜索需求。
- G AI Security & Governance：OWASP 2026 LLM Top 10 的 CC BY-SA 4.0 授权明确，当前 canonical 仓库未见翻译目录；官方翻译 pipeline 已启动，但 registry 当前登记的是 Agentic Top 10，不是 LLM Top 10。是否存在其他 2026 译文仍 UNKNOWN。

详细证据及文件级检查见：[AI 开发者课程多语言供给与增量价值试点 001](../research/2026-11-07-ai-developer-course-locale-supply-pilot-001.md)。

当前不做 AI 项目选型；C/D 泛化课程暂停深挖，E/G 继续研究。搜索量、自然流量、RPM 和广告净收益均为 UNKNOWN。
