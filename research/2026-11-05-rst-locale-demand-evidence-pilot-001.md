# Rust 四语言搜索需求证据试点 001

核实日期：2026-11-05
阶段：RST_LOCALE_DEMAND_EVIDENCE_PILOT
状态：RESEARCH_ONLY
第二项目：NOT_DECIDED

## 一、调查范围

代表市场：de-DE、ko-KR、zh-CN、id-ID。
不是66 locales的全面市场调查。

德国已有可验证的 Google Trends 原始数据。
其余三市场当前没有同等的搜索需求数据。

DEMAND_EVIDENCE_AVAILABLE=1_OF_4_MARKETS

## 二、德国60个月搜索兴趣

来源：https://trends.google.com/explore
原始文件：research/evidence/2026-11-03-google-trends-DE-rust-001.csv
SHA-256：521b755e9487d2f7b891e40a7c412d1a76f81d15b34c606d8ee9abffbf37072b
地区：德国；网页搜索；五个搜索词同批比较。
时间：2021-11至2026-10，共60个连续月份。

| 搜索词 | 月均指数 | 非零月份 | 前12月平均 | 后12月平均 |
| --- | ---: | ---: | ---: | ---: |
| Rust lernen | 0.78 | 3/60 | 0.00 | 3.92 |
| Rust programmieren | 0.43 | 2/60 | 0.00 | 0.50 |
| Rust Programmiersprache | 37.77 | 60/60 | 41.75 | 38.83 |
| Rust Tutorial | 48.70 | 59/60 | 37.58 | 60.25 |
| Rust für Anfänger | 0.03 | 1/60 | 0.00 | 0.17 |

德国 Rust Programmiersprache 存在
60个月持续非零的相对搜索兴趣证据。

Rust Tutorial 也具有长期非零指数，
但该搜索词可能混入同名游戏的搜索意图，
需要进一步检查关联查询与搜索结果。

Rust lernen 的低指数不能用于否定整个市场。

Google Trends指数不是绝对搜索次数。
不能跨不同查询批次直接比较归一化指数。
低指数或零值不代表真实搜索次数为零。

## 三、四市场内容竞争线索

### de-DE

需求：已有Google Trends相对搜索兴趣数据。
完整同源译本竞争：PARTIALLY_OBSERVED。
Rust Book 官方翻译目录包含德语译本。
来源：https://doc.rust-lang.org/stable/book/appendix-06-translation.html
SERP排名及可获取流量：UNKNOWN。

### ko-KR

需求：UNKNOWN。
已发现社区 Rust Book 韩语译本，
以及多个模块的实际韩语PO内容。
来源：https://github.com/rust-kr/doc.rust-kr.org
来源：https://rust-lang-translations.org/
搜索结果竞争强度：UNKNOWN。

### zh-CN

需求：UNKNOWN。
需要单独考虑中国大陆搜索引擎生态。
已有多种Rust中文教程和社区译本。
来源：https://rustwiki.org/
来源：https://course.rs/
来源：https://index.baidu.com/
实际可获取流量：UNKNOWN。

### id-ID

需求：UNKNOWN。
已发现印尼语Rust原创教程和练习项目。
来源：https://rusttutorial.org/id/
来源：https://github.com/magercode/belajar-rust
它们属于同主题竞争线索，
不自动等同于六模块同源完整译本。
实际搜索竞争强度：UNKNOWN。

## 四、商业判断

德国：已有长期相对搜索兴趣证据。
韩国：已有强同源内容竞争证据。
中文：中国大陆存在不同搜索渠道，
且已有成熟中文资料竞争者。
印尼语：并非缺乏Rust学习内容。

以上结论不构成收入或市场优先级排名。

ABSOLUTE_SEARCH_VOLUME=UNKNOWN
ORGANIC_TRAFFIC=UNKNOWN
AD_RPM=UNKNOWN
NET_AD_PROFIT=UNKNOWN
LANGUAGE_COMMERCIAL_RANKING=NOT_READY

## 五、下一轮数据采集

下一轮仅补充尚未取得的市场证据：

ko-KR：Google Trends，调查韩语与英文Rust学习关键词。
id-ID：Google Trends，调查印尼语与英文Rust学习关键词。
zh-CN：优先调查百度指数中的Rust学习关键词。

必须记录地区、日期、搜索词、
搜索类型、来源URL和原始数据。

Google Trends需保留相同查询内的比较关系。
百度与Google指数不能直接按数值排名。

若数据访问受限，记录UNKNOWN或UNCLEAR，
不得使用估算数字代替真实搜索证据。

## 六、阶段决策

RUST_STATUS=RESEARCH_CONTINUE
SECOND_PROJECT=NOT_DECIDED
NEXT=RST_REMAINING_LOCALE_DEMAND_CAPTURE

保持RESEARCH_ONLY。
不启动翻译，不创建网站，不修改go-dev。
