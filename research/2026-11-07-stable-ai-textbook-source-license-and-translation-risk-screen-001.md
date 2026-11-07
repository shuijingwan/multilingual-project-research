# AI 稳定型开放教材：来源授权与多语言替代风险初筛 001

核实日期：2026-11-07  
阶段：`STABLE_AI_TEXTBOOK_SOURCE_LICENSE_AND_TRANSLATION_RISK_SCREEN`  
主项目：go-dev v2（不变）  
第二正式方向：`WORLD_HISTORY / SELECTED_NOT_LAUNCHED`  
新 AI 正式项目：`NO`  
状态：`RESEARCH_ONLY`

## 一、研究背景与方法

前驱：`research/2026-11-07-nvidia-guardrails-doc-license-and-locale-gap-pilot-001.md`。Ragas 和 NeMo Guardrails 等快速变化的开发框架在当前证据下没有明确的独立多语言广告网站机会。本轮刻意转向具有长期基础知识价值的**具体书籍/系统教材**，而非按“AI 很热门”推断自然流量。

先过来源和商业翻译授权，再过同源有效翻译竞争、来源变化、独立内容增量、可达自然搜索。语言菜单、GitHub Star、公开 PDF 或免费访问**不是**商业再分发许可证证明。本轮不做 66 locale 全量排查、SEO 流量预测或翻译实施。

## 二、七个具体来源的初筛

| 来源 | 权利一手证据 | 内容与翻译竞争 | 决策 |
| --- | --- | --- | --- |
| UC Berkeley CS188 *Introduction to Artificial Intelligence* | `BerkeleyAI/textbook/index.md` 本文明确 CC BY-SA 4.0；源仓库公开 Markdown | 搜索、CSP、逻辑、MDP、RL、ML 等较完整的基础内容；本轮只确认英文源，没有逐语言验证完整同源译本；英文大学官方站直接竞争 | `PRIORITY_SOURCE_SPECIFIC_PILOT` |
| *AI Safety Atlas* | `markov-root/atlas/LICENSE` 明确**软件 MIT、教材正文 CC BY-SA 4.0**；官网同样注明 CC BY-SA，例外材料另审 | 8章40+小节，AI 安全、治理和对齐；官方 `TRANSLATING.md` 已规定八章的 Google Docs 翻译、独立复核与官方多语言发布，构成明确的未来官方补齐风险；官网称每季度更新 | `RETAINED / OFFICIAL_EXPANSION_RISK / MAINTENANCE` |
| Stas Bekman *Machine Learning Engineering Open Book* | `stas00/ml-engineering/LICENSE-CC-BY-SA` 与 README 声明 CC BY-SA 4.0 | 7大部分覆盖 GPU、训练、推理、并行、调试等；专业价值较明确，但驱动、硬件、训练栈变化快；未核实各语言完整同源竞争 | `RETAINED / UPDATE_SENSITIVE` |
| Martin Frické *Artificial Intelligence and Librarianship: Notes for Teaching* | 作者/出版方 SoftOption 原始出版页明确 CC BY 4.0，可商业改编翻译；提供 2024 第三版 PDF 和 DOCX | AI 与图书馆交叉学科教材，目标用户更窄；有系统性正文，但真实目标语言搜索规模未知，内容中部分现代 AI 技术也持续变化 | `RETAINED / NICHE_DEMAND_UNKNOWN` |
| *Dive into Deep Learning* (D2L) | `d2l-ai/d2l-en` 授权摘要：正文 CC BY-SA 4.0，示例代码为修改的 MIT 许可；需逐组件遵循 | 官方已建立 zh/vi/ko 等真实仓库和多语言教学体系；存在实质同源竞争、更新和代码演进 | `LOW_PRIORITY / SOURCE_TRANSLATION_COMPETITION` |
| *Machine Learning Systems* (MLSysBook) | 原出版官网 `/about/license.html` 明确教材、实验等 CC BY-NC-SA 4.0（而 TinyTorch MIT，MLSys·im Apache2，StaffML AGPLv3） | 教材可免费读**不等于**可以用于带广告的商业翻译网站；不能把工具代码许可套用到教材 | `COMMERCIAL_TEXTBOOK_TRANSLATION_INELIGIBLE`；后续只可研究单独获授权或不同组件 |
| *Artificial Intelligence: Foundations of Computational Agents* (第三版) | 作者/出版方正文网页标 `CC BY-NC-ND 4.0`，禁止无额外许可的商业翻译改编；可免费阅读不改变此结论 | 权威体系化教材，但缺少所需商业译本授权 | `COMMERCIAL_TRANSLATION_INELIGIBLE` |

## 三、进一步得到的关键证据

### 3.1 Berkeley CS188（下轮优先）

- 课程教材首页：https://inst.eecs.berkeley.edu/~cs188/textbook/
- 原始源：https://github.com/BerkeleyAI/textbook/blob/main/index.md
- 原始仓库：https://github.com/BerkeleyAI/textbook
- 英文源存在可定位文件，例如 `search/uninformed.md`、`search/informed.md`、`mdp/markov-decision-processes.md`、`rl/rl.md`。适合做小范围的章节对照，不需构建整站。
- 作者注记截至 Summer 2025 仍持续维护并自动重新生成 PDF：不能无期限假设版本不变。
- **本轮没有证明** zh-CN、ja-JP、de-DE、es-ES、id-ID 中某门语言缺少完整同源译本。GitHub 名称搜索结果不足以证明不存在；真实同任务竞争（各种 CS188 讲义、算法课程）也未做系统查证。
- 课程另有作业、练习、Pacman 游戏代码与第三方图片。教材 CC BY-SA 不自动覆盖独立课件、官方测验、作业项目/图片；严格只对已确认的源码正文讨论。

### 3.2 AI Safety Atlas（官方多语替代风险）

- 官网：https://ai-safety-atlas.com/
- 原始源码：https://github.com/markov-root/atlas
- 内容明确 CC BY-SA / 代码 MIT：https://github.com/markov-root/atlas/blob/main/LICENSE
- 官方翻译流程：https://github.com/markov-root/atlas/blob/main/TRANSLATING.md
- 官方邀请译者，要求独立第二人审核、词汇表以及八章 Google Docs 双标签；批准后发布在官方 `/{lang}/chapters/v1/...`，并为翻译版本提供站内搜索。**这证明官方翻译扩张机制存在，不证明已有多少 locale 全部完成。**
- 官网声称季度更新。这种源文质量及事实时效维护成本与稳定理论教材不同；不能以 Open Source 等同低维护。

### 3.3 其他四个来源的版权停止线

- Stas 原文：https://github.com/stas00/ml-engineering 与 https://github.com/stas00/ml-engineering/blob/master/LICENSE-CC-BY-SA
- AI 图书馆学作者出版页：https://softoption.us/AIandLibrarianship
- D2L 开源仓库：https://github.com/d2l-ai/d2l-en；跨语言仓库 https://github.com/d2l-ai
- MLSysBook 来源与组件许可证：https://mlsysbook.ai/about/license.html
- ArtInt 3e 来源：https://artint.info/3e/html/ArtInt3e.html

`VERIFIED` 只表示上述明确的来源/许可证和在仓库或原始出版页可观察到的内容。其余外部素材、搜索流量、潜在用户、RPM和有效完整多语言覆盖继续为 `UNKNOWN` 或 `UNCLEAR`。

## 四、为什么选择下一轮聚焦 Berkeley，而不是直接立项

Berkeley CS188 相比 AI Safety Atlas（官方准备本地化）、Stas（快速工程变化）、MLSysBook 和 ArtInt（商业许可不适合），更符合以下待验证假设：基础内容相对稳定、可用 CC BY-SA 改编、按 Markdown 单元翻译及审校成本可控。

但**尚未证明**该教材在五样本语言中存在有价值的同源缺口，也没有证据表明搜索引擎会将独立译站排在现有本地课程、翻译教程和大学站前面。此为**进一步调查顺序**而非商业价值排名或选型批准。

下轮唯一门槛：`BERKELEY_CS188_SOURCE_EQUIVALENT_LOCALE_AND_SEARCH_PILOT`。
1. 冻结一个确切 source commit 和 3—5 个基础章节原文；盘点内容图片/外部资产许可证。
2. 对 zh-CN、ja-JP、de-DE、es-ES、id-ID 逐项对照该教材具体文章是否已有完整同源正式/非正式译本，并单独记录同任务搜索竞争。
3. 只挑 2—3 个有可识别搜索任务的主题，获取可重复的搜索结果样本；若没有可信搜索需求/独立增量，则不继续加大成本。
4. 发现权利、官方替代或已有高质量本地课程阻碍时，明确 PAUSE；不得将 NOT_FOUND_IN_SAMPLE 当作 VERIFIED_GAP。

不要求准确 RPM 预测，但要避免把理论学习价值直接当广告净收益。暂不翻译、不部署、不改动 go-dev、不新增 AI 正式项目。

## 五、结果

`RESULT=PASS`  
`STAGE=STABLE_AI_TEXTBOOK_SOURCE_LICENSE_AND_TRANSLATION_RISK_SCREEN`  
`SCREENED=7`  
`COMMERCIAL_TEXTBOOK_REUSE_POSITIVE_SOURCES=BERKELEY_CS188,AI_SAFETY_ATLAS,STAS_ML_ENGINEERING,AI_LIBRARIANSHIP,D2L`  
`INELIGIBLE_OR_EXTRA_PERMISSION_REQUIRED=MLSYSBOOK_TEXTBOOK,ARTINT_3E_TEXT`  
`AI_SAFETY_ATLAS_OFFICIAL_TRANSLATION_PIPELINE=VERIFIED`  
`BERKELEY_FULL_LOCALE_COMPETITION=UNKNOWN`  
`SEARCH_VOLUME=UNKNOWN`  
`ORGANIC_TRAFFIC=UNKNOWN`  
`AD_PAGE_RPM=UNKNOWN`  
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`  
`FORMAL_AI_PROJECT_SELECTED=NO`  
`SECOND_PROJECT=WORLD_HISTORY`  
`RESEARCH_ONLY=YES`  
`NEXT=BERKELEY_CS188_SOURCE_EQUIVALENT_LOCALE_AND_SEARCH_PILOT`
