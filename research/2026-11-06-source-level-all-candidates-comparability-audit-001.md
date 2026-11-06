# 全候选来源级可比性与“官方 / 社区”边界审计 001

日期：2026-11-06
阶段：SOURCE_LEVEL_ALL_CANDIDATES_COMPARABILITY_AUDIT
状态：RESEARCH_ONLY
比较范围：已保留9个主候选 + 5个子候选/开放方向
商业目标：长期合法广告净收益，同时重视真实的多语言知识可及性增量
正式第二项目：NOT_DECIDED

## 一、输入与本轮实际操作

这是对现有研究报告的**只读证据综合与分级**，不是一轮新的66语言全量网络爬取或原文审校；未获得新数据的项目维度保留UNKNOWN。

输入：
- `research/2026-11-06-all-candidates-content-incremental-value-reassessment-001.md`
- `research/2026-11-06-multilingual-content-incremental-value-selection-rule-001.md`
- `research/2026-11-04-source-equivalent-translation-competition-policy.md`
- `research/2026-11-04-rst-source-equivalent-translation-coverage-pilot-001.md`
- `research/2026-11-04-rst-targeted-body-completeness-check-001.md`
- `research/2026-11-04-his-source-specific-translation-coverage-pilot-001.md`
- `research/2026-11-05-owasp-translation-competition-and-search-intent-gap-pilot-001.md`
- `research/2026-11-05-py-official-translation-coverage-and-search-intent-stop-pilot-001.md`
- `research/2026-11-05-eth-terms-and-source-equivalent-coverage-pilot-001.md`
- `research/2026-11-04-shopify-licensed-vs-external-module-coverage-001.md`
- `research/2026-11-04-geo-specific-user-value-gap-check-001.md`
- `research/2026-11-03-source-license-screening.md`

## 二、负责人确认的执行范围与评估边界

> 一旦选定翻译项目，冻结的66个locale里，**官方未有效支持的语言原则上统一重新翻译**；已有社区译本，无论完整或过时，均**不自动退出**本项目计划。

`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`COMMUNITY_DUPLICATION_AFFECTS_PROJECT_SELECTION=YES`
`OFFICIAL_EFFECTIVE_SUPPORT_MUST_BE_VERIFIED=YES`

适用的**官方支持分级**：
1. `OWNER_OFFICIAL_EFFECTIVE`：源项目/官方平台实质性发布、提供对应源版本与完整目标译文，并有明确维护责任；仅在确认本项目全部相关内容范围已被支持时，才考虑项目级语言排除。
2. `OWNER_HOSTED_OR_INTEGRATED_PARTIAL`：官方平台中有真实译文或贡献内容，但整体/模块完整性未知或部分完成。
3. `OFFICIAL_DIRECTORY_COMMUNITY`：官方网站仅列出、链接、收录社区译本；**不是**官方已完整支持的自动证据。
4. `INDEPENDENT_COMMUNITY`：独立第三方的同源译文；评估项目内容重复，但**不排除locale**。
5. `NOT_FOUND_IN_SAMPLE`：样本中没有找到；**不是缺失已证实**。
6. `UNKNOWN`：无可判断证据。

上游所有者公开接纳译文PR、仓库里存在社区贡献、官方网页显示locale菜单、第三方自称official，均不足以独立证明官方对**完整计划源范围**的持续有效支持。

对于“官方仅覆盖部分模块”的项目，不能因一个模块翻译完整就排除整个locale；最终还需要决定对应项目语言级排除逻辑与模块级完整范围。**本轮不擅自生成确切的 66 - N 数字。**

## 三、翻译型 / 混合型候选的来源级可比性

| ID | 已固定可核实的源内容 | 官方有效覆盖证据 | 社区同源译本证据 | 关键缺失 | 判断 |
| --- | --- | --- | --- | --- | --- |
| RST | Book、Rust By Example、Cargo Book、Reference、Nomicon、Rustlings六模块 | Book官方翻译目录收录社区版；RBE有仓库内置翻译机制；**不能把目录链接当作OWNER_OFFICIAL_EFFECTIVE** | 10 locale×6模块的线索样本；ko四模块有大量实际非空PO条目，zh/ja Rustlings有练习文件 | 66语言全项目官方完整支持状态、社区全文完整性、源版本对齐 | 来源范围已定义；**社区重复有实际证据，但可比性未达到完整覆盖率级别** |
| PY | Python文档（Tutorial、Core及更完整文档体系） | 官方docs.python.org有中文、日语、德语、西班牙语Tutorial正文；2026-11-04面板核心/整体覆盖分开统计 | 另有大量同主题教程，不等于全部是同源翻译 | 模块级已完成范围与本项目完整内容范围不一致；其余62个locale覆盖 | **官方覆盖有较强证据**，但不能把Core比率折算为整个项目的排除语言数 |
| OWASP | Cheat Sheet Series（3主题已取样，全部目标尚未冻结） | 指定三篇英语官方页面；目标语言官方有效支持未建立完整审计 | 中文三篇正文存在、日语三篇历史V1译本 | 其他主题/locale官方与社区覆盖、严格版本对齐和安全修订成本 | 同源竞争样本成立，**全项目重复规模UNKNOWN** |
| SHP | 六类部分MIT许可仓库资料 + 未授权模块仅官方外链 | 整个shopify.dev多语言实际开发文档覆盖未知；原站其他模块不能合法推定为全部可翻译 | 具体同源翻译覆盖调查不足 | 决策对象不能混称完整官方文档；需先冻结**合法可托管内容清单** | **来源边界不完整，先解决范围，再比较重复度** |
| ETH | ethereum.org开发者正文（部分CC BY 4.0）及代码（不同许可） | zh/de各两篇官网正文已实证；历史68语言计划与当前约25入口不能等同完整开发者文档支持 | 有社区贡献历史，但最终在官方站发布的真实正文与外部社区页面需区分 | 独立托管权利歧义、文件级第三方许可、当前多模块×locale完整覆盖 | **官方局部覆盖证据存在，授权仍有UNCLEAR** |
| AI | 微软Generative AI for Beginners等；不同课程必须分源 | 微软源仓库列出50多语言翻译，**尚未核实其所有模块由上游实质发布维护** | 同主题教程及独立译本范围不明 | 课程级官方完整覆盖、源版本、教学材料许可例外；不代表整个AI方向 | **只可比较某本具体课程，不可比较“AI全领域”翻译缺口** |
| HIS | 三本具体开放教材（12章+15章通史，第三本国际关系史） | 官方出版社多语全文覆盖：本轮无可确认量化数据；无证据不能推定0 | 8 locale×3来源；一项西语译本具12章目录并有部分正文，其余23项NOT_FOUND_IN_SAMPLE | 其余文本完整性、文件级插图/地图权利、各locale真实可用译本 | **稀缺性潜力值得验证；样本较浅，不能宣称已证明低重复** |

### 3.1 不能混用的数字

- Rust **60个组合**：10种locale×6模块，是翻译线索采样范围，不是60个全文审计通过项。
- Rust ko四模块 PO 文件具有大量非空译文条目，但解析条目/候选文本不能等价于整本教材完成率、质量或版本同步。
- Rustlings zh/ja文件路径匹配不代表全部提示、题目、测试和答案与最新版一致。
- 历史 **24个组合**：8种locale×3部原书；一个有西班牙语12章结构与正文样本，其余23个没有找到**可核实完整**同源译本，不是23个已证实空白。
- OWASP **3主题×2目标语言**的正文存在性，是6个目标语/主题组合的局部样本（加上3个英语原文），不是66语言的重复率。
- Python zh-CN、ja-JP、de-DE、es-ES核心/整体进度是官方平台快照，不是“官方支持了四个完整语言项目”的证明。
- 微软课程50多种语言是仓库提供的语言清单，不是全部章节逐文件最新审校结论。
- Ethereum官方历史68语言计划数和当前实际网站菜单约25个入口属于不同时间/统计口径；**两者都不可直接作为66的减数**。

## 四、纯工具/数据与混合型项目

| ID | 可核实对象 | 核心“重复”指标 | 当前证据 | 可比性 |
| --- | --- | --- | --- | --- |
| GEO | 国家地理、区划、地图测验与地图功能 | 功能已满足程度、时效与本地数据可用性 | Seterra、JetPunk、DodoThinks、MapChart、OWID；部分行政区划时效差异 | **不能用“社区同源译本重复率”比较** |
| DATA | 开放统计指标与跨国比较 | 用户任务是否被已有统计工具满足；可复用数据是否有授权且保持时效 | OWID、WorldData提供对比与可视化；具体新的数据解释任务未证实 | 同为功能增量，独立于翻译覆盖 |
| SHP（混合） | 合法模块翻译+官方外链 | 被合法翻译的内容增量与外链范围；不能统计外链为翻译 | 6仓库为部分合法来源；六开发功能板块均未证实本站可完整覆盖 | 同时需要来源/功能两套口径 |

因此可以对这三者作**商业和工作量层面定性比较**，但不应该与Rust/历史等教材拿同一个“同源语言空白率”数值横向排名。

## 五、其余保留子候选与来源边界

| 子候选 | 现有来源事实 | 当前不能成立的推断 | 下一步必要前提 |
| --- | --- | --- | --- |
| DeepSeek API/错误诊断 | 官方API文档与某些公开代码仓库可分别找到；官方完整商业文档复用UNCLEAR | 某个MIT模型或仓库许可 = 整个API官方文档可商业重译 | 明确独立内容源授权，分离软件缺陷与内容网站需求 |
| Solidity/Vyper | 与ethereum.org不同的编译器/语言文档来源 | ethereum.org CC BY 4.0自动覆盖Solidity/Vyper | 各自固定源版本、许可证及官方实际locale覆盖 |
| HIST_DATE | 历史文献日期转换工具，英德西中样本存在直接工具 | 现有工具功能重复=文献翻译重复 | 以算法准确性、历史解释与搜索任务缺口评估 |
| AI伦理开放教材/其他开放教材 | Ethics and Artificial Intelligence曾在目录被发现，许可为线索 | 目录CC BY=具体全书文件均可商业复制 | 原出版版本与文件级权利核实，方可与其他教材比较 |
| POLSOC（政治制度/公共社会科学） | 作为项目开放领域保留 | 未发现同源翻译=已经证明稀缺 | 先选择具体可商用知识来源；当前DISCOVERY_ONLY |

AI方向另有 Dive into Deep Learning、Google ML Crash Course、Google ML Glossary等具体来源，存在不同授权与官方多语覆盖；应按**每一教材/词典独立评估**，不因微软课程语言多就淘汰全部AI教育。

## 六、决策缺口的优先级

已经有足够证据判断：
- Rust确有社区同源重复风险，不能因为工程复用就列为自动第一。
- 世界历史三本书具合法正文来源及稀缺性研究价值，**并未证实整个66-locale项目低重复**。
- OWASP中文/日语有同源正文线索，更新压力比静态教材更值得关注。
- Python及微软特定教材的**源所有者多语言支持**是可能缩减计划重译范围的核心变量。
- Shopify、Ethereum、DeepSeek等候选的**具体内容托管许可范围**仍可能先于重复度成为决定障碍。
- GEO/DATA是工具，不应假装同源翻译项目。

但由于现有样本在**研究对象（6模块 vs 3教材 vs 3主题）**、**locale集合（10 vs 8 vs 2）**、**官方完整度检查深度**上不同，不构成可对比的完整百分比或“增量分数”。

### 决定性定义歧义（必须先统一）

1. **Rust官方社区链接**是否算作官方有效支持？按照已明确的用户规则，建议**不算**，除非来源所有者真正发布/维护该具体目标完整译本；仅链接仍为社区翻译。
2. **微软仓库内翻译**是否算官方支持？需要确认源所有者是否实际发布/维护该模块全文，不能简单因为GitHub组织为Microsoft就一概减去对应locale。
3. **官方部分译本**是否排除整个项目的locale？**不能**；应基于已确定的项目完整源范围、模块覆盖逐项判断，并把缺失内容与整体翻译计划区别开。
4. **多地区同语种**（如de-DE/de-AT）：目标locale不变，但需记录现有材料的有效替代性，避免在项目价值上重复计算稀缺性。

## 七、下一次决策门禁——不再做一轮全量爬取

本轮最有用的结果不是任意高低分，而是明确下一次决策前的最小信息：

**只做一次针对“官方支持究竟怎样排除locale、社区译本是否只是列名”的来源归属验证。**

优先用三种不同模式的来源各取一个小样本：
- Rust Book：官方目录收录、外部社区维护的翻译。
- Microsoft Generative AI for Beginners：来源所有者仓库内提交的翻译。
- History SOURCE_A：出版社英文原书与西班牙语外部译本。

比较的是**所有者发布责任、内容完整性证据与社区重复风险**，不是立刻全量审核语言或正文；如结果仍然不改变候选方向则停止。

在完成这一最小澄清后，综合授权、知识可及性增量、更新成本、合理但可接受的较低商业收益，形成第二项目**有条件的选择建议**，不继续循环新增候选。

## 八、当前决策

`ALL_MAIN_CANDIDATES_AUDITED=9`
`ADDITIONAL_DIRECTIONS_AUDITED=5`
`SOURCE_LEVEL_NUMERIC_COMPARABILITY=INSUFFICIENT`
`OFFICIAL_COMMUNITY_OWNER_BOUNDARY=KEY_UNRESOLVED_COMPARABILITY_ISSUE`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`COMMUNITY_TRANSLATION_IS_DUPLICATION_RISK=YES`
`HIS_HYPOTHESIS=CONTINUE_CONDITIONAL_REVIEW`
`RST_HYPOTHESIS=CONTINUE_CONDITIONAL_REVIEW`
`SECOND_PROJECT=NOT_DECIDED`
`FORMAL_PROJECT_SELECTED=NO`
`ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN`
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`
`RESEARCH_ONLY=YES`
`NEXT=SOURCE_OWNER_OFFICIAL_SUPPORT_BOUNDARY_PILOT`

不启动翻译，不创建/部署网站，不购买域名，不改go-dev v2。

## 后续正式修正：合法内容子集优先于整站授权（2026-11-06）

本节为较晚的用户指示修订，涉及 Shopify、Ethereum、DeepSeek 的商业授权解释时**以本节为准**。请参见：
`research/2026-11-06-licensed-content-subset-commercial-project-gate-001.md`。

原来把“整套官网文档没有取得明确授权”当成**该整个候选暂不能比较商业价值**的做法过于严格。项目早已采用：

`LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`

即：**只翻译具体且明确允许商业翻译、独立再分发的内容；其他内容直接链接官方，不要求获得整套官网文档许可，也不要求原创教材补齐。**

所以 Shopify、Ethereum、DeepSeek 都可以针对合法内容白名单，继续比较其内容体量、学习体系完整性、同源重复、目标语言增量、更新成本、搜索需求和可变现页面价值。

这是**立项范围选择**与**单个内容文件的合法性**分开判断。已有许可证不自动覆盖未审计的文件、素材、网站访问条款或整个API文档；`UNCLEAR` 文件仍不得进入本站翻译白名单。但无需先消除官网所有未授权内容的问题才评价整个候选。

同时保持：社区已有译本**不**排除该语言；只是影响整个项目的重复投入和增量价值。

`WHOLE_SITE_LICENSE_REQUIRED=NO`
`LICENSED_SUBSET_VIABILITY_MUST_BE_EVALUATED=YES`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`NEXT=LICENSED_SUBSET_VALUE_SIDE_BY_SIDE_REVIEW`
