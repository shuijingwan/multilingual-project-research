# 全候选项目：社区译本仍重译规则下的内容增量复评 001

核实日期：2026-11-06
阶段：ALL_CANDIDATES_CONTENT_INCREMENTAL_VALUE_REASSESSMENT
状态：RESEARCH_ONLY
商业目标：长期合法广告净收益，同时重视真正的多语言知识可及性增量
固定范围：66 locales（广告支持62，不支持4；沿用既有清单）
主项目：go-dev v2
正式第二项目：NOT_DECIDED

## 一、本次明确修正的项目规则

负责人在2026-11-06进一步明确：

**一旦正式选定一个翻译项目，冻结的66个目标locale中，只排除对应源资料已被官方有效支持的语言；即使社区已经存在同一语言的完整译本，该语言仍原则上重新翻译。**

这与“逐个语言选择是否值得再翻译”不同。社区翻译的重复性只用于**立项前的整个项目比较**：

- 官方有效支持：界定计划翻译范围；需核实具体模块与内容范围。
- 社区完整/部分/过时译本：衡量项目级重复投入和知识可及性增量；**不得自动剔除locale**。
- 同主题不同源教程：衡量用户意图竞争，但**不是同源翻译重复**。
- 翻译后的独立审核、更新、整合导航与本地化可提高使用价值，但不能把这些潜在优势未经验证直接记作“独特内容”。
- 未发现译本（NOT_FOUND_IN_SAMPLE）不等于已证实无人翻译；已有官方语言入口不等于该模块具备完整有效译文。
- 首期分阶段交付可控制go-dev v2机会成本，但不擅自缩减选中项目的既定总语言计划。

`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`COMMUNITY_DUPLICATION_AFFECTS_PROJECT_SELECTION=YES`
`OFFICIAL_EFFECTIVE_SUPPORT_DEFINES_DEFAULT_EXCLUSION=YES`
`FULL_66_LOCALES_AUTOMATICALLY_AUTHORIZED=NO`

## 二、统一比较方法

本轮复评**所有已经记录的主要候选**，包括翻译型、混合型与工具型。比较六个维度：

1. **版权底线**：具体源文件是否允许商业翻译/改编/独立托管；第三方资产、商标、条款分开判断。
2. **官方有效覆盖**：66个目标locale中，拟翻译的具体内容是否已有官方可用译文；UNKNOWN绝不计算为“需要翻译的确定数量”。
3. **社区同源重复程度**：是否有真实正文、练习和版本证据；官方译本与社区译本不能混算。
4. **知识可及性增量**：翻译是否使用户第一次便捷获得高质量资料；“潜在高”只是研究假设，非已量化事实。
5. **用户需求/广告可行性**：已有搜索信号、独立搜索竞争、可能的页面阅读与再访；缺少真实数据仍为UNKNOWN。
6. **工作量/维护风险**：翻译规模、更新频率、跨语言专业审核及是否复用go-dev设施。

不对不同研究深度的候选计算虚假的百分制评分；不将官网拥有多少“语言”直接从66里减去，不比较未经核实的总净收益。

## 三、全部主要候选复评矩阵

| ID | 候选与项目类型 | 已知同源/同功能重复证据 | 内容增量价值判断 | 主要硬风险 | 目前建议 |
| --- | --- | --- | --- | --- | --- |
| RST | Rust六模块学习体系；翻译 | Book等有多门社区译本；ko-KR多模块已有正文，zh-CN教程/练习竞争明显；By Example有内置翻译机制 | **部分模块重译率可能偏高**，其他目标locale和模块仍UNKNOWN | 六模块持续更新、质量审核；官方带广告译站收录UNKNOWN | 保留；不再因工程复用自动列第一 |
| PY | Python官方教程与文档；翻译 | 官方zh-CN、ja-JP核心高度覆盖，de-DE核心100%；还有大量第三方教程 | 官方有效支持部分一般排除；未覆盖的高级资料仍可能有增量，但范围UNKNOWN | 官方自身持续翻译、版本更新、同主题竞争 | 保留、偏低的增量优先度 |
| OWASP | Cheat Sheet Series；翻译 | 3主题zh-CN同源正文、日语历史译文样本；德语同主题权威资料 | 其他locale/主题的增量**尚不明**，不能把3篇样本扩展到全项目 | CC BY-SA合规；安全修正须及时传播 | 保留，重视维护负担 |
| SHP | Shopify开发者学习体系；**合法模块翻译+外链** | 官方及第三方存在开发资料，精确同源覆盖未系统核实 | 部分开放模块可能具有增量，但外链不形成本站翻译增量 | 整个官方文档商业再分发UNCLEAR；季度API更新 | **许可范围先行**，不能视为可完整翻译全站 |
| ETH | ethereum.org开发者文档；翻译候选 | 官方翻译计划历史记录多语言；2篇×zh/de已有4个官方译文样本；完整有效覆盖UNKNOWN | 官方有多语的部分可能直接排除；其余模块增量无法量化 | CC BY文字可用条件已核查，网站条款和素材复用仍UNCLEAR | 暂缓整站选择 |
| AI | AI基础与应用教育；具体源依赖型翻译 | 微软Generative AI for Beginners源仓库列出50多种本地化版本；是否每模块完整需审计 | **若微软课程源维护的官方译文有效，新增语言空间可能相对有限**；其他原创开放AI教材不能套用此结论 | 快速更新，源级素材/质量与独立价值 | 按**具体教材**再细分，不将整个AI领域定低 |
| HIS | 世界历史三本开放教材；翻译 | 8 locale×3书抽样，仅确认SOURCE_A西班牙语12章目录和部分正文；其他23组合 NOT_FOUND_IN_SAMPLE | **值得优先核实的稀缺性假设**；不能直接证明23个组合空白 | 史实/译名审校、图片地图授权、跨文化历史解释 | 在纯翻译型中提高**后续决策关注度** |
| GEO | 国家地理知识与交互工具；混合/工具 | Seterra、JetPunk、DodoThinks等功能成熟，部分支持大量语言 | 不是同源教材重译；应计算**未满足功能和可靠数据的增量** | 地图与行政区划维护、争议标注、功能复制风险 | PARKED；不能用“低翻译重复”虚假加分 |
| DATA | 开放统计数据比较工具；工具 | OWID、WorldData已提供对比、图表及导出；具体新任务仍不清楚 | 不是同源译本问题，优先核实**独特任务/数据解释价值** | API/数据许可各异，数据更新与维护 | 保留，但缺少具体差异化任务 |

### 重要判定

- “高同源重复”不等于已证实66-locale全部重复。
- “尚未找到同源译本”不等于低重复已证实。
- 翻译型项目与数据工具不能只按一个“重复内容比例”做数值排序。
- 不把成熟搜索竞争直接等同于同源译本重复；也不因重复率可能高便违反负责人“社区译本仍重译”的执行规则。

## 四、保留的其他明确子候选与开放方向

| 子候选 | 来源/既有状态 | 增量复评 |
| --- | --- | --- |
| DeepSeek API开发文档与错误处理 | 官方文档存在，模型权重/代码/文档许可不能混同；完整商业复用仍UNCLEAR | 不能在授权未清时按稀缺性批准独立重译；错误诊断任务已存在上游解决方案，不自动形成翻译网站机会 |
| Solidity/Vyper等合约编程语言资料 | Ethereum研究中提及，但不可用ethereum.org许可覆盖其独立文档 | **独立来源评估**；同源覆盖、许可、维护与搜索需求目前不足，不能当作ETH现有文档已核实 |
| HIST_DATE 历史日期转换 | 英德西中已有直接工具；非大规模同源翻译项目 | 按具体未满足转换功能评估，既有停止线继续有效 |
| AI伦理等其他开放教材 | 已发现Ethics and Artificial Intelligence目录，源版本/许可证仍未充分确认 | 只有候选发现，不可视为已拥有完整合法的66-locale翻译来源 |
| 世界政治制度、公共知识、社会科学 | 项目初始研究范围允许，但尚未确定可商用、可完整翻译的具体来源 | DISCOVERY_ONLY；不得拿未研究的领域与已核查完整项目做确定排名 |

这些子方向仍可被研究，但目前不应因名称更换或低检索覆盖而宣称内容稀缺。

## 五、重点候选的定性比较

### 5.1 世界历史与Rust

**世界历史的已确认同源竞争样本较少，Rust的部分已核实译本竞争较多**。这使世界历史成为新标准下更值得进入下一轮可比性核查的候选，而不是立即认定历史在66-locale中具有最低重复率。

注意：Rust现有样本覆盖10 locale×6模块；历史仅8 locale×3本书，且样本检索方法、章节粒度不同，不能对“1/24 vs Rust若干”做直接率值比较。

世界历史增量需核实是否存在可用的本地世界史替代教材；即使不是同源翻译，也会影响用户价值和SEO，但不减少同源稀缺性。

### 5.2 OWASP的稀缺性与负担

OWASP潜在源级语言空白可能不小，但每篇安全指南涉及后续准确性更新。若66-locale都重新译，旧文安全建议传播的风险与维护成本会放大；不能仅因某语言缺少同源译本而自动给高优先级。

### 5.3 Python、微软AI课程、Ethereum的官方覆盖

Python和微软课程已经存在正式的官方或源仓库内译本支持。对拟选源的具体模块核实后，这些语言可能默认不进入项目重新翻译范围。Ethereum也有官方多语计划，但官网语言数不等于所有开发文档语言完整性。

相反，Rust部分社区译本虽然很成熟，**按照负责人规则依然全部重新翻译对应locale（除官方有效支持者）**；这一点是本轮比较与执行范围的关键差异。

### 5.4 Shopify的混合路线

只能翻译明确开放授权的文档模块，其他部分链接到官方。即使社区翻译较少，**来源本身不能合法完整独立托管**，仍然可能导致内容体系不完整及外链流失PV，不能仅凭“稀缺”提升为完整翻译项目。

## 六、当前相对机会判断（非广告收益排名）

在**“明确许可的完整翻译来源 + 已有同源翻译相对稀缺 + 维护可控”**三个目标之间，现有证据支持以下**调查顺序**：

1. **HIS：先验证**三本书中的一项源级、可比语言覆盖及媒介权利边界；它具有潜在内容稀缺性，仍没有证明66-locale总体低重复。
2. **RST：保留主要备选**，明确哪些模块确实存在完整社区译本，以及整个重译计划是否仍有合理知识可及性增量；工程复用优势保留。
3. **OWASP：条件备选**，必须把安全更新及时性作为硬成本考量。
4. **PY/微软AI官方支持课程**：因官方/source-owner现有多语言投入，内容增量研究优先度相对较低；但不是永久排除整个技术或AI领域。
5. **SHP/ETH/DeepSeek及Solidity**：独立源授权与可托管内容范围需要先解决，无法按潜在低重复率取代授权底线。
6. **GEO/DATA/HIST_DATE**：属于独立工具路径，保留原本的功能差异化研究状态，不参加“译本重复率”直接排序。
7. **POLSOC/其他具体未选开放书**：只标记源发现不足，不用“未知=高价值”做排名。

上述顺序表示**当前研究边际价值和下一项核实优先度**，不是项目商业收入、长期广告净利或已经获授权的开工顺序。

## 七、可操作的统一比较样本与停止线

为了不启动66-locale全量审计，下一项低成本研究建议：

- 固定一组此前研究使用过的代表locale：zh-CN、ja-JP、de-DE、es-ES、id-ID；不能冒充全部66。
- 对 HIS 三本教材、RST 六模块、OWASP 三主题各做相同定义的官方/社区源级核查。
- 对 PY、微软AI、ETH 按其官方支持的具体模块先核实有效覆盖；不要重复已经有官方完整译本的语言。
- Shopify/DeepSeek等受许可证限制者只对明确合法的具体源建立覆盖表。
- 对工具类完全独立的“已满足/未满足功能”矩阵，不与翻译类比例混合。
- 为每个来源记录 URL、源版本/更新日期、目标locale、正文或练习存在性、完整程度、证据状态、来源权利及维护信号。
- 只复用可追溯现有证据；如果不能比较，则标记 UNKNOWN，优先补**最能改变候选选择的一项**，不穷尽调查。

**特别声明**：本项目不实施“已有社区译文就不重新翻译”的过滤。它是选题阶段对重复劳动与知识可及性增量的减分信号，不是译文任务分配规则。

## 八、结论

`ALL_MAIN_CANDIDATES_REASSESSED=9`
`ADDITIONAL_SUBCANDIDATES_OR_OPEN_DIRECTIONS_REVIEWED=5`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`COMMUNITY_DUPLICATION_AFFECTS_PROJECT_SELECTION=YES`
`HIS_CONTENT_NOVELTY_HYPOTHESIS=PRIORITY_TO_VERIFY`
`RUST_PREVIOUS_SOLE_FRONT_RUNNER=WITHDRAWN`
`TRANSLATION_CANDIDATE_RANKING=QUALITATIVE_PROVISIONAL_ONLY`
`NET_AD_PROFIT_RANKING=NOT_READY`
`ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN`
`AD_PAGE_RPM=UNKNOWN`
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`
`SECOND_PROJECT=NOT_DECIDED`
`FORMAL_PROJECT_SELECTED=NO`
`RESEARCH_ONLY=YES`
`NEXT=SOURCE_LEVEL_ALL_CANDIDATES_COMPARABILITY_AUDIT`

不启动翻译，不建立新站，不部署，不购买域名，不修改go-dev v2。

## 九、证据追溯与官方来源

研究仓库（复用已归档结果）：

- research/2026-11-04-rst-full-ecosystem-license-and-coverage-gate-001.md
- research/2026-11-05-rst-language-opportunity-reassessment-001.md
- research/2026-11-04-his-licensed-corpus-scope-gate-001.md
- research/2026-11-04-his-source-specific-translation-coverage-pilot-001.md
- research/2026-11-05-owasp-translation-competition-and-search-intent-gap-pilot-001.md
- research/2026-11-05-py-official-translation-coverage-and-search-intent-stop-pilot-001.md
- research/2026-11-05-eth-commercial-reuse-clarification-stop-gate-001.md
- research/2026-11-04-shopify-project-level-demand-feasibility-screen-001.md
- research/2026-11-04-geo-specific-user-value-gap-check-001.md
- research/2026-11-05-hist-date-intent-gap-stop-pilot-001.md
- research/2026-11-03-cross-domain-commercial-evidence-001.md

2026-11-06额外核实官方公开来源：

- Rust By Example翻译机制与MIT/Apache-2.0： https://github.com/rust-lang/rust-by-example
- Rust Book翻译机制： https://github.com/rust-lang/book
- OWASP Cheat Sheet CC BY-SA 4.0： https://github.com/OWASP/CheatSheetSeries/blob/master/LICENSE.md
- 微软Generative AI for Beginners源仓库译文清单（50多语言）： https://github.com/microsoft/generative-ai-for-beginners
- 微软课程MIT许可证： https://github.com/microsoft/generative-ai-for-beginners/blob/main/LICENSE

上述网页核实仅确认当前公开声明，不能替代文件级权利核查或译本完整性审核。
