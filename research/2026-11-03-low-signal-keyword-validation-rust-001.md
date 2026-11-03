# 德国 Rust 低信号关键词验证 001

核实日期：2026-11-03
状态：RESEARCH_ONLY
阶段：RUST_LOW_SIGNAL_KEYWORD_VALIDATION

## 一、数据来源

Google Trends：https://trends.google.com/explore

地区：德国（DE）
时间：2021-11-01 至 2026-10-31
搜索类型：网页搜索
样本：5个搜索词，60个月

本批次共享0～100归一化尺度。
不同批次的指数不得直接拼接比较。

## 二、实测数据

| 搜索词 | 60月平均 | 前12月 | 后12月 | 0值月份 |
| --- | ---: | ---: | ---: | ---: |
| Rust lernen | 0.78 | 0.00 | 3.92 | 57/60 |
| Rust programmieren | 0.43 | 0.00 | 0.50 | 58/60 |
| Rust Programmiersprache | 37.77 | 41.75 | 38.83 | 0/60 |
| Rust Tutorial | 48.70 | 37.58 | 60.25 | 1/60 |
| Rust für Anfänger | 0.03 | 0.00 | 0.17 | 59/60 |

## 三、研究结论

### Rust Programmiersprache

60个月均有非零指数。
该表达明确指向Rust编程语言。
观察到长期持续的搜索兴趣。

### Rust Tutorial

本批次指数较高，
但同时可能涉及同名游戏教程。
不能全部视为Rust编程学习需求。

### 其他三个表达

Rust lernen、Rust programmieren、
Rust für Anfänger多数月份为零。
这些零值不能证明编程需求不存在。

## 四、竞争证据

Microsoft Learn德语Rust初学者系列：
https://learn.microsoft.com/de-de/shows/beginners-series-to-rust/

2026年德语Rust Book译本：
https://rust-lernen.de/books/978-3-98871-008-6.html

现有德语学习供给已存在。
完整覆盖、SEO竞争及可获取流量
仍需要独立调查。

## 五、商业判断

Rust编程搜索兴趣存在：VERIFIED。
Rust Tutorial搜索意图归属：UNCLEAR。
独立站可获取流量：UNKNOWN。
实际Page RPM：UNKNOWN。
长期广告净收益：UNKNOWN。

保留Rust候选，不优先立项。
不再因单个低信号关键词淘汰领域。

## 六、原始证据

CSV：`research/evidence/2026-11-03-google-trends-DE-rust-001.csv`
SHA-256：`521b755e9487d2f7b891e40a7c412d1a76f81d15b34c606d8ee9abffbf37072b`

原始60个月数据按字节保留。

## 七、下一阶段

CROSS_DOMAIN_INTENT_COMPETITION_PILOT

停止本轮关键词试验，
返回跨领域用户意图、竞争供给
和独立站可获取流量研究。

不修改66-locale顺序。
不启动翻译、建站或部署。
不修改go-dev v2。
