# 真实用户未满足工作流证据试点 001

核实日期：2026-11-06
阶段：USER_REPORTED_UNMET_WORKFLOW_EVIDENCE_PILOT
状态：RESEARCH_ONLY
商业目标：LONG_TERM_AD_NET_PROFIT
第二正式项目：NOT_DECIDED

## 一、目的、范围及方法

前驱：
- `research/2026-11-06-cross-domain-e3-differentiation-gate-001.md`
- `research/2026-11-05-hist-date-intent-gap-stop-pilot-001.md`
- `research/2026-11-06-cross-domain-demand-evidence-synthesis-001.md`

本轮不再凭空设想用户任务，抽样寻找已有公开、可追溯的第一人称实际问题，比较现有公开解决方案，判断其是否意味着独立多语言内容/工具网站机会。

分别标记：
1. USER_REPORTED_PROBLEM：用户本人表达的困难（不等于客观软件缺陷已复现）。
2. CURRENT_SUPPLY：截至本轮可核实的竞争方案。
3. UNMET_NEED_AFTER_SUPPLY：问题是否仍未得到解决。
4. SEARCH_DEMAND：是否有可信、与问题相符的搜索需求量。
5. WEBSITE_BUSINESS_CASE：能否作为具有独立可获取流量的合法广告网站。

本轮只调查两个任务：家谱旧式日期核对与 AI API 错误排查。样本不是全部候选领域的市场排名。

## 二、任务 A：家谱研究中的旧式日期保留、转换与校验（HIST_DATE）

### 2.1 真实用户报告

Reddit r/Genealogy，2025-04-30：

https://www.reddit.com/r/Genealogy/comments/1kbl3q0

一名家谱研究者比较 1738—1739 年相关遗嘱日期时，描述多个日历转换结果不一致、部分计算器可能遗漏英国旧式年份从3月25日开始的规则，并请求更可靠的转换来源。

**证据含义**：用户明确报告具体任务与转换疑惑。其指出「Google AI 和多个计算器错误」是用户的实际说法；本轮**没有独立复现**全部被指控网站的错误，不可将其一概标为 VERIFIED BUG。

Reddit r/Genealogy，2024-03-08：

https://www.reddit.com/r/Genealogy/comments/1b9lpfn

用户报告原始教区记录与 Ancestry 记录采用不同日期表达，担心保留原始日期会令后续读者困惑；2024-11-07 有参与者明确表示希望能在家谱记录里同时保留旧式与新式日期。

Reddit r/Genealogy，2024-09-21：

https://www.reddit.com/r/Genealogy/comments/1fltm94

用户讨论俄罗斯帝国1893年受洗记录应保持旧式日期还是转换；不同参与者建议在原始记录与新式日期之间保留明确标识。

结论：
- USER_REPORTED_PROBLEM=VERIFIED
- SPECIFIC_WORKFLOW=SOURCE_DATE_PRESERVATION_AND_CROSS_CALENDAR_COMPARISON
- INDEPENDENT_BUG_REPRODUCTION=NOT_DONE
- LONG_TERM_SEARCH_VOLUME=UNKNOWN

### 2.2 现有解决方案

截至 2026-11-06 的公开网页：

1. The Old Reckoner：英国旧历转新历、3月25日年初选择、双年份说明、原始写法/年份规范化/公历三形式示例；页面说明 2026-10-20 更新。
   https://theoldreckoner.co.uk/old-style-new-style/
2. TNAADO：双向历法转换、英国旧式年份选项及双年份处理。
   https://tools.tnaado.ca/calculators/general/old-style-new-style-date-converter/
3. FreeREG：针对家谱登记的双年份书写指导。
   https://www.freereg.org.uk/information-for-transcribers/numbers-and-dates
4. Family Historian 用户组：已有双年份的输入与资料说明。
   https://www.fhug.org.uk/kb/kb-article/historical-date-formats/

这些页面说明历史文献原始日期保留和双年份解释已存在可用竞争解决方案，但**没有对所有转换输入执行端到端测试**，更没有核实其搜索点击量。

### 2.3 结果

- SPECIFIC_USER_PROBLEM=VERIFIED
- CURRENT_SOLUTIONS=VERIFIED
- FULL_FUNCTIONAL_QA=NOT_DONE
- UNMET_NEED_AFTER_SUPPLY=NOT_VERIFIED
- INDEPENDENT_WEBSITE_VALUE=NOT_VERIFIED
- ORGANIC_TRAFFIC=UNKNOWN
- AD_RPM=UNKNOWN
- DECISION=KEEP_HIST_DATE_DEEP_DIVE_PAUSED

不能仅因真实用户曾经抱怨，就推断 2026 年仍没有解决方案。

## 三、任务 B：AI API 限流/配额错误诊断（AI_ERROR）

### 3.1 公开问题报告

2026-08-19 起的 GitHub `deepseek-ai/deepseek-harness` 讨论：

https://github.com/deepseek-ai/deepseek-harness/discussions/3338

用户报告在特定 OpenAI-compatible gateway/relay 情况下，HTTP 429 错误被适配器归类为不可重试的 QUOTA，导致请求终止；后续讨论包含配置层处理方案与代码层建议。

2026-08-18 起的讨论：

https://github.com/deepseek-ai/deepseek-harness/discussions/3128

用户报告某适配器没有传递服务器 `Retry-After` 头，因而过早重试；讨论聚焦 SDK/框架内的重试机制。

2026-10-04 的 DeepSeek-V3 Issue：

https://github.com/deepseek-ai/DeepSeek-V3/issues/1693

用户报告特定文本经主页转到 Chat 时发生异常限流，并提供复现步骤。此例是 Chat 网站/跳转行为，**不属于 API 429 SDK 问题**，不得合并计算为一个产品需求。

### 3.2 关键分类

这些是具体、可追溯的第一人称错误报告；其所述根因或普遍性未由本项目独立验证。

- 客户端/SDK 状态分类错误，优先由相关软件维护者修复。
- `Retry-After` 丢失属于适配器或网络接口实现问题，而不只是缺少文档翻译。
- Chat 站点的输入触发限流属于供应商自身产品问题。
- 没有证据证明上述用户会转向独立的多语言广告内容网站解决这些问题。
- 不因仓库名称、模型权重许可证或开放接口自动推定官方文档具有商业翻译再分发许可。

状态：
- USER_REPORTED_API_ERRORS=VERIFIED
- SPECIFIC_ROOT_CAUSES=REPORTED_NOT_INDEPENDENTLY_REPRODUCED
- SUITABLE_SOLUTION_CHANNEL=UPSTREAM_FIX_OR_PROVIDER_DOCS
- MULTILINGUAL_CONTENT_SITE_GAP=NOT_VERIFIED
- SEARCH_VOLUME=UNKNOWN
- OFFICIAL_DOC_REUSE_RIGHTS=UNCLEAR
- MAINTENANCE_COST=UNKNOWN
- DECISION=DO_NOT_LAUNCH_AI_ERROR_SITE

## 四、交叉分析：真实抱怨与网站机会的差别

| 检查项 | HIST_DATE | AI_ERROR |
| --- | --- | --- |
| 第一人称真实问题 | VERIFIED | VERIFIED |
| 可见现有解决方案 | VERIFIED | 存在上游修复与配置工作流 |
| 独立多语言网站必要性 | NOT_VERIFIED | NOT_VERIFIED |
| 具体搜索规模 | UNKNOWN | UNKNOWN |
| 可获取自然流量 | UNKNOWN | UNKNOWN |
| 长期广告净收益 | UNKNOWN | UNKNOWN |

真实用户报告解决了「这是不是研究者想象出来的需求」的问题，但没有自动解决「用户会不会 Google 搜索」「已有网页是否已满足」「新网页是否能排名」或「广告能否覆盖维护成本」。

注意时间维度：2024/2025 年的抱怨不能证明 2026 年竞争工具仍然缺失；软件错误也可能在后续版本修复，不能把一次问题当作长期稳定内容资产。

## 五、停止线和下一轮选择原则

本轮没有取得能够恢复 HIST_DATE 或启动 AI_ERROR 的 E3 新证据。

- USER_REPORTED_PAIN_EVIDENCE=VERIFIED_IN_SAMPLE
- E3_UNMET_NEED=NOT_VERIFIED
- E3_INDEPENDENT_VALUE=NOT_VERIFIED
- ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
- LONG_TERM_AD_NET_PROFIT=UNKNOWN
- FORMAL_PROJECT_SELECTED=NO
- SECOND_PROJECT=NOT_DECIDED

**停止沿已暂停候选不断搜集边际相似的评论。**

下一轮只有在能找到具备以下全部要素的线索时，才开展单一任务的深入验证：

1. 最近仍反复出现、不同用户独立报告的同一类问题。
2. 至少两项明确竞争方案经对照仍不能满足核心步骤。
3. 该问题更适合独立查询/内容/工具网站，而非现有软件维护者修复。
4. 存在可验证的搜索意图及可能重复使用的页面价值。
5. 所需内容或数据权利可确认，更新维护可控。

缺少这些条件时，报告 `NO_QUALIFIED_TASK`，不要因为研究仓库需要连续提交而强行选择开发目标。

## 六、后续建议

`NEXT=CROSS_DOMAIN_DISCOVERY_STOP_OR_REOPEN_DECISION`

下一步用现有所有停止线与本轮用户问题证据做**一次短决策**：是否出现符合继续专项调查的候选；没有则建议暂缓本研究项目的主动扩张，把精力留给当前主项目的正常上线与真实 SEO 数据观察。

保持 RESEARCH_ONLY；不翻译、不建站、不购买域名、不改 go-dev v2。
