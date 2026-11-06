# 世界历史三书：混合官方阅读链接与自建网页的体验和商业取舍

日期：2026-11-06
阶段：HIS_MIXED_HOSTING_VS_UNIFIED_READING_EXPERIENCE_ASSESSMENT
状态：RESEARCH_ONLY
性质：研究建议，非负责人正式批准的新政策

## 问题

三部教材针对66个目标locale分别选择内容供给。当某一书某语言已有出版方合格完整HTML时，按先前原则可链接官方；另一本或两本没有可用官方HTML时则通过官方原著制作本站网页。负责人担心跳转出版社网站破坏统一阅读体验；若全部自建又可能带来内容重复和维护成本。

HIS-C官方XML已通过8章、24/24段落样本与出版方PDF匹配；这只是抽样一致性信号，不是完全逐段等同。

## 建议：统一入口与发现体验，不强制统一正文托管

以每个`(book,locale)`单独判断。本站统一提供：书目页、书籍和语言标签、对应区域的章节发现路径、清晰指示本站阅读还是官方阅读、跨语言已有内容情况。只有官方网页存在且满足当前语言、章节完整、可直接深链、移动阅读和可用性标准时，优先指向官方全文。若只有PDF、网页不完整、不可直接导航、与所需locale不匹配，或自建具备可验证增量价值，则保留合规自建HTML选项。

用户点击外部阅读应显式标记“前往出版社阅读”；不能假装仍在本站，也不应建立66x3个只有链接的低价值空壳页。可在真正有内容价值时做原创导读/跨书历史时间线与交叉索引，但不能为了制造SEO页面做薄弱导流站。

## 目前示例en-US

- HIS-A：OpenALG Manifold已有首中末3章可读HTML，尚缺12章全覆盖核验；暂优先官方链接，不必机械复制。
- HIS-B：ETSU官方PDF已取得，但未核实到独立语义HTML；负责人已批准“官方仅PDF时允许自建网页”政策。
- HIS-C：官方XML和PDF均已取得，8章XML与PDF抽样24/24；是否存在完整可读官方英语HTML仍未解决，先核验再决定是否自建。

这些是三个书籍的差异，不是忽略七种英语locale的理由。目标英语变体：en-US,en-GB,en-CA,en-AU,en-IN,en-SG,en-ZA。其他地区按正式本地化政策保留，避免仅以一个英语原文代替其他英语地区。

## 商业与维护边界

- 若三书所有66个locale都自建，仅书级组合就有3x66=198种。如果每章一页、三本共有12+15+8=35章，理论上35x66=2310个章语言页面（实际会因官方完整覆盖而减少）；这个数量是组合数量，不是收入或访问量预测。
- 全部自建的优点是界面一致、本站PV可控、可共享章节搜索、导航和语言切换；成本是高质量翻译/版次更新、图片授权、内容QA和可能与出版社现有页面重复。
- 混合承载的优点是减少重复工作、保持出版方内容新鲜度、将精力集中在官方缺口；缺点是跨站切换、本站广告浏览机会减少、外部链接随时可能变更，以及出版社页面不一定具有相同的章节导航。
- 官方存在HTML并不等于该locale“有效完整覆盖”，应核查该书、该locale、每章质量及用户实际任务。
- Google说明重复/高度相似页面可能发生规范化选择，不能保证自建合法CC正文一定有独立自然流量；大量无新增价值的重新发布和机械翻译存在垃圾内容风险。不同地区英语可以用hreflang指示，但不保证每个地区页均获独立流量。以上属于搜索风险，不意味着法律上禁止依据已获许可原著制作HTML。

权威来源（2026-11-06核实）：
https://developers.google.com/search/docs/essentials/spam-policies
https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls
https://developers.google.com/search/docs/specialty/international/localized-versions

## 后续唯一最有价值的研究

建立轻量`BOOK_X_LOCALE_OFFICIAL_HTML_COVERAGE`事实矩阵，而不是提前生成66x3个页面。只检验官方是否有真实可读HTML、章节是否完整、该语言变体是否一致、是否支持章节深链、是否符合媒体许可证。

建议首先对en-US三本教材做极小样本的阅读路径比较（官方跳转与本站HTML候选），确认混合承载是否会产生不可接受的用户障碍，再决定是否需要任何“官网已有HTML仍自建”的例外。

```text
RESULT=PASS
STAGE=HIS_MIXED_HOSTING_VS_UNIFIED_READING_EXPERIENCE_ASSESSMENT
SECOND_PROJECT=WORLD_HISTORY
RECOMMENDATION=UNIFIED_DISCOVERY_MIXED_CONTENT_HOSTING
OFFICIAL_HTML_AUTO_REHOST=NO
LANGUAGE_VARIANTS_ALL_TARGETED=YES
HIS_C_XML_PDF_SAMPLES=24_OF_24
ORGANIC_TRAFFIC=UNKNOWN
AD_RPM=UNKNOWN
PROJECT_LAUNCH_AUTHORIZED=NO
RESEARCH_ONLY=YES
NEXT=HIS_EN_US_THREE_BOOK_OFFICIAL_HTML_READER_COVERAGE_PILOT
```
