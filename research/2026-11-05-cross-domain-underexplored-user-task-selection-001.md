# 跨领域未充分研究用户任务筛选 001

核实日期：2026-11-05
阶段：CROSS_DOMAIN_UNDEREXPLORED_USER_TASK_SELECTION
状态：RESEARCH_ONLY

商业目标：LONG_TERM_AD_NET_PROFIT
目标范围：冻结66个locale
第二正式项目：NOT_DECIDED

## 一、研究背景

此前已经调查：

- Rust完整学习体系。
- Python官方学习文档。
- OWASP安全资料。
- Ethereum开发资料。
- Shopify开发资料。
- 世界历史开放教材。
- 国家地理与比较工具。

多个候选已经完成阶段停止线。

当前共同问题：

- 可获取自然流量UNKNOWN。
- 广告Page RPM UNKNOWN。
- 独立用户价值尚未充分验证。
- 长期广告净收益UNKNOWN。

不能仅因内容开放授权，
就继续投入大规模翻译。

本轮改变调查单位：

从宽泛内容领域，
转向具体用户任务。

## 二、任务A：历史文献日期核对

代号：HIST_DATE

用户任务：

研究历史文献、家谱、
旧报纸及历史事件时，
核对不同历法记载的日期。

具体可能需要：

1. 儒略历与公历双向换算。
2. 区分历史纪年与计算纪年。
3. 核对不同地区采用公历的时间。
4. 识别英国旧式年份记法。
5. 处理历史日期中的双年份。
6. 给出计算依据与历史解释。

这不是普通日期加减计算器。

### 2.1 权威计算资料

美国海军天文台：

https://aa.usno.navy.mil/data/JulianDate

算法说明：

https://aa.usno.navy.mil/faq/JD_formula.html

NASA JPL：

https://ssd.jpl.nasa.gov/tools/jdc/

状态：

CALENDAR_CALCULATION_REFERENCES=VERIFIED

这些资料可以作为
未来独立实现的核对依据。

但不能自动认定其网页、
软件或其他素材均可商业转载。

REFERENCE_CONTENT_REUSE_RIGHTS=NOT_AUDITED

应优先考虑自主编写算法和说明，
而不是复制第三方网站代码。

### 2.2 历史复杂性

不同地区采用公历的日期不同。

例如：

1582年部分欧洲地区开始改历。

英国及其殖民地在1752年改历。

俄罗斯在1918年改历。

英国旧式年份还有
以3月25日开始新年的问题。

因此：

同一个历史日期的解释
可能依赖地区和历史时期。

另外必须区分：

JULIAN_CALENDAR：
儒略历。

JULIAN_DAY_NUMBER：
天文学中的儒略日数。

二者不是同一概念。

历史日期转换还可能涉及：

- 不同地区的特殊改革。
- 历史年份没有公元零年。
- 公元前日期。
- 地方历法与宗教历法。
- 文献日期本身有歧义。

不能用简单固定天数
处理所有历史情况。

### 2.3 已有竞争

美国海军天文台：
https://aa.usno.navy.mil/data/JulianDate

The Old Reckoner：
https://theoldreckoner.co.uk/old-style-new-style/

KleioBase：
https://kleiobase.com/tools/calendar-converter

ORA：
https://www.ora-extension.com/en/date-converter.htm

法语计算器：
https://www.vmaths.fr/apps/convertisseur-dates-historiques-julien-gregorien

其他日期转换工具已经存在。

状态：

DIRECT_COMPETITION=VERIFIED

尤其不能声称
地区改历、旧式年份处理
是全新的市场空白。

### 2.4 潜在独立价值

可进一步验证的差异化：

- 多语言历史文献阅读辅助。
- 原始日期和规范日期同时展示。
- 显示地区与时期的解释依据。
- 明确标记不确定的历史日期。
- 提供可复制的日期说明。
- 结合来源和引用信息。

以上只是产品假设。

USER_VALUE_DIFFERENTIATION=UNKNOWN

需要检查竞争者是否已经提供
同等或更好的功能。

### 2.5 商业风险

历史日期本身相对稳定。

但历史采用记录、
地方差异及例外需要专业审核。

用户可能完成一次转换后
立即离开网站。

可能缺少重复访问及足够PV。

搜索引擎也可能直接回答
简单日期转换问题。

因此：

SEARCH_VOLUME=UNKNOWN
ORGANIC_TRAFFIC=UNKNOWN
REPEAT_USAGE=UNKNOWN
MAINTENANCE_COST=UNKNOWN
AD_NET_PROFIT=UNKNOWN

不能将内容稳定
直接等同于商业优势。

## 三、任务B：统计指标变化解释

代号：DATA_CHANGE

用户任务：

输入国家、指标及年份，
获得绝对变化、百分比变化、
数据来源和缺失值说明。

候选数据源：

https://datacatalog.worldbank.org/public-licenses

https://www.worldbank.org/ext/en/legal/terms-conditions/datasets

世界银行部分数据
具有CC BY 4.0授权。

但不同数据集存在许可例外。

API与数据集授权条件
应分别审查。

此前GEO已经研究
国家统计比较功能。

成熟竞争者也提供
类似国家数据比较。

因此：

DATA_LICENSE=PARTIALLY_VERIFIED
DATA_TASK_DISTINCTNESS=NOT_VERIFIED

暂不选择DATA_CHANGE。

重新研究前必须明确
不同于GEO的独立用户价值。

## 四、任务C：AI开发错误诊断

代号：AI_ERROR

用户任务：

根据实际API错误、
状态码及请求配置，
找到对应原因和修复方法。

潜在应用对象：

DeepSeek等AI开发平台。

官方技术资料：

https://api-docs.deepseek.com/

但需要核实：

- 文档商业复用权限。
- 官方错误代码覆盖。
- 现有开发者工具竞争。
- 版本和接口变化。
- 故障处理内容的审核成本。

不能将模型权重许可证
套用到官方API文档。

目前：

FULL_DOC_REUSE_RIGHTS=UNCLEAR
SEARCH_VOLUME=UNKNOWN
MAINTENANCE_COST=UNKNOWN

暂不选择AI_ERROR。

## 五、三任务筛选

| 任务 | 已有竞争 | 授权风险 | 维护风险 |
| --- | --- | --- | --- |
| HIST_DATE | VERIFIED | 自主算法路径可研究 | 历史例外核实 |
| DATA_CHANGE | VERIFIED | 数据及API需分开核实 | 数据更新 |
| AI_ERROR | PARTIAL | 官方文档许可不明 | 接口变化 |

三项任务均未证明
具有长期广告净收益。

本表不是商业收益排名。

## 六、本轮选择

SELECTED_NEXT_RESEARCH=HIST_DATE

选择依据：

1. 用户任务足够具体。
2. 可参考权威历法资料。
3. 基础计算规则相对稳定。
4. 可以研究自主实现路径。
5. 与GEO的国家比较工具不同。
6. 可采用小规模竞争调查。
7. 可以设置明确停止线。

但是：

市场未被证明低竞争。

已有多个直接工具。

本轮只选择调查对象，
不是批准建立新网站。

FORMAL_PROJECT_SELECTED=NO
SECOND_PROJECT=NOT_DECIDED

## 七、下一轮调查

NEXT=HIST_DATE_INTENT_GAP_STOP_PILOT

只调查以下问题：

1. 是否存在明确的历史日期
   搜索需求和用户任务证据。

2. 已有竞争者具体覆盖哪些功能。

3. 是否存在真正未满足的
   地区、历法或文献阅读需求。

4. 中文、英文、德语、
   西班牙语等少量语言市场，
   是否存在可验证的有效供给差异。

5. 普通搜索结果和AI搜索结果
   是否已经满足用户需求。

6. 自主实现是否能够避免
   第三方素材授权问题。

7. 用户完成转换后，
   是否有足够理由继续访问其他页面。

8. 维护及史料核实成本
   是否与潜在收益相称。

不得为了继续推进项目，
刻意寻找细小功能差异。

如果已有竞争者满足核心任务，
且无法发现可信流量机会，
应及时暂停HIST_DATE调查。

## 八、停止条件

出现以下情况应停止：

- 没有可靠需求证据。
- 已有工具完整满足主要需求。
- 差异化只能依赖复杂历史资料整理。
- 需要大量难以审核的地方历法数据。
- 没有可解释的自然搜索点击机会。
- 单次使用难以支持合理的广告收入。

这些条件不是预先判定失败。

下一阶段必须依据证据判断。

## 九、总体商业状态

HIST_DATE_STATUS=RESEARCH_PILOT

SEARCH_VOLUME=UNKNOWN
ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
AD_PAGE_RPM=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN

COMMERCIAL_RANKING=NOT_READY
FORMAL_PROJECT_SELECTED=NO
SECOND_PROJECT=NOT_DECIDED

研究状态保持RESEARCH_ONLY。

不启动正式工具开发。
不创建内容网站。
不部署服务。
不购买域名。
不修改go-dev v2。
