# AI 开发者课程多语言供给与增量价值试点 001

核实日期：2026-11-07  
阶段：`AI_DEVELOPER_COURSE_LOCALE_SUPPLY_PILOT`  
范围：C 普通开发者 AI 应用开发、D AI Agent 开发、E AI 工程评估/可靠性；新增观察方向 G AI 安全与治理。  
状态：`RESEARCH_ONLY`  
本报告不是市场规模测算、商业排名或第二项目选型。

## 一、核心结论

1. **C 普通开发者 AI 应用开发**：Microsoft `Generative AI for Beginners` 已有 21 课、MIT 仓库许可和 50+ 多语言翻译。5 个语言目录的 Markdown 路径样本完整，但源哈希抽样发现 RAG 一课译文已过期。通用入门课程的内容供给竞争很强，不建议继续泛化扩张。
2. **D AI Agent 开发**：Microsoft `AI Agents for Beginners` 18 课、50+ 语言；Hugging Face Agents Course 74 个英文 MDX 页面、7 个语言目录，其中西班牙语/法语路径完整，中文接近完整，韩语/俄语/越南语明显不完整。D 方向并非完全没有 locale 缺口，但已有成熟课程与强竞争，必须具体到进阶主题，而非再做一套通用 Agent 入门。
3. **MCP 是 D/C 的子主题，不宜视为低竞争空白**：Microsoft MCP for Beginners 是 MIT 课程，README 列出 50+ 语言；课程已按 2026-07-28 规格更新。它说明该协议主题竞争和维护速度都很高。
4. **E LLM Evaluation / Observability**：有 Evidently、DeepLearning.AI、LangChain Academy、AI Evals Academy 等成熟免费或商业课程；中文搜索结果已经出现 Hugging Face、DataCamp、MongoDB 等教程。一个 9 模块、87 篇 Markdown/语言版本的双语开源课程提供 CC BY 4.0 正文许可，但来源质量、长期维护与用户需求仍未经验证。另一个新课程的内容许可文件与仓库标题不一致，不能确认授权。
5. **新增 G AI Security & Governance**：OWASP GenAI LLM Top 10 2026 有权威组织来源、CC BY-SA 4.0 明确商业适配许可、10 个风险类别、122 页 PDF；OWASP 公开称首 48 小时下载超过 10,000 次。活动源码仓库没有翻译目录；OWASP 新翻译 pipeline 当前 registry 只有 Agentic Top 10 资产，未登记 LLM Top 10 2026。但官方翻译体系正建设中，不能将当前未登记解释为长期空白。
6. 所有方向的**关键词搜索量、可获取自然流量、RPM 和广告净收益仍为 UNKNOWN**。课程免费、GitHub stars、下载数或语言数量均不能直接转换成广告收入。

## 二、C：普通开发者 AI 应用开发

### Microsoft Generative AI for Beginners

来源：https://github.com/microsoft/generative-ai-for-beginners

- `VERIFIED`：课程 README 为 21 lessons；GitHub 仓库根许可为 MIT。
- `VERIFIED`：当前仓库存在 55 个 `translations/<code>/` 目录。此数是目录代码数，不等于 55 个与目标 66 locale 完全对应的有效地区版本。
- `VERIFIED`：源课程样本有 31 个 Markdown lesson 路径；`zh-CN`、`ja`、`de`、`es`、`id` 五个目录各有 31/31 对应路径。
- `VERIFIED`：对四个源文件的 MD5 与 Co-op Translator metadata `original_hash` 抽样比较，Intro、AI Agents、Application Lifecycle 三页匹配；`15-rag-and-vector-databases/README.md` 不匹配，五个抽样 locale 均显示 stale source hash。故本次 4 页样本中 1 页过期，**不是全课程过期比例**。
- `VERIFIED`：该项目 README 说明多语言翻译由 Co-op Translator 维护。
- `UNKNOWN`：全 21 课语义质量、各 locale 地区表达、全部源哈希当前性和真实搜索流量。

### 66 locale 映射限制

55 个翻译目录混合了基础语言代码和地区代码，例如 `ja`、`de`、`es`、`fr`，而目标表使用 `ja-JP`、`de-DE`、`es-ES`、`fr-CA` 等。不能简单把 55/66 当作有效覆盖率。英语源语言地区变体也需要单独确认；本次未完成全部 66 locale 的地区适配核查。

初步判断：C 方向的通用课程内容供给很强。若继续调查，应寻找特定实用任务或质量缺口，而不是重建泛用生成式 AI 入门课程。

## 三、D：AI Agent 开发

### Microsoft AI Agents for Beginners

来源：https://github.com/microsoft/ai-agents-for-beginners

- `VERIFIED`：18 lessons，仓库根许可 MIT，README 列出 50+ 语言。
- `VERIFIED`：源课程样本有 43 个 Markdown lesson 路径；`zh-CN`、`ja`、`de`、`es`、`id` 五个目录各有 43/43 对应路径。
- `VERIFIED`：四个源文件 MD5 与五个 locale 的 metadata 抽样比较中，Intro、Agentic RAG、Production 三页匹配；`18-securing-ai-agents/README.md` 的当前源哈希与五个 locale metadata 均不匹配。故本次 4 页样本中 1 页过期，**不是全课程过期比例**。
- `VERIFIED`：安全页的 metadata 日期较新（部分 locale 为 2026-11-02），但源哈希仍不匹配，说明仅看翻译日期不能证明 currentness。

### Hugging Face Agents Course

来源：https://github.com/huggingface/agents-course

- `VERIFIED`：仓库根许可 Apache-2.0；英文课程有 74 个 MDX 文件。
- `VERIFIED`：当前有 7 个语言目录：`en`、`es`、`fr`、`ko`、`ru-RU`、`vi`、`zh-CN`。
- `VERIFIED`：按相对 MDX 路径与英文 74 文件比较：es 74/74、fr 74/74、ko 50/74、ru-RU 23/74、vi 23/74、zh-CN 70/74（另有 5 个额外路径，需进一步核查命名差异）。
- `VERIFIED`：课程含基础 Agent、smolagents、LangGraph、LlamaIndex、Agentic RAG，以及 bonus unit 中的 observability/evaluation 内容。
- `UNKNOWN`：路径存在不等于正文质量通过；本次未进行完整译文语义审核、逐文件源哈希核验和全部 66 locale 映射。

判断：Hugging Face 课程比 Microsoft 的通用入门课程更有框架深度，但仍已覆盖多个主要语言；它可能存在长尾 locale 增量，却不能据此推断搜索需求或商业收益。

### MCP 子主题

来源：https://github.com/microsoft/mcp-for-beginners

- `VERIFIED`：MIT 仓库；README 列出 50+ 语言翻译。
- `VERIFIED`：课程覆盖 MCP 基础、安全、客户端/服务器、多个编程语言示例、部署、测试与监控。
- `VERIFIED`：README 说明当前规格为 2026-07-28；英文 changelog 记载 2026-09-09 对 38 个英文文档文件进行规格对齐更新。
- `ESTIMATE`：协议和 SDK 变化速度较快，翻译同步与示例复测维护成本较高。
- `UNKNOWN`：本次未做 5 locale 文件路径和 hash 完整性抽样。

判断：MCP 是 AI 应用/Agent 开发的具体子主题，但已有大规模官方多语言课程，不宜把“缺少一套 MCP 入门翻译”作为项目机会。

## 四、E：LLM Evaluation / Observability / Reliability

### 已有课程与竞争供给

1. Evidently AI — LLM Evaluation for Builders：免费三周课程、10+ 视频教程和 Python 代码练习，涉及评估集、LLM Judge、RAG 评估、对抗测试和 Agent 评估。https://www.evidentlyai.com/llm-evaluation-course-practice
2. DeepLearning.AI — Evaluating AI Agents：15 个视频课程、6 个代码示例，涵盖 tracing、agent component evaluation、LLM-as-a-Judge 和生产监控。https://www.deeplearning.ai/courses/evaluating-ai-agents
3. LangChain Academy — Building Reliable Agents：Observation、Evaluation、Moving Towards Production 三个阶段，含 code-based eval、LLM-as-Judge、pairwise evaluation 和 online eval。https://academy.langchain.com/courses/building-reliable-agents
4. AI Evals Academy：页面列出 11 模块、41 lessons、35 个交互式 playground；课程内容再分发许可本次未核实。https://aievalsacademy.com/

以上课程可以作为竞争者并链接官方页面；**免费不等于允许翻译、转载或商业再分发**。没有找到明确内容许可的课程标记 `UNCLEAR`，不得直接翻译托管。

### 可能的开放内容来源：LLM Engineering Program

来源：https://github.com/jlcases/llm-engineering-program

- `VERIFIED`：`LICENSE.md` 明确规定教育 Markdown、图表、教育数据集和原创问题采用 CC BY 4.0；代码采用 MIT。
- `VERIFIED`：9 个模块，覆盖 LLM 基础、Prompt Engineering、RAG、Agents、Harness、Loops、Graphs、Production 和项目。
- `VERIFIED`：西班牙语正文 87 个 Markdown 文件；`translations/en` 有对应 87 个 Markdown 文件，路径集合一致。当前只发现西班牙语与英语两个内容版本。
- `VERIFIED`：仓库还包含 51 个 Python 文件；英文目录中有 39 个对应 Python 文件。未对全部代码逐一运行。
- `UNKNOWN`：课程教学正确性、独立专家审核、实际学习完成率、自然搜索需求、长期维护和其他 locale 的有效供给。
- `ESTIMATE`：该课程覆盖的主题较广，可能比单一 RAG/Agent 入门课程更有内容体量；但源作者及课程市场认可度尚未得到独立验证。

判断：这是目前 E 方向值得保留的一个 CC BY 4.0 内容候选，但不能因 2 个语言版本就认定它值得投入 64 个 locale；必须先完成质量、维护和需求核查。

### 授权不确定或内容未完成的来源

- TechNaom `llm-evaluation-for-everyone`：仓库有 `LICENSE-CONTENT`，但该文件把授权内容描述为另一个项目名 `Context Engineering for Everyone`，与仓库标题不一致，故内容许可标记 `UNCLEAR`。README 还说明 13 章中只有第 1 章上线。暂不作为翻译源。https://github.com/TechNaom/llm-evaluation-for-everyone
- `ai-engineering-curriculum/agentic-ai-engineer-learning`：根许可证 MIT，课程 README 描述 9 个模块、约 119 小时，但内容仍处于 AI-assisted / human review 过程，成熟度尚未验证。https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning

### 语言搜索竞争样本

本次中文搜索已找到：
- Hugging Face 中文 Cookbook：RAG 评估；
- DataCamp 中文：RAG 评估教程，2026-10-19 更新；
- MongoDB 中文文档：RAG 应用评估；
- 独立中文技术博客：生产级 RAG 评测。

这说明中文 E 子主题已有实际竞争，不是空白。日语、德语、西班牙语、印度尼西亚语的 SERP 尚未形成足够可靠的可比样本。

搜索量和可获得流量仍为 `UNKNOWN`。

## 五、新增 G：AI Security & Governance

### OWASP GenAI LLM Top 10 2026

来源：
- https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/
- https://github.com/GenAI-Security-Project/GenAI-LLM-Top10

- `VERIFIED`：2026 版于 2026-08-04 发布，包含 10 个风险类别和相关框架映射、架构/威胁建模附录。
- `VERIFIED`：官方 PDF 为 122 页；本次对 13 个主要 Markdown 文件抽取约 26,520 个英文词（包含较大的框架映射附录）。
- `VERIFIED`：2026 PDF 第 2 页明确 CC BY-SA 4.0；允许商业分享和改编，但必须署名、标明修改，并以相同许可发布改编作品。PDF 中第三方外链内容不因此获得再分发许可。
- `VERIFIED`：OWASP 2026-09-02 新闻稿称该版本发布后前 48 小时下载超过 10,000 次，GenAI Security Project 社区超过 30,000 名成员。这是关注度/下载信号，**不是搜索量或可获取网站流量**。
- `VERIFIED`：当前 canonical 2026 源仓库没有 locale translation 目录。
- `VERIFIED`：OWASP 新 `GenAI-Security-Project/translations` 仓库目前处于 Incubator；registry 中登记的是 Agentic Top 10 2026 资产，locale 为 de-DE、fa-IR、fr-FR、pl-PL、ru-RU；未登记 LLM Top 10 2026。README 说明该流程还缺少正式 approvers、真实 LLM secret 和旧文档迁移。
- `UNKNOWN`：LLM Top 10 2026 是否已在该 pipeline 之外产生其他语言版本；不能仅因 registry 未登记就断言全球不存在译文。
- `ESTIMATE`：10 个风险类别适合作为 AI 应用安全参考资料，但单独一份 Top 10 不足以支撑大型多语言内容网站；若扩展，需要分别核实 Agentic Top 10、GenAI Data Security、OWASP cheat sheets、MITRE ATLAS、NIST AI RMF 等来源的授权与更新边界。

新增理由：该方向有权威专家社区、一手公开内容、明确商业可改编许可和实际下载关注度，值得纳入 AI 研究；但官方自身已有多语言项目建设，且内容规模有限，暂不做项目选择。

## 六、比较结论与决策

| 方向 | 多语言供给 | 内容许可 | 当前判断 |
| --- | --- | --- | --- |
| C AI 应用入门 | Microsoft 55 个翻译目录，样本 5 locale 路径完整，出现源 hash stale | MIT | 泛化入门暂停深挖 |
| D Agent 入门 | Microsoft 55 目录；HF 7 语言，部分 locale 不完整 | MIT / Apache-2.0 | 不做通用 Agent 入门；可研究进阶缺口 |
| D MCP | Microsoft 50+ 语言 | MIT | 竞争强、更新快，暂缓 |
| E Evaluation / Observability | 课程来源较多；开放双语候选有限 | 多数课程 UNCLEAR；一个 CC BY 4.0 候选 | 保留，需验证质量和搜索需求 |
| G AI Security / Governance | 2026 LLM Top10 源仓库未见翻译目录；官方翻译 pipeline 已启动 | CC BY-SA 4.0 | 新增观察方向，需检查官方翻译进展和扩展内容源 |

**不作商业排名**：C/D 内容供给强并不等于广告价值低；E/G 内容缺口也不等于流量或 RPM 高。所有搜索量、自然流量、广告 RPM、广告净收益保持 `UNKNOWN`。

## 七、唯一下一步建议

开展一个 E 与 G 的**五 locale 搜索意图/竞争页面对比试点**，使用既定的 `zh-CN`、`ja-JP`、`de-DE`、`es-ES`、`id-ID`：
- E 只取两个任务：RAG Evaluation、Agent Evaluation。
- G 只取两个任务：LLM Security / Prompt Injection、OWASP GenAI LLM Top 10 2026。
- 记录每个 locale 的真实查询表达、SERP 前 10 个页面的官方/第三方来源、页面类型、内容深度、更新时间和可见的多语言覆盖。
- 搜索量仍需 Google Trends / Bing keyword data 另行验证；无数据时保持 UNKNOWN。
- 不做翻译、不建站、不部署，不改变 `WORLD_HISTORY` 已选状态和 `GO_DEV_V2_PRIORITY`。

`AI_DIRECTIONS=7`  
`C_STATUS=RESEARCH_PAUSE_GENERAL_COURSE`  
`D_STATUS=RESEARCH_PAUSE_GENERAL_COURSE`  
`E_STATUS=RESEARCH_CONTINUE`  
`G_STATUS=NEW_CANDIDATE_RESEARCH_CONTINUE`  
`SEARCH_VOLUME=UNKNOWN`  
`ORGANIC_TRAFFIC=UNKNOWN`  
`AD_RPM=UNKNOWN`  
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`  
`SECOND_PROJECT=WORLD_HISTORY`  
`FORMAL_AI_PROJECT_SELECTED=NO`  
`IMPLEMENTATION_AUTHORIZED=NO`  
`GO_DEV_MUTATION=NONE`  
`RESEARCH_ONLY=YES`
