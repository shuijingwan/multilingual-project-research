# Shopify、Ethereum、DeepSeek 合法内容子集价值横向复评 001

核实日期：2026-11-06
阶段：LICENSED_SUBSET_VALUE_SIDE_BY_SIDE_REVIEW
状态：RESEARCH_ONLY
商业目标：LONG_TERM_AD_NET_PROFIT，同时考虑多语言内容新增价值
第二正式项目：NOT_DECIDED

## 一、政策及研究边界

沿用2026-11-03已确立、2026-11-06再次确认的：
`LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`。

- **只翻译明确获得商业翻译、改编、独立再分发许可的文件或文字**。
- 许可不明确、不允许商业再分发或不具备合法获取路径的内容：官网外链，不复制。
- **不需要取得整站授权**，不要求原创编写教程补齐未授权内容。
- 社区已有同源完整译本**不能排除目标locale**；只在立项前影响重复劳动与内容增量价值的判断。
- 66个目标locale固定；对于各项目，官方实际有效支持的语言须在指定来源/模块级核实，不能根据语言菜单机械相减。
- 评估的是本站合法可提供的内容及其用户价值，不把外部官方网页算作本站PV。

本轮目标是**在三个具体候选之间**比较；不构成与世界历史、Rust、OWASP、Python、GEO/DATA等全部候选的最终商业排名。

本轮新增只读数据来自公开GitHub仓库内容与Shopify/Ethereum官方条款，未进行批量文件级许可审计、源文件导入或建站。

## 二、内容级证据（较此前多了一层实际内容量核查）

### 2.1 Shopify：已确立的可用合法子集规模

先前报告已经核实下列官方GitHub仓库根目录MIT许可证及具体源版本（注意：本轮未逐文件排除全部第三方例外）：

1. `Shopify/theme-liquid-docs`
2. `Shopify/shopify-app-js`
3. `Shopify/hydrogen`
4. `Shopify/cli`
5. `Shopify/theme-extension-getting-started`
6. `Shopify/shopify-ai-toolkit`

依据：
`research/2026-11-04-shopify-licensed-vs-external-module-coverage-001.md`

**2026-11-06新抽样：** 直接读取当前GitHub公开源码目录，解析三份JSON及目录文件，不依赖前期截图。

| 具体文件/目录 | 可见范围 | 内容信号 | 当前报告使用方式 |
| --- | ---: | --- | --- |
| `theme-liquid-docs/data/filters.json` | 155条 | 155有summary；245个examples | Liquid过滤器可检索参考 |
| `theme-liquid-docs/data/objects.json` | 142条 | 142有summary；38个examples | Liquid对象可检索参考 |
| `theme-liquid-docs/data/tags.json` | 33条 | 33有summary；60个examples | Liquid标签可检索参考 |
| `shopify-app-js/packages/apps/shopify-api/docs/guides/` | 10个MD文件 | OAuth、Billing、Webhooks、Session Storage等 | 部分真实开发指南 |

前三份JSON累计**330条**独立参考记录（155+142+33），示例累计343个（245+38+60）。样本并非整个项目源资料总规模。

核查路径与源文件SHA：
- https://github.com/Shopify/theme-liquid-docs/blob/main/data/filters.json  — blob SHA `c34f2e0cea8184601c562312edc6b75b97cbfa36`
- https://github.com/Shopify/theme-liquid-docs/blob/main/data/objects.json
- https://github.com/Shopify/theme-liquid-docs/blob/main/data/tags.json
- https://github.com/Shopify/shopify-app-js/tree/main/packages/apps/shopify-api/docs/guides
- OAuth指南sample blob SHA `558f2687a914cf57e4119efdbdc6b27a9ca7a977`

**解释限制：**
- JSON记录不是330篇有自然搜索价值的独立页面，不能机械创建大量低价值薄页面。
- 343个examples也不能直接等于343个完整、能运行的学习练习。
- 部分数据属于引导参考、代码或技术标识，真正可翻译的自然语言比例未测量。
- 10个Markdown并不能证明一个覆盖Apps开发全生命周期的课程。
- 源代码根MIT不是所有外部引用、第三方插图、商标和未核实生成文件的再分发许可。
- Shopify每季度发布API版本；Liquid等未版本化接口可能随时更新，不能把JSON参考当作永远不变。官方版本政策：https://shopify.dev/docs/api/usage/versioning

判断：
`LICENSED_SOURCE_CONTENT_SIGNAL=VERIFIED_IN_SAMPLE`
`PRACTICAL_REFERENCE_SUBSET=PARTIALLY_VERIFIED`
`ENTIRE_LEARNING_PATH_COMPLETENESS=UNKNOWN`
`FILE_LEVEL_ASSET_RIGHTS=PARTIALLY_AUDITED`

### 2.2 Ethereum：源内容结构广，合法使用子集尚无法估算

公开GitHub源目录：

https://github.com/ethereum/ethereum-org-website/tree/dev/public/content/developers/docs

2026-11-06读取目录：当前顶层共有31个项目（30个目录 + 1个index.md）；覆盖账户、API、EVM、Gas、合约、共识、网络、扩容等方向。**这是目录项，不是文档总篇数或合法页数。**

样本：
- `public/content/developers/docs/gas/index.md`：实际Markdown正文约13K字符，含图片，blob SHA `a9e1da3ee2e2ceae9a507c4db2fc7106f6bccbf9`。
- `public/content/developers/docs/intro-to-ethereum/index.md`：之前报告已核查实际英文正文和中德官网译文。

官方来源：
- https://ethereum.org/terms-of-use/
- https://github.com/ethereum/ethereum-org-website

内容默认：非代码CC BY 4.0、代码MIT，前提是具体内容无另行标记。CC BY允许符合条件的商业改编，但当前网站访问条款、从GitHub取得内容的法律适用、第三方图示/视频及商标边界曾被前驱研究标为UNCLEAR。

**严格应用混合授权规则：** 已有CC BY权利依据的具体文字可以进入进一步白名单审核；凡文件级权利或获取路径仍存实质争议者暂不算“已安全可发布的白名单”。不能把整站版权或某张插图的不确定性解释成这个候选整体不能比较；也不能把理论上许可开放理解为所有网页都可直接独立发布广告。

官方已核实部分中文与德文同源正文；但完整开发者源范围的各locale覆盖率、官方维护责任及重复翻译规模均UNKNOWN。

判断：
`SOURCE_CONTENT_STRUCTURE=VERIFIED_IN_SAMPLE`
`DEFAULT_TEXT_LICENSE=VERIFIED_CONDITIONAL`
`PUBLISHABLE_WHITELIST_EXACT_SCOPE=UNKNOWN`
`TERMS_AND_THIRD_PARTY_EXCEPTIONS=UNCLEAR`
`OFFICIAL_TRANSLATION_COMPETITION=VERIFIED_IN_SAMPLE`

### 2.3 DeepSeek：源仓库真实，但已核实的阅读型内容规模有限

已核实的具体开源来源：https://github.com/deepseek-ai/DeepSeek-R1

2026-11-06读取仓库根目录（main）：

- `README.md`：单份英文Markdown，读取约19.4K字符；blob SHA `40d1af36fdb96e26129527b0531bb3ac195f6713`。
- `DeepSeek_R1.pdf`：研究论文PDF，需**独立核实论文/第三方引用/图片的实际版权范围**，不自动视为MIT正文。
- `figures/`：素材目录，需逐项核实。
- `LICENSE`：MIT，blob SHA `d42fae903e9fa07f3e8edb0db00a8d905ba49560`。
- 还有`.github/`，不代表面向学习者的完整文档。

当前仓库README包括模型说明、使用/部署/下载提示等；**这是面向某个模型的技术说明，不能等同于整套DeepSeek API开发文档**。

具体官方API文档：https://api-docs.deepseek.com/
API网页文字的完整商业再分发许可尚未确定，按规则应外链，不翻译复制。

前驱：`research/2026-11-03-source-license-screening.md`

判断：
`SOURCE_SPECIFIC_MIT_LICENSE=VERIFIED`
`MODEL_REPO_README_CONTENT=VERIFIED`
`LICENSED_HUMAN_LEARNING_CORPUS_COMPLETENESS=NOT_VERIFIED`
`API_DOC_TRANSLATION_RIGHTS=UNCLEAR`
`OTHER_DEEPSEEK_REPOSITORIES_NOT_EXHAUSTIVELY_AUDITED=YES`

不可用单个R1仓库内容少就断言“整个DeepSeek生态不存在开放且丰富的教材”。

## 三、共同的业务对照（本轮定性比较）

| 维度 | Shopify合法子集 | Ethereum合法候选子集 | DeepSeek现有核实子集 |
| --- | --- | --- | --- |
| 具有实际阅读或查询价值的源内容 | 多个JSON参考与实际MD指南，部分验证 | 多主题实际MD开发文档，部分验证 | 一个较长README与其他非同权素材 |
| 明确源许可基础 | 6个MIT仓库（文件级例外仍审） | 官方默认CC BY正文，个别来源/访问条款需审 | 指定MIT仓库README等，PDF等另审 |
| 现有可核实内容体量 | 330 Liquid条目 + 10 MD指南为**部分样本** | 30目录+index，**不能当作页面数** | R1样本1 README；不能代表整个生态 |
| 是否形成完整本站教程 | UNKNOWN；合法外链可补导航 | UNKNOWN；部分材料需排除 | NOT_VERIFIED；大量API官网内容可能只适合外链 |
| 当前多语言同源重复 | UNKNOWN；未以统一locale完成覆盖 | 已见官网中文、德文部分正文；整体UNKNOWN | README及相似技术文档语言覆盖UNKNOWN |
| 维护负担 | API季度发布、Liquid可能随时变化 | 协议与开发工具升级 | 模型/API变更速度与版本一致性 |
| 可获取自然搜索流量 | UNKNOWN | UNKNOWN | UNKNOWN |
| 长期AdSense净收益 | UNKNOWN | UNKNOWN | UNKNOWN |

### 关键评价

**Shopify在三者中具有更明确的“合法来源内可直接转化为结构化参考的内容证据”。** 这是相对样本证据强度，不是收入排序。

Ethereum可能拥有更大且更完整的原始开发者文档范围，但**能无歧义进入本站翻译的具体文件集尚未冻结**；应标记为高潜在内容范围、实际可发布白名单UNKNOWN，而不是把全站授权视为继续研究的前置条件。

DeepSeek目前核实的R1开源README不够支持“完整API文档翻译站”的已验证论证；可以转向更多**明确可商用的源仓库说明**做有限补查，但不因名称热度扩展无尽仓库清单。

**注意研究深度偏差**：Shopify已经调查六个源码仓库、Ethereum多个文档主题，DeepSeek只审过R1样本；不得将内容体量样本排序冒充整个生态真实规模排名。

## 四、内容稀缺性与66语言

对三个项目均执行：
- 66个目标locale固定，**只排除已在指定项目全部正式来源范围内获得有效官方支持的locale**；若官方只支持局部，项目级排除不可机械成立。
- 社区译本即使完整，若项目最终选中仍重新翻译对应locale；竞争只降低立项前的内容增量评价。
- Shopify部分官方营销/商家帮助有多语言内容，不等于其可翻译源仓库已有完整官方多语。
- Ethereum历史语言数、官网当前语言菜单均不是完整开发者资料的语言数。
- DeepSeek官方API中英说明与R1开源说明不是同一个权利和内容对象。
- **没有任何一个候选能据当前证据严谨算出66减官方语言的确切值**。

新增知识可及性：本轮均为`UNQUANTIFIED`，不得因为“尚未发现译文”而标为已确认高稀缺。

## 五、决定性停止线与下一步

对三个候选现在可以作出有限项目级判断：

1. **SHP：CONDITIONAL_POSITIVE_RESEARCH_PRIORITY**。存在实质合法内容主体线索，但能否由330条结构化数据和其他指南形成对读者有用、可被自然搜索访问的整体仍UNKNOWN。下一次只有文件例外审计或正式启动范围界定时才值得核查更细。
2. **ETH：RESEARCH_ELIGIBLE_LEGAL_SUBSET**。需要给拟纳入的文字建立明确且合法的获取/再分发白名单；不要求整站授权。暂不把该子集的SEO/收入当成已知。
3. **DEEPSEEK：SOURCE_SUBSET_THIN_IN_CURRENT_SAMPLE**。合法仓库技术材料存在，但本轮已核实的人类阅读型源较少；若继续研究，应先找一个更丰富的明确授权内容源，避免重复调查API官网授权。

目前没有证据授予三者中的任意一个正式建设批准。政策允许接受低于go.dev的收益，但不能将已授权数量等同于广告用户规模。

`POLICY=LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`
`WHOLE_SITE_LICENSE_REQUIRED=NO`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`SHOPIFY_LIQUID_ITEMS=330`
`SHOPIFY_APP_JS_GUIDES=10`
`ETH_TOP_LEVEL_DOC_DIRECTORIES=30`
`DEEPSEEK_R1_ROOT_READMES=1`
`SHP_SUBSET_VALUE=CONDITIONAL_POSITIVE_SIGNAL`
`ETH_SUBSET_VALUE=UNKNOWN`
`DEEPSEEK_SUBSET_VALUE=NOT_VERIFIED_IN_SAMPLE`
`ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN`
`AD_PAGE_RPM=UNKNOWN`
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`
`FORMAL_PROJECT_SELECTED=NO`
`SECOND_PROJECT=NOT_DECIDED`
`RESEARCH_ONLY=YES`
`NEXT=ALL_CANDIDATES_CONDITIONAL_SELECTION_DECISION`

下一项工作应把**这三个候选的合法内容子集研究结果放回全部候选池**，基于已确认授权、非重复知识增量、维护成本及可接受的商业不确定性，进行一次有条件、可回退的项目选择建议。不要继续把全站许可作为阻碍，也不要为了避免做决定而不断要求更多关键词数据。

不翻译、不建站、不购买域名、不部署、不修改go-dev v2。
