# 跨领域搜索需求证据门槛 001

核实日期：2026-11-05
阶段：CROSS_DOMAIN_SEARCH_DEMAND_EVIDENCE_GATE
状态：RESEARCH_ONLY

商业目标：LONG_TERM_AD_NET_PROFIT
目标语言：冻结66个locale
正式项目：NOT_DECIDED

## 一、问题定义

此前调查多个候选领域：

- Rust
- Python
- OWASP
- Shopify
- Ethereum
- 世界历史
- 地理及数据工具
- 历史日期核对

已经积累许可证和竞争证据。

但是多项研究反复出现：

SEARCH_VOLUME=UNKNOWN
ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
AD_PAGE_RPM=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN

因此先改进商业证据方法，
暂时不增加新的正式项目候选。

本阶段只建立可执行的证据门槛，
不声称已经取得搜索量实测数据。

## 二、Bing Keyword Research

官方来源：

https://www.bing.com/webmasters/help/keyword-research-628070b6

Bing Webmaster Tools：

https://www.bing.com/webmasters/

官方说明该工具可以提供：

- 关键词搜索量。
- 搜索趋势。
- 相关关键词。
- 问题关键词。
- 地区和语言筛选。
- 最近六个月内的时间范围。
- 搜索结果中的前十URL。

状态：

BING_KEYWORD_TOOL=VERIFIED
BING_VOLUME_CAPABILITY=VERIFIED

但本阶段尚未登录账号
或取得实际关键词数据。

BING_KEYWORD_DATA=NOT_COLLECTED
ACCOUNT_ACCESS=NOT_TESTED

Bing搜索量不能直接
等同于Google搜索量。

不能自行乘以某个固定系数
推算Google自然搜索流量。

## 三、Google Keyword Planner

官方来源：

https://support.google.com/google-ads/answer/7337243

官方提供：

- 平均月搜索量。
- 关键词建议。
- 地理位置筛选。
- 历史趋势与广告预测。

Google Ads账号需要完成
相应设置及账单信息填写。

本研究不为查看数据
自动启动广告活动或付款。

状态：

GOOGLE_KEYWORD_PLANNER=VERIFIED
ACCOUNT_ACCESS=NOT_TESTED
GOOGLE_KEYWORD_VOLUME=NOT_COLLECTED

注意：

广告点击预测不等于
新建内容网站的自然搜索点击。

关键词搜索量也不等于
可获取的网站访问量。

## 四、Google Trends

官方说明：

https://support.google.com/trends/answer/4365533

Google Trends属于
归一化的相对搜索兴趣数据。

数值范围0至100。

它不能直接提供
关键词的绝对月搜索次数。

低搜索量可能显示为0，
部分低量数据可能受抽样噪声影响。

状态：

RELATIVE_SEARCH_INTEREST=VERIFIED
ABSOLUTE_VOLUME_FROM_TRENDS=NOT_AVAILABLE

此前已完成德国市场试点：

research/2026-11-03-google-trends-search-interest-pilot-001.md

该报告包含：

- 60个月连续数据。
- 五个关键词。
- 德国市场。
- 同批次相对比较。

本阶段复用历史证据，
不重新开展相同Trends调查。

## 五、Google Search Console

官方来源：

https://developers.google.com/search/docs/monitor-debug/search-console-start

Search Console提供
已验证站点的搜索表现：

- 展示次数。
- 点击次数。
- CTR。
- 搜索查询。
- 页面和国家维度。

现有go-dev项目的真实数据，
可用于观察已有网站
如何从搜索曝光获得点击。

但不能直接推断
其他主题的新网站也能取得相同表现。

状态：

OWN_SITE_PERFORMANCE_SOURCE=VERIFIED
CROSS_PROJECT_TRANSFERABILITY=NOT_VERIFIED

如果未来使用实际项目数据，
需要明确网站、语言、
查询、日期和页面范围。

不得将统计来源不明的PV
冒充自然搜索点击。

## 六、证据分级

### E0：只有用户任务设想

例如某个工具可能有用。

状态：

DEMAND=UNKNOWN

不能据此批准项目。

### E1：公开搜索兴趣或需求线索

例如Google Trends、
论坛问题、已有相关工具。

状态：

DEMAND_SIGNAL=PARTIAL

不能推断绝对市场规模。

### E2：可复核的关键词搜索量

至少记录：

- 搜索引擎。
- 完整关键词。
- 地区。
- 语言。
- 设备。
- 时间范围。
- 数值及单位。
- 数据来源。
- 获取日期。

可以确认特定查询的
搜索需求规模估算或观察值。

但不代表新站能够获得点击。

### E3：独立竞争机会

需要记录：

- 搜索结果主要竞争者。
- 官方网站覆盖。
- 成熟工具及内容覆盖。
- 用户任务未满足的部分。
- 搜索意图与预期页面匹配程度。
- 多语言市场差异。

不得将竞争者存在
直接认定为机会不存在。

也不得把某个细小功能差异
当成商业优势已经成立。

### E4：可获取自然流量

需要具有依据的：

- 搜索需求规模。
- 搜索结果竞争。
- 可能获得的展示和点击。
- 实际可用的点击率证据。
- 搜索结果直接回答影响。
- 其他关键流量限制。

若缺少关键数据，
继续使用UNKNOWN。

不编造新网站CTR。

### E5：长期广告净收益

需要进一步取得：

- 可获得的自然访问量。
- 页面浏览量。
- 适用地区的Page RPM。
- 广告可用性。
- 托管及运行费用。
- 维护和内容审核成本。

Google AdSense官方说明：

https://support.google.com/adsense/answer/112030

Page RPM =
Estimated earnings / Page views × 1000

该公式用于实际广告指标。

不能在缺少RPM与PV时
计算出可靠的广告收入。

## 七、第一轮实际数据试点

选择德国市场：

COUNTRY=DE
LANGUAGE=de
DEVICE=ALL

理由：

已经存在德国Google Trends
历史研究证据。

可以在相同国家背景下
取得另一种搜索需求证据。

优先使用Bing Keyword Research。

候选关键词：

1. Python lernen
2. Geschichte lernen
3. Julianischer Kalender umrechnen
4. gregorianischer julianischer Kalender
5. historische Datumsberechnung

前三个覆盖：

- 编程学习。
- 历史学习。
- 历史日期工具。

后两个用于探索
更具体的历史日期查询。

关键词仅为初始输入。

工具可能返回其他相关词、
不同拼写或者没有数据。

应保存实际返回值，
不能人为补齐数字。

建议时间范围：

最近三个月。

同时保存：

- 查询日期。
- Bing显示的原始搜索量。
- 搜索量统计口径。
- 关键词建议。
- 可用的前十结果。
- 地区及语言设置。

若数据缺失，
记录NOT_AVAILABLE。

不得将没有结果解释为
搜索量等于零。

## 八、停止条件

下一轮只针对少量关键词。

若Bing无法访问或没有有效数据，
先记录实际原因。

不购买昂贵SEO订阅。

若获得搜索量，
继续比较具体竞争者。

若搜索量明显有限，
但存在高价值专业需求，
仍需检查用户任务和变现方式，
不能机械地根据单个数字淘汰。

若无实际需求证据、
无独立用户价值，
则停止对应候选深入调查。

不能将所有UNKNOWN
自动转换成REJECTED。

## 九、当前结论

SEARCH_DEMAND_METHOD=DEFINED

BING_VOLUME_CAPABILITY=VERIFIED
BING_KEYWORD_DATA=NOT_COLLECTED

GOOGLE_TRENDS_HISTORY=AVAILABLE
GOOGLE_ABSOLUTE_VOLUME=UNKNOWN

INDEPENDENT_ORGANIC_TRAFFIC=UNKNOWN
AD_PAGE_RPM=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN

FORMAL_PROJECT_SELECTED=NO
SECOND_PROJECT=NOT_DECIDED

本次完成的是证据获取方法，
不是商业可行性证明。

## 十、下一阶段

NEXT=BING_DE_KEYWORD_VOLUME_AND_SERP_EVIDENCE_PILOT

下一轮实际操作：

1. 进入Bing Webmaster Tools。
2. 打开Keyword Research。
3. 设置德国与德语。
4. 查询本报告的样本关键词。
5. 保存实际搜索量和结果证据。
6. 比较既有Google Trends结论。
7. 确定哪些候选值得重新研究。

首先只完成一个国家样本。

不扩展到全部66个locale。
不购买付费SEO订阅。
不启动翻译。
不建立网站。
不修改go-dev v2。

保持RESEARCH_ONLY。
