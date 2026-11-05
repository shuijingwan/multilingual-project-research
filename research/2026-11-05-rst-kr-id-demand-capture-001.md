# Rust 韩国与印尼搜索需求证据采集 001

核实日期：2026-11-05
阶段：RST_REMAINING_LOCALE_DEMAND_CAPTURE_KR_ID
状态：RESEARCH_ONLY
正式项目：NOT_DECIDED

## 一、数据说明

来源：https://trends.google.com/explore
界面：新版 Google Trends Explore
搜索类型：Google 网页搜索
类别：所有类别
时间：2021-11 至 2026-10
每个国家：60个月、5个搜索词

各国内部五个词在同一查询中比较。
韩国与印尼分别归一化，不能直接比较指数。
原始CSV逐字节保存，不修改任何数据。

## 二、韩国（KR）

原始文件：research/evidence/2026-11-05-google-trends-KR-001.csv
SHA-256：95cc8cb96dce2cb48499fab4e10f2169775c807f6c180492a63952bcbf6de53a

| 搜索词 | 60月平均 | 非零月份 | 前12月平均 | 后12月平均 |
| --- | ---: | ---: | ---: | ---: |
| Rust 프로그래밍 | 6.88 | 11/60 | 9.33 | 0.42 |
| 러스트 언어 | 20.58 | 26/60 | 21.42 | 7.92 |
| Rust tutorial | 11.30 | 14/60 | 10.08 | 37.75 |
| Rust ownership | 6.28 | 7/60 | 0.00 | 31.42 |
| Rust 강좌 | 0.00 | 0/60 | 0.00 | 0.00 |

## 二、印度尼西亚（ID）

原始文件：research/evidence/2026-11-05-google-trends-ID-001.csv
SHA-256：c5ebfba7f5b7b23e15cdfd75d914664fe47104280f08123c6064eab08cfba879

| 搜索词 | 60月平均 | 非零月份 | 前12月平均 | 后12月平均 |
| --- | ---: | ---: | ---: | ---: |
| belajar Rust | 0.05 | 1/60 | 0.00 | 0.25 |
| bahasa pemrograman Rust | 0.10 | 1/60 | 0.00 | 0.50 |
| tutorial Rust | 3.13 | 10/60 | 0.00 | 8.75 |
| Rust programming | 27.43 | 54/60 | 13.50 | 47.25 |
| Rust ownership | 0.32 | 1/60 | 0.00 | 1.58 |

## 三、证据解释

### 韩国

러스트 언어具有可观测搜索兴趣，
但60个月中仍有大量零值月份。
Rust tutorial、Rust ownership可能存在
非编程语言或其他搜索意图，尚未独立排除。

2026年7月至9月，五个词均显示为零。
记录为待复核现象，不推断市场需求消失。

### 印度尼西亚

Rust programming在54个月显示非零指数，
比本轮选定的印尼语关键词更稳定。
但不能直接推断用户偏好英文内容。
需另查实际搜索意图与现有排名网站。

## 四、商业判断

德国、韩国、印尼三个市场已经具有
可核实的Google Trends搜索兴趣证据。

GOOGLE_TRENDS_MARKETS=3
TARGET_MARKETS=4
ZH_CN_DEMAND=UNKNOWN
ABSOLUTE_SEARCH_VOLUME=UNKNOWN
OBTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
AD_RPM=UNKNOWN
NET_AD_PROFIT=UNKNOWN

指数不代表绝对搜索次数。
零值不代表没有真实搜索需求。
不同国家的指数不得直接排名。
本轮尚不能决定Rust多语言项目的商业优先级。

## 五、下一步

NEXT=RST_ZH_CN_DEMAND_CAPTURE

只补充中国大陆Rust搜索需求证据。
优先调查百度指数及其他可靠数据来源。
如无法取得数据，应保留UNKNOWN。

RUST_STATUS=RESEARCH_CONTINUE
SECOND_PROJECT=NOT_DECIDED

不启动翻译，不创建网站，不修改go-dev。
