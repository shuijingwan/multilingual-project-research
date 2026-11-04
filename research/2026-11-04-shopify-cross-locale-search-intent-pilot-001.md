# Shopify 跨语言搜索意图初筛 001

核实日期：2026-11-04

阶段：SHOPIFY_CROSS_LOCALE_SEARCH_INTENT_PILOT

状态：RESEARCH_ONLY

候选：Shopify Developer Learning & Documentation

目标范围：冻结66个locale

第二项目：NOT_DECIDED

## 一、原始证据

全球Google Trends网页搜索，五词同时比较。

时间范围：2021-11至2026-10，共60个月。

时间序列：

`research/evidence/time_series_Worldwide_20211101-0800_20261104-1154.csv`

SHA-256：`c80cff0eba21cb83fe68cb453108360b07a087773dd598d1fe47f282945546ad`

地域构成：

`research/evidence/by_region_Worldwide_20211101-0800_20261104-1154.csv`

SHA-256：`b0e1dd6502c0676d3c4c27453f54ab7d80ad096d6cfd766e7e80d60230541843`

地区行数：65。

注意：65个地区不等于66个目标locale。

## 二、时间序列结果

以下数值均为同一次比较中的
归一化相对搜索兴趣指数。

不是实际月搜索次数。

| 搜索词 | 2022月均 | 2024月均 | 2025-07 | 2025-08 | 2026-06 | 2026-10 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Shopify Liquid | 18.67 | 24.58 | 21 | 47 | 100 | 6 |
| Shopify app development | 2.00 | 3.33 | 4 | 16 | 20 | 2 |
| Shopify theme development | 1.00 | 1.83 | 2 | 7 | 22 | 1 |
| Shopify GraphQL | 5.08 | 10.17 | 14 | 71 | 52 | 3 |
| Shopify CLI | 3.08 | 4.50 | 5 | 25 | 54 | 3 |

观察：

1. Shopify Liquid在五词中整体兴趣最高。
2. Shopify GraphQL具有较明显的长期搜索信号。
3. 2025-08五个搜索词同时明显跳升。
4. 2026-06部分词出现高峰。
5. 2026年后期又出现明显下降。

不能直接解释为开发者搜索需求暴增
或者随后需求崩溃。

时间序列结构性变化的原因：
UNKNOWN。

不根据高峰预测长期流量。

## 三、地域数据结构

所有65个地区的数据行，
五个搜索词合计恰好为100。

因此这是五词在各地区的
相对构成数据。

不是各国绝对搜索量，
不是每个词在当地全部Google搜索中的比例。

| 地区 | Liquid | App | Theme | GraphQL | CLI |
| --- | ---: | ---: | ---: | ---: | ---: |
| 美国 | 49 | 9 | 5 | 23 | 14 |
| 德国 | 52 | 7 | 3 | 25 | 13 |
| 法国 | 51 | 5 | 2 | 28 | 14 |
| 日本 | 52 | 4 | 2 | 24 | 18 |
| 韩国 | 34 | 21 | 8 | 22 | 15 |
| 印度 | 57 | 8 | 4 | 22 | 9 |
| 俄罗斯 | 42 | 23 | 11 | 17 | 7 |

例如韩国App的21，
不能解释成韩国开发者搜索量
高于美国App的9。

本轮全部是英文搜索词。

本地语言搜索需求：
UNKNOWN。

不能用本轮数据对66个locale
进行商业收益排名。

## 四、方法限制

Google Trends是抽样数据。

数据按时间和地区归一化，
不能当作月搜索量。

低搜索兴趣词可能受到
采样、统计噪声等因素影响。

官方方法说明：

https://support.google.com/trends/answer/4365533

https://newsinitiative.withgoogle.com/resources/trainings/google-trends/basics-of-google-trends/

没有充分证据解释
2025-08之后的共同波动。

不能把可能的采样异常
视为已证实的真实需求增长。

## 五、项目商业判断

Shopify开发者搜索兴趣存在：
PARTIALLY_VERIFIED。

Liquid及GraphQL是值得继续调查
的具体技术搜索意图。

但以下内容仍为UNKNOWN：

- 异常波动的原因。
- 本地语言开发者搜索需求。
- 完整66-locale市场缺口。
- 独立翻译站可获取的自然流量。
- 实际广告Page RPM。
- 长期广告净收益。

现有内容策略不变：

LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS

只有明确授权资料才能翻译。

未明确授权资料直接链接官方。

不要求原创补齐。

## 六、下一阶段与停止线

NEXT=SHOPIFY_TRENDS_BREAKPOINT_VALIDATION

下一阶段优先对共同时间断点
进行低成本独立交叉检查。

避免继续增加大量关键词
却没有解释数据可靠性问题。

若断点不能被充分验证，
使用保守的长期稳定需求信号，
不得使用异常高峰预测商业价值。

不启动翻译、建站或部署。
不修改go-dev v2。

## 七、保守基准修订（2026-11-04）

决策：STOP_BREAKPOINT_INVESTIGATION

不再追查2025-08至2026-07
共同高波动区间的具体原因。

这不代表该区间已被证明是错误数据。

主要分析基准：
2021-11至2025-07，共45个月。

排除区间：
2025-08至2026-07，共12个月。

2026-08至2026-10仅3个月，
不纳入长期基准。

### 五词基准结果

| 搜索词 | 45个月月均相对指数 |
| --- | ---: |
| Shopify Liquid | 21.27 |
| Shopify GraphQL | 8.11 |
| Shopify CLI | 3.84 |
| Shopify app development | 2.67 |
| Shopify theme development | 1.42 |

本表数据由已归档CSV重新计算。

指数并非实际搜索次数。
不代表月搜索量或可获取自然流量。

阶段性发现：

1. Liquid具有最强相对搜索兴趣。
2. GraphQL排名第二。
3. 其他英文词低指数
   不能证明本地语言市场没有需求。
4. 不利用被排除高波动区间
   预测网站流量或广告收入。

长期流量：UNKNOWN。
实际Page RPM：UNKNOWN。
66-locale商业收益：UNKNOWN。

### 下一阶段

NEXT=SHOPIFY_CROSS_LOCALE_COMPETITION_GAP_PILOT

停止进一步研究趋势异常。

优先核查有明确许可的内容主题
在代表性目标语言市场中的：

- 搜索竞争。
- 官方及第三方内容覆盖。
- 真实多语言资料缺口。
- 独立翻译站的额外用户价值。

抽样不得冒充66-locale完整结论。

不启动正式项目。
不翻译未授权内容。
不要求原创补齐。
不修改go-dev v2。
