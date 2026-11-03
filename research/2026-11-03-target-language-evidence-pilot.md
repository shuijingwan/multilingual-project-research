# 目标语言市场证据试点

核实日期：2026-11-03
阶段：TARGET_LANGUAGE_DEMAND_EVIDENCE
状态：RESEARCH_ONLY
正式立项：NONE

## 一、研究范围

固定目标语言为 go-tour-i18n 中的 66 门。

正式范围与顺序引用：
research/2026-11-03-target-locales-source-snapshot.md

本轮仅对部分目标语言开展供给核查，
不重新选择语言或调整商业排序。

本次主要调查 zh-CN、de-DE。

样本不足以代表全部 66 门语言。

## 二、Python 官方教程

zh-CN：
https://docs.python.org/zh-cn/3/tutorial/

de-DE：
https://docs.python.org/de/3/tutorial/

状态：VERIFIED

上述语言均已有官方 Tutorial。

但整个 Python 文档体系的
有效翻译覆盖仍为 UNKNOWN。

不能仅凭 Tutorial 存在，
判断整套官方文档已经完整覆盖。

## 三、Rust 学习体系

中文官方学习入口：
https://rust-lang.org/zh-CN/learn/

该页面提供社区翻译入口。

德文 Rust Book 出版记录：
https://rust-lernen.de/books/978-3-98871-008-6.html

状态：VERIFIED

德文译本在 2026 年存在持续更新证据。

但 Rust Book、Rust By Example、
Cargo、Reference、Rustonomicon 等
完整学习体系的覆盖情况仍需分别核实。

不能把单本教材译本视为完整覆盖。

## 四、OWASP 安全资料

中文 SQL 注入防御指南：
https://cheatsheetseries.owasp.ac.cn/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html

当前英文官方指南：
https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html

状态：VERIFIED

已有中文译文。

初步发现中文页面与当前英文页面
在结构及表述上存在差别。

是否属于版本滞后：
UNKNOWN，需结合 Git 历史核实。

整个系列的中文有效覆盖：
UNKNOWN。

## 五、Ethereum 开发文档

德文官方文档：
https://ethereum.org/de/developers/docs/

状态：VERIFIED

已有德文开发文档入口。

具体章节完整性、更新及时性：
UNKNOWN。

不因此认定其他目标语言已经覆盖。

## 六、历史及其他非技术领域

已发现开放历史教材及数据来源。

但本轮尚未获得足够可靠的
目标语言翻译覆盖和搜索需求证据。

状态：UNKNOWN。

不得把没有搜到译本
直接解释为没有竞争对手。

## 七、搜索需求数据源

### Google Trends

https://trends.google.com/trends/

用途：
比较同一市场、同一时间范围下
不同主题的相对搜索兴趣。

数据归一化，通常显示为 0～100。

不能将其当作搜索次数或广告收入。

来源：
https://support.google.com/trends/answer/4365533

### Google Keyword Planner

https://ads.google.com/home/tools/keyword-planner/

用途：
估计关键词平均月搜索次数。

访问相关功能可能需要完成
Google Ads 账户及计费资料设置。

来源：
https://support.google.com/google-ads/answer/7337243

不将广告主 CPC 当作网站 AdSense RPM。

### Google Search Console

https://support.google.com/webmasters/answer/7576553

用途：
衡量已验证自有站点的
展示量、点击量、查询词等指标。

现有 go-dev 数据可作为参考，
但不能直接推算其他领域搜索规模。

## 八、证据状态

| 指标 | 状态 |
| --- | --- |
| 固定 66 门语言来源 | VERIFIED |
| 部分目标语言存在译本 | VERIFIED |
| 译本完整性及质量 | UNKNOWN |
| 66 门语言整体覆盖 | UNKNOWN |
| 关键词平均月搜索量 | UNKNOWN |
| Google Trends 相对需求 | NOT_MEASURED |
| AdSense Page RPM | UNKNOWN |
| 长期广告净收益 | UNKNOWN |

## 九、下一步

GOOGLE_TRENDS_DEMAND_PILOT

选择少量代表性搜索主题，
在同一地区及相同时间范围内
比较相对搜索兴趣。

优先从 Google 搜索适用的市场开始。

中国大陆市场需结合其他搜索平台，
不能简单依赖 Google Trends 代表全部需求。

如果无可靠测量结果，
继续标记 UNKNOWN，不编造数值。

不启动翻译、建站或部署。
不修改 go-dev v2。
