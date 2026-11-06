# 已授权内容子集的项目级商业价值决策修正 001

日期：2026-11-06
阶段：LICENSED_CONTENT_SUBSET_COMMERCIAL_PROJECT_GATE
状态：RESEARCH_ONLY
涉及候选：SHP、ETH、DeepSeek（原则适用于所有混合授权来源）
正式第二项目：NOT_DECIDED

## 一、纠错背景与权威原则

本研究在2026-11-03已正式确定：
`LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`。

权威前驱：
`research/2026-11-03-shopify-licensed-translation-official-links-decision-001.md`

项目负责人于2026-11-06再次明确：**不要求整个官方文档体系获得商业翻译授权；仅翻译具体、明确允许商业再分发的内容，其他资料直接链接至官方。第二项目评价应聚焦合法可翻译内容子集是否值得建立新项目。**

因此对近期两份全候选报告中可能将「整站/整套官方文档版权UNCLEAR」视作整个项目不能继续商业比较的表述予以纠正。

这不是把未知授权改为已授权，而是把评估对象从「无法保证整站合法」改为「已核实合法内容白名单是否足以形成独立有价值的站点」。

## 二、正式四分类

- `LICENSED`：指定版本与文件具有足够明确的商业翻译、修改、独立再分发许可依据；遵守署名、许可说明和例外处理。
- `EXTERNAL_LOCALIZED`：本站无明确再分发授权，官方有目标语言页面；直接链接。
- `EXTERNAL_ENGLISH`：本站无明确再分发授权，官方缺相应语言；链接官方英文页面。
- `UNAVAILABLE`：链接无效/资源不在；不创建内容空壳页。

当内容许可或获取路径存在实质疑问时，该内容**不进入 LICENSED 白名单**，可在来源有效时列为外链。无需为整个项目申请“全站授权”。

仅有外链目录不等于本站有效内容资产；不得把官方网页的阅读PV或广告收益计入本站。

## 三、对三项候选的实质修正

| 候选 | 已经存在的授权基础（按既有仓库证据） | 不能据此声称 | 真正需要做的项目级评估 |
| --- | --- | --- | --- |
| Shopify | 六个指定官方 GitHub 仓库先前已核实根目录MIT：theme-liquid-docs、shopify-app-js、hydrogen、cli、theme-extension-getting-started、shopify-ai-toolkit | 六大板块完整文档都授权；每个源码素材/生成文档都同权；整体shopify.dev可复制 | 对实际适合用户阅读的合法JSON/Markdown参考和学习指南建立白名单，判断其完整性、更新成本、搜索需求与访问价值。未授权官网资料外链 |
| Ethereum | 官网默认非代码文本CC BY 4.0、代码MIT的公开声明；开发者文档有公开Markdown源码路径；已在既有研究中核实部分文字版权商业改编的**条件性**依据 | 所有图片、第三方示意图、商标、获取路径均无条件合法；网站服务条款与内容许可歧义已全部解决 | 只核查可明确归入CC BY的具体文字及合法获取路径，排除UNCLEAR文件/图；其余资料直接外链。评估剩余合法内容的独立价值 |
| DeepSeek | DeepSeek-R1等特定GitHub仓库有既有MIT授权调查；仓库内受许可覆盖的README/技术说明可列为进一步文件级候选 | MIT模型/仓库许可覆盖整个DeepSeek API网站文档或模型权重；仓库README就是完整API教程 | 将受MIT覆盖的**实际技术内容**与未获商业再分发授权的API文档分离；后者外链。评估仓库合法学习资料是否足够完整、长期有人查阅及有利于广告网站 |

以上是对**既有核实结论**的重分类，而不是2026-11-06重新逐文件发布版权审查结果。对有第三方材料或适用条款争议的具体文件，仍需 fail closed，不放入可翻译白名单。

具体原始记录：
- `research/2026-11-04-shopify-licensed-vs-external-module-coverage-001.md`
- `research/2026-11-05-eth-commercial-reuse-clarification-stop-gate-001.md`
- `research/2026-11-03-source-license-screening.md`

## 四、六个真正决定能否立项的问题

针对每个候选的 **LICENSED 子集**回答：

1. **内容体量与完整性**：已核实合法的、面向最终读者的实质内容有多少？能否支持从入门到进阶或有用的参考查询？不足时能否接受少量官方外链？
2. **来源稀缺性**：针对既定66 locales，官方有效支持哪些来源模块？社区已有同源译本多少？**社区已有译本仍须重译**，但重复风险降低项目增量价值。
3. **稳定性**：多久更改、更新后的翻译/审核成本如何？API动态版本说明不能直接当作长期稳定教材。
4. **用户价值**：用户会在本站阅读/使用什么，而非只点击外链？不得把导航链接数当作内容价值。
5. **自然搜索与商业价值**：合法内容是否对应长期可检索需求、有多语言用户，以及合理的广告展示机会？流量/RPM不足时记UNKNOWN；允许低于go.dev的可接受回报，但不能编造收益。
6. **实施成本与许可边界**：合法内容白名单的文件审核、术语审校、版本更新和版权遵守是否可控，且不干扰go-dev v2？

**许可证只决定内容能否进入白名单；项目价值决定整个候选是否值得做。** 两者不能混为一谈。

## 五、三候选的阶段性差异（非商业排名）

### Shopify
当前已核实六个仓库的MIT基础与一些具体JSON/Markdown指南。其合法子集横跨Liquid、App SDK、Hydrogen、CLI等，但完整教学体系和真正面向人类读者的内容数量尚不能确定。**候选保留，不要求Shopify全站授权。**

### Ethereum
默认CC BY文字存在积极许可证据；部分官网条款与第三方素材需要按实际来源/获取方式处置。**不能把存在争议的某些文件直接判定为整个候选被阻断**，也不能认为全部开发者资料都已清白。合法子集可以作为独立候选比较，尚需明确文件界限。

### DeepSeek
受MIT覆盖的特定仓库内容可以继续作为合法子集候选，但官方API文档不能借此取得许可。**问题更可能是合法可翻译的开发者学习内容是否足够丰富，而非一定要拿到整个API官网授权。**

三个方向的长期搜索流量、广告Page RPM、长期净收益仍为 UNKNOWN；此前的暂停只是研究资源决定，并不是“整站未获授权便永久淘汰”。

## 六、与最新候选规则衔接

继续适用已确认的全部用户偏好：

- 固定66 locale，具体内容的官方有效支持范围用于判断默认排除；不能以官网语言菜单数量机械相减。
- **社区已有完整译本不排除该locale**；作为立项前的重复生成风险。
- 减少不必要重复翻译、增加稀缺语言可用知识，属于独立的内容增量价值评价。
- 接受潜在广告回报弱于go.dev，但长期维护成本、真实内容价值、商业权利不能忽略。
- 地理与数据工具按功能增量评价，不套用同源教材翻译标准。

## 七、结果与下一步

`POLICY=LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`
`WHOLE_SITE_LICENSE_REQUIRED=NO`
`UNCLEAR_CONTENT_TRANSLATED=NO`
`UNLICENSED_CONTENT_ACTION=OFFICIAL_LINK`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`SHP_REMAINS_ELIGIBLE_FOR_LICENSED_SUBSET_ASSESSMENT=YES`
`ETH_REMAINS_ELIGIBLE_FOR_LICENSED_SUBSET_ASSESSMENT=YES`
`DEEPSEEK_REMAINS_ELIGIBLE_FOR_LICENSED_SUBSET_ASSESSMENT=YES`
`LICENSED_SUBSET_PROJECT_VALUE=UNKNOWN`
`FORMAL_PROJECT_SELECTED=NO`
`SECOND_PROJECT=NOT_DECIDED`
`RESEARCH_ONLY=YES`

`NEXT=LICENSED_SUBSET_VALUE_SIDE_BY_SIDE_REVIEW`

下一步优先利用已存资料，对三者已授权内容子集做**小范围、同口径项目价值比较**，而不是重新启动整站版权调查或无限扩充开源仓库。得不到充分源级内容时如实标记UNKNOWN，并维持研究停止线。

不启动翻译、建站、部署、购买域名，不修改go-dev v2。
