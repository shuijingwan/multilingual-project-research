# 第二多语言项目：全候选有条件选择建议 001

核实与建议日期：2026-11-06
阶段：ALL_CANDIDATES_CONDITIONAL_SELECTION_DECISION
仓库状态：RESEARCH_ONLY
当前主项目：go-dev v2
正式第二项目：NOT_DECIDED
决策性质：RESEARCH_ADVISOR_RECOMMENDATION（不是项目负责人正式批准）
目标：长期合法广告净收益，同时减少同源重复投入、增加高质量多语言知识可及性

## 一、最新且具有约束力的选择规则

本轮以前驱文档记录的负责人最新指示为准：

1. **不要求第二项目达到go.dev同等级的广告回报**。项目应仍然具有长期用户价值，内容更新、质量审核与运营成本应可控。没有可靠数据时自然流量、RPM、净收益继续UNKNOWN，不编造商业预测。
2. 目标范围为冻结的66个locale。**一旦正式选定翻译项目，除了该项目具体正式源内容已被官方有效完整支持的locale，其他locale原则上重新翻译**。官网语言菜单、仅有社区链接、源项目内贡献入口都不能直接证明官方完整支持。
3. **即使存在社区完整同源译本，对应locale也不会被排除或改为复用社区译文**；社区重复度只影响整个项目的立项选择，而不是项目选定后的语言筛选。
4. **LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS**：任何候选只翻译确有商业翻译和再分发许可的内容；不明确、不允许或难以合法取得的资料只链接至官方。**不要求获得整站统一授权**，也不要求原创编写缺失教材补齐导航。
5. 将商业搜索竞争与指定原书/模块的同源重复翻译竞争分开；历史的其他教材、Rust原创教程等是搜索和用户意图竞争，不是指定原书已被翻译的证据。
6. GEO、DATA及历史日期换算属于工具/数据任务，不用教材同源重复率做错误排名。
7. 用户价值仍优先于页面数或语言数；Google的规模化低价值内容政策限制仅为增加排名而自动翻译大量页面：https://developers.google.com/search/docs/essentials/spam-policies 。

## 二、正式候选建议

### A. 有条件首选：世界历史开放教材（HIS）

建议状态：`CONDITIONAL_FRONT_RUNNER`。

三个明确的来源：
- World History: Cultures, States, and Societies to 1500（UNG；12章；正文CC BY-SA 4.0）
  https://oer.galileo.usg.edu/history-textbooks/2/
- World History Since 1500: An Open and Free Textbook（ETSU；15章；原出版页CC BY 4.0）
  https://dc.etsu.edu/etsu-oer/13/
- History of International Relations: A Non-European Perspective（Open Book Publishers；CC BY 4.0）
  https://www.openbookpublishers.com/books/10.11647/obp.0074

上述出版方当前许可信息于2026-11-06复核。相应正文商业改编有许可证依据，但原书中第三方图、表、照片、引用和改编素材不自动获得同样许可；尤其UNG原书对引入第三方作品作出了明确例外说明。

优点：
- 研究对象是明确、有广泛年代覆盖的**具体来源内容**，不是临时原创覆盖整个世界史。
- 基础历史事实和学习结构相对长期稳定；这只是相较快速API更新的定性维护优势，并不表示史实审校零成本。
- 此前8 locale×3书同源检索中，只核实一项西班牙语译本具有12章目录及部分真实正文；对其余23项仅为`NOT_FOUND_IN_SAMPLE`，**不能视作23个真实空白**。
- 相比已有成熟社区翻译的部分Rust模块，存在值得进一步验证的**多语言知识可及性增量假设**。

主要风险：
- 历史教材版权分层、插图/地图权利、专有名词与史实跨文化审校可能消耗大量精力。
- 教材不像API Reference天然覆盖大量精确长尾查询；能否吸引稳定SEO阅读尚UNKNOWN。
- 先后两本通史是否完全衔接、是否有内容重复、第三本国际关系史如何进入学习路径，仍需在正式执行范围中明确。
- 较少发现同源译文不等于当前语言市场没有高质量历史学习资料。

接受条件：在**正式立项前**冻结三本书版本及合法文本范围，排除没有明确许可的图片/第三方素材；确认首期有效学习路径与历史审校方案；设定go-dev优先以及成本停止线。**不要求先取得精确RPM预测。**

### B. 主要备选：Shopify合法开发文档子集（SHP）

建议状态：`COMMERCIAL_ORIENTED_ALTERNATIVE`。

截至2026-11-06具体MIT仓库材料中已核实：
- Liquid Filters：155个JSON记录。
- Liquid Objects：142个JSON记录。
- Liquid Tags：33个JSON记录。
- Shopify App JS：一个实际包含10份Markdown开发指南的目录。
- 其他已有核实的部分资料涉及Hydrogen、CLI、扩展及AI Toolkit。

这些330个Liquid记录不是330篇必然合格的SEO页面；10篇指南不是完整应用开发课程。合法混合路线**无需取得整个shopify.dev授权**，未许可内容官方外链。

优势：
- 具体开发者查阅任务清晰，结构化参考、语法与SDK指南具可核实的用户应用场景。
- 项目负责人具有开发平台经验，技术理解与工程复用可能较好；但本研究没有量化个人时间优势。
- 在SHP/ETH/DeepSeek三者中，合法来源内可供结构化阅读的资料已经有最明确的量化样本。

风险：
- 官网开发文档与已有教程竞争，版本变化和SDK维护较快。
- API/CLI/Agents部分文件并非面向人类的完整教程；外链不能算本站PV。
- 目标66 locale的官方有效覆盖与社区同源重复仍UNKNOWN。

**切换到SHP成为首选的条件**：负责人最终更重视开发者查询类广告业务和既有技术经验，或HIS实质合法图文/审校成本失去优势；切换不需重新争论整站授权。

### C. 主要备选：Rust六模块完整学习体系（RST）

建议状态：`ENGINEERING_REUSE_ALTERNATIVE`。

六模块：Book、Rust By Example、Cargo、Reference、Nomicon、Rustlings。此前各主要源的开源商业授权基础得到核实，Rust Book有社区翻译官方目录和独立托管先例，但目录收录不等于官方实质完整托管/维护。

优势：学习路径、官方内容质量和go-dev翻译/审校/SEO工程复用较明确。

劣势：多模块社区同源内容已被核实，韩语的Book/Cargo/Reference/Nomicon存在大量非空翻译条目，简中与日语Rustlings有实际练习竞品；这使**完整重新翻译这些locale**在知识增量方面更难胜过真正稀缺的材料。需要持续处理上游技术变化。

**社区译本不因此被跳过**。若选择RST，仍须按已确认的语言策略重新翻译非官方有效支持的locale；这只是降低它当前的整个项目优先级。

### D. 条件备选：OWASP Cheat Sheet Series

建议状态：`MAINTENANCE_SENSITIVE_ALTERNATIVE`。

主许可证CC BY-SA 4.0，三主题中文与历史日语同源正文已核实。其他主题/locale覆盖未知。安全文档更新准确性与紧急修复可能使66语言翻译维护负担明显重于一般静态教材。若能接受安全内容更新的专业审核责任，则保留长期候选；不在当前次序超过前三项。

## 三、其余主要候选与子方向的去留

| 候选 | 本轮决策 | 原因 |
| --- | --- | --- |
| Python官方文档 | RETAINED / NOT_PREFERRED_NOW | 官方中文、日语及德语核心等已有实际翻译，官网文档体系具有直接同源竞争；即使其他模块可翻译，整体内容增量难度较高 |
| AI基础学习（微软Generative AI for Beginners等） | RETAINED / SOURCE_SPECIFIC_REVIEW | 微软指定课程已有50多种语言入口，但并不证明每语言全章由源所有者完整维护；不能把这一课程竞争套用到全部AI教材 |
| Ethereum开发资料 | RETAINED / LICENSED_SUBSET_ELIGIBLE | 默认CC BY文字有许可基础，但部分文件获取/素材权利仍需严格白名单审核；官网已具实际多语言正文 |
| DeepSeek R1与其他开放技术资料 | RETAINED / LICENSED_SUBSET_ELIGIBLE | 特定MIT仓库有实际README等技术内容；不能把模型或仓库许可套用于API网页，当前已核实人类阅读内容规模较薄 |
| GEO国家地理/地图练习 | PARKED / TOOL_TRACK | 现有成熟多语言工具，本轮未发现充分独立功能增量；非同源翻译类 |
| DATA开放统计数据工具 | RETAINED / TOOL_TRACK | 开放数据许可部分已验证，查询与比较功能竞争成熟；需要另立具体用户任务 |
| HIST_DATE历史日期转换 | DEEP_DIVE_PAUSED / TOOL_TRACK | 有真实用户报告，也有多个直接工具满足关键流程；缺少独立搜索价值 |
| Solidity / Vyper | RETAINED / SOURCE_NOT_FROZEN | 不可套用ethereum.org许可；需独立明确来源与版本后才可比较 |
| AI伦理及其他开放教材 | DISCOVERY_ONLY | 目前只有来源/许可证线索，不能以研究深度少视作稀缺性高 |
| 政治制度、社会科学与公共知识 | DISCOVERY_ONLY | 仍在开放领域范围；尚无确定、可商用、可审校的具体全套原始资料 |

这里的项目先后是**当前研究顾问的有条件推荐**，不是成功概率或广告净收益排名。所有保留候选仍可在未来重新开放。

## 四、明确不可推出的结论

- 不存在可信的跨项目月搜索量、自然点击、AdSense Page RPM和长期净收益预测：均`UNKNOWN`。
- 不存在可信的66-locale全部同源翻译空白率：`UNKNOWN`。
- 不将“未查到译本”计作“已证明不存在”，不将官方语言菜单或社区目录链接直接减去66。
- 没有证据表明HIS必然拥有比Shopify/Rust更大的可获取自然搜索流量。
- 没有证据表明2026年的历史教材原本无需要人工审核或可直接商业再分发全部插图。
- 不将个人偏好、公共知识价值直接当作广告收入保证。

## 五、可回退的下一步与正式授权边界

当前阶段**完成有条件推荐，不再循环开展同类广泛候选调查**。

向项目负责人呈现三个清楚的取舍路径：
- **若更重视减少互联网同源重复并增加长期知识可及性：选择HIS进行正式立项决策。**
- **若更重视较直接的开发者检索场景、既有商业开发经验：选择SHP合法内容子集进行正式立项决策。**
- **若更重视go-dev现有工程的高度复用：选择RST进行正式立项决策。**

如果无额外偏好更新，研究顾问建议：`CONDITIONAL_FRONT_RUNNER=HIS`，`MAIN_ALTERNATIVES=SHP,RST`。

下一步**只请项目负责人决定是否接受HIS作为下一正式项目候选**。接受“作为候选”不等于授权现在启动正式翻译或建站。正式立项前必须明确拟翻译的源书/模块、具体许可边界、语言范围、go-dev优先级和有限资源预算。

若主项目go-dev v2尚未具备空余实施能力，可以完成选题记录但暂不启动。

`STAGE=ALL_CANDIDATES_CONDITIONAL_SELECTION_DECISION`
`CONDITIONAL_FRONT_RUNNER=HIS`
`MAIN_ALTERNATIVES=SHP,RST`
`OWASP=CONDITIONAL_ALTERNATIVE`
`SHOPIFY_WHOLE_SITE_LICENSE_REQUIRED=NO`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`SECOND_PROJECT=NOT_DECIDED`
`OWNER_SELECTION_PENDING=YES`
`FORMAL_PROJECT_SELECTED=NO`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN`
`AD_PAGE_RPM=UNKNOWN`
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`
`NEXT=SECOND_PROJECT_OWNER_SELECTION_DECISION`

## 六、核实来源与前驱

2026-11-06复核的官方来源：

- UNG原始出版页：https://oer.galileo.usg.edu/history-textbooks/2/
- ETSU原始出版页：https://dc.etsu.edu/etsu-oer/13/
- Open Book Publishers原始出版页：https://www.openbookpublishers.com/books/10.11647/obp.0074
- Google搜索规模化内容政策：https://developers.google.com/search/docs/essentials/spam-policies

研究仓库前驱：
- research/2026-11-06-licensed-subset-value-side-by-side-review-001.md
- research/2026-11-06-all-candidates-content-incremental-value-reassessment-001.md
- research/2026-11-06-source-level-all-candidates-comparability-audit-001.md
- research/2026-11-06-multilingual-content-incremental-value-selection-rule-001.md
- research/2026-11-06-second-translation-project-threshold-revision-001.md
- research/2026-11-04-his-licensed-corpus-scope-gate-001.md
- research/2026-11-04-his-source-specific-translation-coverage-pilot-001.md
- research/2026-11-04-rst-full-ecosystem-license-and-coverage-gate-001.md
- research/2026-11-05-owasp-search-demand-differentiation-stop-gate-001.md
- research/2026-11-05-py-official-translation-coverage-and-search-intent-stop-pilot-001.md

RESEARCH_ONLY；不批量翻译，不创建新网站、不部署、不购域名、不修改go-dev v2。
