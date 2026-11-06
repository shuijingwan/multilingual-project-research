# 世界历史项目：官方已有英语PDF时是否建立英语网页版——格式缺口例外评估 001

核实日期：2026-11-06
阶段：HIS_ENGLISH_WEB_FORMAT_GAP_EXCEPTION_ASSESSMENT
状态：RESEARCH_ONLY
第二项目：WORLD_HISTORY（已正式选定）
项目域名：world-history；各locale与go-dev正式生产映射一致；额外en-US没有现成Go production hostname authority
正式开发/翻译授权：NO

## 1. 问题与规则的新边界

负责人提出：66种目标语言原本不重复官方已存在语言，但**当英文原著只有PDF、没有独立的HTML全文阅读页时，是否应该建立英文网页以改善体验？**

本报告建议：**允许有条件的“官方语言已覆盖，但官方格式/使用任务未覆盖”例外**。这里并不是“英译英”，而是将**官方、获得商业改编许可的英语正文**转换为具有实质阅读价值的英文HTML页面。

该例外与66-locale策略并行：语言覆盖不能仅凭是否存在PDF或官网菜单判断，还需按**来源书、具体locale、内容范围、呈现形式和用户任务**核实官方有效覆盖。

这是一份研究顾问的**建议**，不是负责人已经批准新的英文站开发，正式权威规则仍待负责人明确采纳。

## 2. 三本教材的英语网页差异

| 书 | 英文内容公开形式（已验证证据） | 建议 |
| --- | --- | --- |
| HIS-A (World History...to 1500) | OpenALG Manifold官方关联阅读平台已有逐章HTML正文，已抽检首/中/末3章；全12章逐一核实仍未完成 | 不优先重复英文页面；先链接现有英文阅读页并完成章节覆盖审查 |
| HIS-B (World History Since 1500) | ETSU官方2022书目、15章PDF已获维护者浏览器下载，sha `fb20f23c3913fcaef68cc503a171e6debe2954775402e83b923722666721cc3b`；官方书目只有PDF下载，“viewed online”不证明语义HTML，公开资料未查到完整正式HTML版 | **有条件推荐基于官方PDF制作英文网页** |
| HIS-C (History of International Relations) | 出版社官方PDF和XML都已取得，另登记HTML ISBN并有Read Online入口，但可直接访问的章节网页暂未验证连续HTML正文 | 先查真实官方英文HTML正文；若存在优质官方版，原则上不重复；若仅目录/元数据或格式不可用，可再按HIS-B同样门禁评价 |

HIS-B官方：https://dc.etsu.edu/etsu-oer/13/
HIS-A官方关联：https://alg.manifoldapp.org/projects/world-history
HIS-C出版社：https://www.openbookpublishers.com/books/10.11647/obp.0074

2026-11-06的外部来源：
- ETSU原文说明“downloaded as a pdf or viewed online”，但实际网页显示PDF查看器，不等于HTML章节；
- Open Textbook Library格式栏目只列PDF：https://open.umn.edu/opentextbooks/textbooks/world-history-since-1500-an-open-and-free-textbook

`HIS_B_OFFICIAL_ENGLISH_PDF=VERIFIED`
`HIS_B_OFFICIAL_ENGLISH_HTML=NOT_FOUND_IN_SAMPLE`
`HIS_B_ENGLISH_WEB_VALUE_SIGNAL=CONDITIONAL_POSITIVE`

## 3. 商业版权：英文原文转HTML与翻译的区别

- ETSU官方原著正文CC BY 4.0，允许满足条件的商业复制与改编，因此**将受许可的英文正文转换为自托管英文HTML页面在许可层面有明确的积极依据**。
- 需要清晰展示作者、原始出版社、原著来源、具体许可证及修改说明（例如“依据官方PDF排版转换为HTML，非出版社官方网页”），不得暗示ETSU认可或联合运营本站。
- 原书的图片、地图、照片可能具有独立许可；出版社购买的iStock图像不随正文CC BY4.0允许本站复制，也不得靠热链接绕过。逐图授权、合法替代或普通链接仍是硬门槛。
- 许可本身**不是搜索流量保证**，也不等于自动获得网站模板、Logo、商标、出版平台CSS/JS的复用权。
- 原版权说明：https://creativecommons.org/licenses/by/4.0/

## 4. 搜索与广告净收益不确定性

Google官方明确：搜索能索引PDF和HTML。PDF无法像普通章节HTML那样天然支持本站自定义目录、手机排版、交叉链接、跨locale导航、按章检索和适合阅读的脚注交互，但“HTML优于PDF”不构成算法排名保证。

- 如果只是将PDF机械切成大量几乎无额外用户价值的HTML页面，会遇到“重复内容/重新发布内容缺乏增量价值”风险。
- Google的scaled content abuse及scraping政策强调**创建大量内容主要为操纵排名而非帮助读者**是风险，而不是说任何合法CC开放教材的网页版都自动违规。
- 即使本站HTML是合法改编，Google也可能将原PDF识别为相近内容并在搜索中偏好另一份；自声明canonical只是提示，不能保证本站HTML被选为代表版本。也不建议为了避免版权问题机械给原PDF跨站canonical；要结合是否是真正独立有用页面、所需搜索可见性逐项判断。
- 目前没有独立验证的英语相关搜索量、自然点击机会、广告Page RPM或长期净收益：`UNKNOWN`。

权威资料（2026-11-06核实）：
- Google索引PDF/语义HTML：https://developers.google.com/search/docs/fundamentals/get-started-developers
- Google重复内容的规范化：https://developers.google.com/search/docs/crawling-indexing/canonicalization
- Google垃圾内容政策：https://developers.google.com/search/docs/essentials/spam-policies

## 5. 英文网页有价值的最低条件与停止线

若未来正式实施，先用**单个HIS-B章节**验证，不能在研究阶段直接重建15章：

1. **来源**：只使用已取得并冻结sha的ETSU官方PDF英文原著文本。
2. **质量**：正确恢复双栏顺序、脚注引用、表格与图片caption，核对原PDF起始与结尾段落；不把PDF页眉、页码、断行误当正文。
3. **阅读价值**：清晰的章/节目录、可用的移动端与桌面阅读宽度、章节导航、语义化标题、可点击引文、按章搜索能力；与“把PDF放进浏览器iframe”有实质区别。
4. **版权**：醒目的原作者与出处/CC BY4.0说明，图片按具体许可复用、替换或链接官方原图页面。
5. **商业**：搜索表现/RPM仍UNKNOWN；不能把英语HTML页数当作流量增长或长期利润证明。
6. **复用性**：使用未来三本书共享的最低成本阅读模板，避免为英语独立建立与其余65-locale不兼容的工程。

如果单章的结构恢复、历史排版、媒体许可修复成本明显超出复用价值，就暂缓这项例外，不为英语单独开发复杂PDF提取流水线。

## 6. 66-locale 与English host命名约束

此前研究冻结的65个Go正式生产hostname可通过替换域名中`go-dev`为`world-history`派生；额外`en-US`是研究目标范围内第66个locale，**go-dev没有对应的正式production_hostname**。

因此，如选择自建英文网页：
- **不得臆造“从go-dev直接推导的en-US正式域名”**；
- 需要另行决定英语主站hostname、对应locale标识，以及`en-GB`、`en-AU`等英国/澳大利亚英语市场若正文基本相同是否只链接主英文站以免大量同语重复页面。
- 这是**主机名的一项尚未批准例外**，不影响已经确定的65个现有Go locale原样映射。
- 不因“英语网页有效”而自动使三本教材在所有英语地区创建相同英文页面。

## 7. 有条件建议与下一步

`RESULT=PASS`
`STAGE=HIS_ENGLISH_WEB_FORMAT_GAP_EXCEPTION_ASSESSMENT`
`SECOND_PROJECT=WORLD_HISTORY`
`FORMAL_PROJECT_SELECTED=YES`
`PUBLISHED_FORMAT=WEB_ONLY`
`SOURCE_OFFICIAL_ONLY=YES`
`EXISTING_OFFICIAL_LANGUAGE_AUTOMATIC_EXCLUSION=NEEDS_FORMAT_AWARE_EXCEPTION`
`HIS_B_ENGLISH_HTML_PILOT=RECOMMENDED_CONDITIONAL`
`HIS_A_ENGLISH_DUPLICATE_PAGES=NOT_RECOMMENDED_NOW`
`HIS_C_ENGLISH_HTML=CHECK_PUBLISHER_FULLTEXT_FIRST`
`EN_US_GO_DEV_PRODUCTION_HOSTNAME=NONE`
`ENGLISH_WEB_HOSTNAME=UNDECIDED`
`ENGLISH_DUPLICATE_REGION_SITES=NOT_AUTHORIZED`
`SEARCH_TRAFFIC=UNKNOWN`
`AD_RPM=UNKNOWN`
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_ENGLISH_FORMAT_GAP_OWNER_POLICY_DECISION`

本报告提出建议，但不代替负责人确认是否接受“官方已有语言但未提供合格网页正文时，可以为该特定书/locale建立英文网页版”的例外。即便同意规则，本阶段仍只研究，不启动建站或翻译。
