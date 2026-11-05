# Ethereum开发者文档授权与多语言覆盖初筛 001

核实日期：2026-11-05
阶段：ETH_DEVELOPER_SOURCE_LICENSE_AND_COVERAGE_GATE
状态：RESEARCH_ONLY

候选：Ethereum Developer Learning & Documentation
目标语言：冻结的66个locale
正式项目：NOT_DECIDED

## 一、研究范围

本阶段优先调查ethereum.org官方开发者文档。

官方入口：
https://ethereum.org/developers/docs/

源仓库：
https://github.com/ethereum/ethereum-org-website

研究对象包括：

1. 开发者入门与基础概念。
2. Ethereum协议、账户及交易。
3. EVM与Gas。
4. 智能合约开发。
5. 开发工具及客户端API。
6. JSON-RPC。
7. 节点、共识与网络。
8. 开发者教程。
9. 高级开发主题。

以上是内容范围分类，
不代表已完成页面级清单。

Solidity、Vyper、Hardhat、
EIPs及其他生态项目的独立文档，
不得自动归入ethereum.org授权范围。

本阶段不研究代币投资、
价格预测或交易策略网站。

## 二、官方源码许可证

仓库：
https://github.com/ethereum/ethereum-org-website

许可证：
https://github.com/ethereum/ethereum-org-website/blob/dev/LICENSE

仓库许可证：MIT。

状态：

REPOSITORY_LICENSE=VERIFIED
SOFTWARE_LICENSE=MIT

MIT允许商业使用，
但必须遵守其许可条件。

不能仅依据仓库MIT，
推断网站所有内容、图片、
第三方资料和商标均采用MIT。

## 三、网站内容许可证

官方使用条款：
https://ethereum.org/terms-of-use

官方说明：

除另有标记外：

- 非代码内容：CC BY 4.0。
- 软件及代码：MIT。

状态：

DEFAULT_NON_CODE_LICENSE=CC_BY_4_0_VERIFIED
DEFAULT_CODE_LICENSE=MIT_VERIFIED

CC BY 4.0：
https://creativecommons.org/licenses/by/4.0/

CC BY 4.0原则上允许商业改编，
包括翻译与再分发。

应提供适当署名、
许可证链接及修改说明，
不得暗示官方认可独立网站。

但仍须检查具体文件
是否具有例外许可、
第三方权利或额外限制。

## 四、网站使用条款风险

同一官方使用条款还规定：

- 网站访问者限于个人用途。
- 对自动访问与复制存在限制。
- 官方商标另有保护。

因此必须区分：

1. 内容本身的开放许可证。
2. 访问ethereum.org的网站服务条款。
3. 从GitHub取得源文件的条件。
4. 独立托管、翻译和广告变现。
5. 官方名称、Logo及商标使用。

不能将CC BY直接视为
网站所有使用方式已获批准。

状态：

CONTENT_LICENSE_COMPATIBILITY=VERIFIED_DEFAULT
SITE_ACCESS_TERMS_CONFLICT=UNCLEAR
INDEPENDENT_AD_HOSTING_CLEARANCE=UNCLEAR
THIRD_PARTY_ASSETS=UNCLEAR
TRADEMARK_CLEARANCE=UNCLEAR

下一阶段必须进一步核实
网站条款与开放许可证的适用边界。

不得通过违反网站访问条款的
批量抓取来取得研究材料。

## 五、开发者文档源码范围

仓库技术文档：
https://github.com/ethereum/ethereum-org-website/blob/dev/docs/stack.md

相关目录包括：

public/content/developers/docs

public/content/developers/tutorials

这些目录分别对应
开发者文档与教程内容。

但仍需核实：

- 当前仓库的实际文件清单。
- 页面与源文件的对应关系。
- 外部转载、嵌入及第三方素材。
- 文件级许可证例外。
- 文档更新频率。

状态：

SOURCE_REPOSITORY=VERIFIED
SOURCE_PATH_DESCRIPTION=VERIFIED
CURRENT_FILE_INVENTORY=UNKNOWN
FILE_LEVEL_RIGHTS_AUDIT=INCOMPLETE

## 六、官方多语言覆盖

官方翻译项目：
https://ethereum.org/contributing/translation-program/

截至本次核查，
官方翻译项目页面说明：

- 已有68种语言上线。
- Crowdin完整页面翻译计划正在收尾。
- 不再通过Crowdin接受新翻译提交。
- 既有翻译仍保留在网站上。

状态：

TRANSLATION_PROGRAM_STATUS=VERIFIED
REPORTED_LIVE_LANGUAGES=68
FULL_PAGE_TRANSLATION_INTAKE=PAUSED

此前观察到的网站语言下拉
约25种语言。

这与官方历史累计
68种语言上线的统计口径不同。

不能认定二者互相矛盾，
也不能将任一数字直接当成
完整开发者文档覆盖数量。

ACTIVE_LANGUAGE_COVERAGE=UNKNOWN
EXACT_DEVELOPER_DOC_COVERAGE=UNKNOWN

## 七、同源覆盖抽样

简体中文：
https://ethereum.org/zh/developers/docs/

德语：
https://ethereum.org/de/developers/docs/

英语原文：
https://ethereum.org/developers/docs/

本次确认中文、德文
开发者文档入口可访问，
并显示相应语言内容。

状态：

ZH_DEVELOPER_ENTRY=VERIFIED
DE_DEVELOPER_ENTRY=VERIFIED

但没有完成逐页面、
逐章节、逐版本对照。

因此：

ZH_COMPLETE_COVERAGE=UNKNOWN
DE_COMPLETE_COVERAGE=UNKNOWN
TRANSLATION_FRESHNESS=UNKNOWN

这些页面是直接的
官方同源翻译竞争信号。

不得因为页面存在，
就认定开发者文档
已在对应语言中完整覆盖。

## 八、66个目标语言

沿用仓库现有的
66-locale来源快照。

不得修改语言顺序。

继续区分：

- 62个广告支持locale。
- 4个广告不支持locale。

这属于既有项目范围约束，
不是本轮重新测量结果。

不要求本阶段逐一调查
全部66种语言。

重点是建立能够扩展的
同源页面覆盖验证方法。

## 九、搜索竞争

主要直接竞争者：

ethereum.org官方多语言文档。

竞争优势包括：

- 官方主域名。
- 社区贡献体系。
- 已有翻译积累。
- 开发者入口整合。
- 原始内容维护来源。

潜在差异化方向：

- 官方未完整覆盖的语言。
- 缺少更新的译本。
- 更完整的开发学习路径。
- 跨版本对照与维护记录。
- 原始文档与译文的术语一致性。

这些目前只是研究假设。

SEARCH_VOLUME=UNKNOWN
ORGANIC_TRAFFIC=UNKNOWN
EFFECTIVE_LANGUAGE_GAP=UNKNOWN
COMPETITIVE_ADVANTAGE=UNKNOWN

## 十、长期维护风险

Ethereum开发资料
存在较高的上游变化风险。

需要特别关注：

- 协议升级。
- EVM及执行层变化。
- 共识层变化。
- JSON-RPC及客户端行为。
- 智能合约安全实践。
- 开发框架及工具变化。

不能把所有内容
视为长期静态知识。

应将稳定基础概念
与快速变化的开发资料分开。

UPDATE_COST=UNKNOWN
TECHNICAL_REVIEW_COST=UNKNOWN

## 十一、广告商业价值

研究目标仍然是：

LONG_TERM_AD_NET_PROFIT

目前尚无足够证据证明：

- 可获取的自然搜索访问量。
- 多语言有效搜索缺口。
- 用户持续访问频率。
- 广告Page RPM。
- 维护成本后的净收益。

上述全部为UNKNOWN。

不能将Ethereum市场规模、
交易金额或加密资产价格，
用作开发文档广告收益预测。

## 十二、初筛结论

ETH_STATUS=RESEARCH_CONTINUE

SOURCE_LICENSE=PARTIALLY_VERIFIED

DEFAULT_CONTENT_LICENSE=CC_BY_4_0_VERIFIED

CODE_LICENSE=MIT_VERIFIED

COMMERCIAL_HOSTING_TERMS=UNCLEAR

OFFICIAL_TRANSLATION_COMPETITION=VERIFIED

EXACT_FULL_TRANSLATION_COVERAGE=UNKNOWN

ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN

NET_AD_PROFIT=UNKNOWN

FORMAL_PROJECT_SELECTED=NO

SECOND_PROJECT=NOT_DECIDED

不能因官方翻译计划收尾，
就推断独立多语言网站
一定具有商业机会。

也不能因为官方已有
大量翻译，就自动淘汰ETH。

现阶段保留候选，
不批准正式开发。

## 十三、下一阶段

NEXT=ETH_TERMS_AND_SOURCE_EQUIVALENT_COVERAGE_PILOT

优先解决两个问题：

1. 官方网站使用条款与
   CC BY开放许可之间，
   对商业独立托管是否存在
   实质性限制或需要澄清。

2. 抽样比较英语、中文、
   德语等开发者资料，
   确定实际同源章节覆盖、
   译文完整性与更新时间。

先解决授权不确定性。

若商业独立托管不能获得
清晰、合法的授权依据，
应停止继续投入深度SEO研究。

如授权边界可明确，
再调查语言缺口与搜索需求。

保持RESEARCH_ONLY。

不启动翻译。
不建设网站。
不购买域名。
不修改go-dev v2。
