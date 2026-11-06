# 世界历史：英语地区变体全覆盖与官方PDF缺少HTML时的网页例外——负责人正式决策

记录与外部核实日期：2026-11-06
阶段：HIS_ENGLISH_REGIONAL_VARIANTS_AND_WEB_GAP_OWNER_DECISION
第二项目：WORLD_HISTORY（已正式选定）
域名项目标识：world-history
状态：RESEARCH_ONLY
GO_DEV_V2_PRIORITY=UNCHANGED

## 一、正式且优先的负责人决策

2026-11-06负责人明确批准前驱提议：
> “官方只有 PDF、没有合格 HTML 时，允许建设对应语言的网页版。”

同一消息又明确要求：
> “英语网站的语言，我记得区分了国家地区的。比如说美国、英国等。我希望先判断出源语言是美国还是英国了。然后所有的英文变体皆是需要翻译的。”

从本报告起：
1. `OFFICIAL_PDF_NO_HTML_WEB_EXCEPTION=APPROVED`：对于官方只有PDF/其他非网页文件、缺少可用HTML正文的**具体语言×教材**组合，允许用出版社官方源转换为具有实际用户阅读增量的HTML网页。不是整个网站已获建站批准。
2. `ENGLISH_REGIONAL_VARIANTS=ALL_TARGETED`：英语地区变体是独立locale，不因为任何一个英语源版本的存在而排除其余英语locale。本研究**不得把多地区英语正文机械合并成en-US或en-GB**，也不得根据搜索近重复风险擅自跳过已冻结的目标英语地区。
3. **逐本识别原文英语变体**：不能简单按英语统一源，也不能仅凭出版社国家断定其作者正文一定使用英式/美式。
4. **原文locale的特殊情况**：若官方已经有相同locale合格HTML，则按原规则优先链接官方而不无意义重复翻译；若官方只有PDF，则该locale可建设原文HTML**转换/排版版**，不伪称“英语翻译成同一英语”。源原文本身不会被伪装成一份“新翻译”。
5. **其余英语地区locale**：即使已存在另一英语原文、社区译文或某源英语网页，也按负责人要求纳入正式未来地区本地化翻译与独立审核范围。地区差异应遵循实际语言习惯，不凭空篡改历史事实或造出低价值近重复内容。
6. 仍然 `TRANSLATION_SOURCE_OFFICIAL_ONLY=YES`；不从第三方社区副本做正式翻译来源，不以热链接规避图片许可。
7. `RESEARCH_ONLY=YES`：此处是语言覆盖政策决策，**未授权现在开始任何英语翻译、页面工程、DNS和部署**。

该决定**覆盖**2026-11-06此前“无需同时建立多个英语地区版本”等宽泛排除建议。原报告历史陈述保留为前驱，不再作为当前权威。

## 二、实际英语locale清单，来自go-dev官方生产身份

只读权威：
`shuijingwan/go-tour-i18n/production/identity.json`（main，blob `585ae11543b47cbc1b03908896acb4372a1ae958`），该文件正式提供65门Go生产locale，不包含en-US。

英文locale：
| locale | Go生产hostname | 未来HIS规划hostname |
| --- | --- | --- |
| en-GB | en-gb-go-dev.shuijingwanwq.com | en-gb-world-history.shuijingwanwq.com |
| en-CA | en-ca-go-dev.shuijingwanwq.com | en-ca-world-history.shuijingwanwq.com |
| en-AU | en-au-go-dev.shuijingwanwq.com | en-au-world-history.shuijingwanwq.com |
| en-IN | en-in-go-dev.shuijingwanwq.com | en-in-world-history.shuijingwanwq.com |
| en-SG | en-sg-go-dev.shuijingwanwq.com | en-sg-world-history.shuijingwanwq.com |
| en-ZA | en-za-go-dev.shuijingwanwq.com | en-za-world-history.shuijingwanwq.com |
| en-US | **Go不存在此生产locale/hostname**（研究第66门目标） | **HOSTNAME_UNDECIDED**；必须单独确定并批准，不能假称从Go生产身份推导 |

`TARGET_ENGLISH_LOCALES=7`
`GO_PRODUCTION_ENGLISH_LOCALES=6`
`ADDITIONAL_EN_US_LOCALE=1`

上述HIS域名只是按已选域名项目标识`world-history`的未来规划例子，并未创建DNS或实际网站。

## 三、三本书英语原文的变体初步核实

### HIS-A：美式英语，VERIFIED_HIGH_CONFIDENCE

出版方为美国University of North Georgia Press；其官方关联OpenALG/Manifold的第1章真实文本有美式词形`analyzed`、`recognize`等。美国出版方与实际正文拼写相互支持。

证据：
- https://ung.edu/university-press/books/world-history-cultures-states-societies-to-1500.php
- https://alg.manifoldapp.org/read/world-history/section/26bcf032-404d-4c85-9f3b-6c0cafa5cc25

`HIS_A_SOURCE_ENGLISH_VARIANT=en-US`
`HIS_A_SOURCE_VARIANT_STATUS=VERIFIED_HIGH_CONFIDENCE`

### HIS-B：美式英语，VERIFIED_HIGH_CONFIDENCE

出版方为美国East Tennessee State University；2026-11-06直接根据负责人提供的**官方PDF全233页提取正文**做了双变体拼写词汇计数，代表性结果（原PDF文字提取，**不等于复杂文体分类**）：

| 美式词形 | 命中 | 英式词形 | 命中 |
| --- | ---: | --- | ---: |
| color | 7 | colour | 0 |
| center | 15 | centre | 0 |
| labor | 57 | labour | 0 |
| organization | 15 | organisation | 1 |
| defense | 11 | defence | 0 |
| recognize | 7 | recognise | 0 |

这是原著文本而非营销页面的实证。偶见英式形式、历史专名或引文混合不改变总体判断。

PDF权威来源：https://dc.etsu.edu/etsu-oer/13/
附件文件SHA256 `fb20f23c3913fcaef68cc503a171e6debe2954775402e83b923722666721cc3b`。

`HIS_B_SOURCE_ENGLISH_VARIANT=en-US`
`HIS_B_SOURCE_VARIANT_STATUS=VERIFIED_HIGH_CONFIDENCE`

### HIS-C：英国出版社，但英语变体尚需按官方XML正文确定

原出版社为英国剑桥Open Book Publishers；其原著书目只登记`Language: English`，没有在官方书目明确指定`en-GB`，而出版社书目所在地**不能证明所有作者使用英国拼写**。

关键额外证据：Open Book Publishers的出版样式指南（针对其Studies on Mathematics Education and Society系列）**允许作者为章或书选择英式或美式**，因此不可直接把它作为该书必然英式英语的依据。
- https://www.openbookpublishers.com/books/10.11647/obp.0074
- https://www.openbookpublishers.com/series/2755-2624/style-guide

负责人刚从出版社官方页面下载到：
`~/下载/obp.0074.zip`
SHA256 `ef00fa6df2eeffa73f05188e26f07810eb21f1a327bda0875efba94345bb82f0`；
含14个可解析XML，包含`XML-edition/ch1.xml`等，抽样词103296，结构PASS。

**该官方XML目前未上传到本会话，因此在这里不捏造它的british/american用词统计。**

`HIS_C_SOURCE_ENGLISH_VARIANT=UNKNOWN`
`HIS_C_PROVISIONAL_RESEARCH_HYPOTHESIS=en-GB`
`HIS_C_SOURCE_VARIANT_PROOF=OFFICIAL_XML_LEXICAL_AUDIT_PENDING`

**必须优先只读检查XML-edition/ch*.xml中的美/英拼写词对，排除封面/参考文献/专有名称或引文后人工确认；对不明显或混合风格应标为MIXED/UNCLEAR，不能强制二选一。** 该判断影响到底应将哪一个英语locale视为源版，必须在正式翻译前冻结。

## 四、逐书逐locale的实际处理示例

| 教材 | 原文英语locale（当前证据） | 原英语locale已有HTML时 | 原英语locale只有PDF时 | 其他英语locale |
| --- | --- | --- | --- | --- |
| HIS-A | en-US | 已有官方关联HTML，原文en-US一般可继续链接官方 | 可单独评估形式缺口；未发现此缺口 | 其余6个英语变体做本地化翻译 |
| HIS-B | en-US | 如未来发现官方完整英语HTML，则重新评估 | **负责人已批准可将官方PDF原文制作英语HTML** | 其余6个英语变体做本地化翻译 |
| HIS-C | UNKNOWN；假设en-GB待查 | 官方真实HTML是否可直接阅读仍待验证 | 缺少合格英语HTML则原文locale可建设网页版 | 除实证原始英语locale外，其余英语地区均做本地化翻译 |

此处并不是限制只翻译英文；原先其他目标locale与官方有效语言覆盖规则均不变。

地区本地化可能包括：拼写与标点习惯、语法词汇、日期表达、术语及页面导航语言。历史人名、地点、年代、引文、原版史实保持准确，不得为了制造不同正文而随意替换事实。两种英语地区非常相似时可以采用严谨的locale-specific QA及轻量差异，而不是人为重写全部章节。

## 五、SEO及内容质量风险（不构成取消英语变体依据）

- 多个英语locale的内容相近，`hreflang`、明确的不同地区URL、内部语言切换、合理的规范化规则及差异化服务对搜索呈现重要；
- 不要以页面数或仅替换`color/colour`制造大量无用网页，必须提供**适合地区读者的可验证用户价值**；
- Google不保证每一地区页面都被独立收录或带来对应广告收入，重复与规范化选择需要上线后的实际数据检验；
- 用户要求每一英语变体做本地化，不因搜索策略猜测自动删除locale；
- `EN_VARIANT_ORGANIC_TRAFFIC=UNKNOWN`
- `EN_VARIANT_AD_REVENUE=UNKNOWN`。

官方文档：
https://developers.google.com/search/docs/specialty/international/localized-versions
https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

## 六、下一步唯一低成本研究证据

`NEXT=HIS_C_OFFICIAL_XML_SOURCE_ENGLISH_VARIANT_LEXICAL_GATE`

维护者在真实本地对已经取得的出版社官方XML ZIP执行**只读词形核验**，确认`HIS-C`源英语变体。只输出两组词形计数摘要及结论`en-US/en-GB/MIXED_OR_UNCLEAR`，完整结果留在`/tmp`，不对研究仓库新增源码/页面，不再重新下载任何文件。

正式政策状态：
`RESULT=PASS`
`STAGE=HIS_ENGLISH_REGIONAL_VARIANTS_AND_WEB_GAP_OWNER_DECISION`
`SECOND_PROJECT=WORLD_HISTORY`
`OFFICIAL_PDF_NO_HTML_WEB_EXCEPTION=APPROVED`
`ALL_TARGET_ENGLISH_REGIONAL_VARIANTS=IN_SCOPE`
`TARGET_ENGLISH_LOCALES=7`
`HIS_A_SOURCE_ENGLISH_VARIANT=en-US`
`HIS_B_SOURCE_ENGLISH_VARIANT=en-US`
`HIS_C_SOURCE_ENGLISH_VARIANT=UNKNOWN`
`HIS_C_SOURCE_VARIANT_HYPOTHESIS=en-GB`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`TRANSLATION_SOURCE_OFFICIAL_ONLY=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_C_OFFICIAL_XML_SOURCE_ENGLISH_VARIANT_LEXICAL_GATE`

本文件是当前新决策权威；不允许此前“只要某处存在英语原文则可以舍弃其他地区英语站”的建议覆盖它。
