# 历史日期核对搜索意图与竞争停止线 001

核实日期：2026-11-05
阶段：HIST_DATE_INTENT_GAP_STOP_PILOT
状态：RESEARCH_ONLY

候选：历史文献日期核对工具
目标范围：冻结66个locale
商业目标：LONG_TERM_AD_NET_PROFIT
正式项目：NOT_DECIDED

## 一、具体用户任务

目标用户：

- 家谱研究者。
- 历史研究者。
- 档案阅读者。
- 历史文献编辑者。

需要解决：

1. 儒略历与公历转换。
2. 地区采用公历的具体时间。
3. 英国旧式年份及双年份。
4. 保留原始日期与规范日期。
5. 历史日期出处与不确定性。
6. 不同历法记录之间的日期核对。

这些任务存在实际使用场景。

但用户任务存在不等于
已测得长期搜索需求。

## 二、权威证据

### 2.1 英国历法改革

英国原始法律：

https://www.legislation.gov.uk/apgb/Geo2/24/23

Calendar (New Style) Act 1750。

法律明确规定：

- 1752年开始采用1月1日作为年初。
- 1752年9月2日之后为9月14日。
- 改历时省略11个日期标签。

状态：

UK_REFORM_PRIMARY_SOURCE=VERIFIED

历史档案解释：

https://libguides.ctstatelibrary.org/hg/colonialresearch/calendar

康涅狄格州立图书馆说明
旧式纪年、双年份及历史记录问题。

### 2.2 天文计算

美国海军天文台：

https://aa.usno.navy.mil/faq/JD_formula

提供儒略日数与日期的换算说明。

注意：

Julian Day Number与Julian Calendar
不是同一个概念。

海军天文台的相关公式
还存在明确的年份适用范围。

不得将某个限定年份的公式
未经验证地扩展到全部历史年代。

CALCULATION_REFERENCE=VERIFIED

COMPLETE_HISTORICAL_ALGORITHM=NOT_AUDITED

### 2.3 历史复杂性

必须区分：

- 数学上的历法转换。
- 历史地区实际使用的历法。
- 历史资料中的年份记法。
- 研究者对不确定日期的解释。

只根据国家名称或世纪，
不能保证判断所有历史文献正确。

## 三、英语竞争

KleioBase：

https://kleiobase.com/tools/calendar-converter

页面提供：

- Gregorian。
- Julian。
- Hebrew。
- French Republican。
- 地区改历信息。
- Old Style双年份。
- 星期及计算说明。

The Old Reckoner：

https://theoldreckoner.co.uk/old-style-new-style/

提供：

- 英国旧式日期转换。
- 3月25日年初规则。
- 双年份解释。
- 历史实例。
- 使用限制及来源说明。

TNAADO：

https://tools.tnaado.ca/calculators/general/old-style-new-style-date-converter/

提供同类旧式日期转换。

状态：

EN_DIRECT_COMPETITION=VERIFIED

地区改历和双年份
不是尚无人提供的新功能。

## 四、德语竞争

Familienforschung Krauss：

https://www.familienforschung-krauss.de/de/genealogie/genealogie-datumdifferenz-rechner/

提供：

- 家谱日期计算。
- 儒略历与公历选择。
- 历史地区改革说明。
- 出生与死亡日期相关计算。
- 多个地区的改革资料。

苏黎世大学Ad fontes：

https://www.adfontes.uzh.ch/tutorium/datierungen-aufloesen/chronologie/julianischer-kalender

提供历史日期和历法解释。

状态：

DE_DIRECT_COMPETITION=VERIFIED

不能将德国地区改历资料
认定为独立网站特有优势。

## 五、西班牙语竞争

Promystical：

https://promystical.eu/es/juliano-gregoriano

提供：

- 儒略历与公历换算。
- 历法差异说明。
- 不同地区的改历资料。

状态：

ES_DIRECT_COMPETITION=VERIFIED

但尚未核实全部历史家谱
与特殊年份处理功能。

ES_FULL_TASK_COVERAGE=UNKNOWN

## 六、简体中文竞争

TempleKit：

https://templekit.com/zh-hans/tools/date-calculator

提供：

- 家谱日期计算。
- 儒略历与格里历换算。
- 双年份输入说明。
- 地区改历资料。

另有其他中文历法工具。

但部分工具处理的是
儒略日数而非儒略历。

不得混淆两种用户任务。

状态：

ZH_DIRECT_COMPETITION=VERIFIED

ZH_FULL_TASK_COVERAGE=UNKNOWN

## 七、竞争汇总

| 语言 | 直接竞争 | 全部需求覆盖 |
| --- | --- | --- |
| en | VERIFIED | PARTIAL |
| de | VERIFIED | UNKNOWN |
| es | VERIFIED | UNKNOWN |
| zh | VERIFIED | UNKNOWN |

这里的PARTIAL表示已确认
多个主要功能存在竞争供给，
不是整体市场覆盖率。

其他62个目标locale
没有开展完整调查。

本轮没有运行竞争工具的
全套算法正确性测试。

COMPETITOR_FUNCTIONAL_QA=NOT_DONE

## 八、搜索需求证据

本次公开网页调查能确认：

- 已有面向历史日期的具体工具。
- 已有家谱及档案使用说明。
- 多语言市场存在相关内容。
- 相关工具面向不同研究任务。

但没有取得：

- 可信关键词月搜索量。
- 搜索点击率。
- 竞争站点自然访问量。
- 新站可获取流量份额。
- 用户重复使用频率。
- 真实广告Page RPM。

因此：

SEARCH_INTENT=IDENTIFIED
SEARCH_VOLUME=UNKNOWN
SERP_RANKINGS=NOT_MEASURED
ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
REPEAT_USAGE=UNKNOWN
AD_PAGE_RPM=UNKNOWN

不得把公开搜索结果中出现工具，
当作搜索量证明。

也不得因找到竞争工具，
直接断言没有市场需求。

## 九、独立用户价值

本轮最初提出的功能：

- 地区改历。
- 双年份。
- 历法转换。
- 历史解释。
- 原始日期保留。

多数已有直接竞争信号。

剩余可能的改进包括：

- 更细地区历史记录。
- 完整文献出处。
- 更一致的多语言使用体验。
- 可复制的研究引用格式。

但是：

这些差异尚未证明
具有独立、持续的搜索需求。

部分功能还需要
复杂的历史资料审核。

INDEPENDENT_USER_VALUE=NOT_VERIFIED

不应只为增加少量功能
就开始开发新的计算器网站。

## 十、工程与商业风险

潜在成本：

- 历法算法验证。
- 地区改革例外维护。
- 历史年份记法处理。
- 多语言解释内容。
- 资料来源复核。
- 用户输入错误处理。

成本尚未量化。

MAINTENANCE_COST=UNKNOWN

历史日期具有长期查询价值，
但单次转换可能只产生一次访问。

不能由此推断具体PV或RPM。

LONG_TERM_AD_NET_PROFIT=UNKNOWN

## 十一、停止线

证据判断：

DIRECT_COMPETITION=VERIFIED
INDEPENDENT_USER_VALUE=NOT_VERIFIED
SEARCH_VOLUME=UNKNOWN
ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN

当前没有足够证据支持
继续开展66-locale全面调查。

决策：

HIST_DATE_STATUS=RESEARCH_CONTINUE
HIST_DATE_DEEP_DIVE=PAUSED

不批准工具开发。

该决策不代表
历史日期工具不存在商业价值。

只是当前无法证明
新增调查投入具有合理回报。

## 十二、恢复研究条件

出现下列新增证据可复评：

1. 可验证的具体关键词搜索需求。
2. 已有工具无法满足的实际用户任务。
3. 多个目标语言存在明确供给缺口。
4. 可低成本实现的独立差异化。
5. 自然流量可能覆盖维护成本的证据。

不得仅因为发现新竞争网站
或新功能设想就恢复深入研究。

## 十三、下一阶段建议

NEXT=CROSS_DOMAIN_SEARCH_DEMAND_EVIDENCE_GATE

建议先改变商业证据获取方法，
再继续选择新研究方向。

重点调查：

1. 如何低成本取得可信搜索需求证据。
2. 如何区分搜索兴趣与自然流量。
3. 如何估计新站可获得的搜索点击。
4. 如何验证具体用户任务尚未满足。
5. 如何设置不依赖猜测的停止门槛。

不创建昂贵的SEO研究系统。

不为取得数据购买高价订阅。

只有出现有价值的新证据，
才继续投入具体候选的深入研究。

SECOND_PROJECT=NOT_DECIDED
FORMAL_PROJECT_SELECTED=NO

保持RESEARCH_ONLY。

不启动翻译。
不建设正式网站。
不部署服务。
不修改go-dev v2。
