# 跨领域需求证据试点 001

核实日期：2026-11-03
阶段：CROSS_DOMAIN_DEMAND_EVIDENCE_PILOT
状态：RESEARCH_ONLY

## 一、数据来源及范围

官方数据源：
https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/reference/page-views.html

观察对象：德语维基百科的八篇代表性文章。

统计时间：2025-11 至 2026-10，共12个月。

口径：all-access、user，每月页面浏览次数。

这是德语内容的全球读者浏览量，
不是德国境内的浏览量。

不是 Google 搜索量、搜索点击量、
独立站可获取流量、广告收入或 RPM。

## 二、实际测量结果

| 领域 | 代表主题 | 12个月浏览次数 |
| --- | --- | ---: |
| 编程语言 | Python | 122,429 |
| 编程语言 | Rust | 81,202 |
| AI知识 | 人工智能 | 406,820 |
| 应用安全 | 信息安全 | 26,368 |
| 区块链 | Ethereum | 41,420 |
| 商业开发 | Shopify | 35,596 |
| 世界历史 | 世界历史 | 7,926 |
| 地理知识 | 地理学 | 37,147 |

上述数据是实际观测，不是收入预测。

## 三、解释边界

1. 每个领域只选取一篇百科条目，
   不代表完整领域的用户需求。
2. 浏览量高不代表学习或工具使用需求高。
3. 百科条目的浏览量不代表翻译站可获流量。
4. 文章来源及标题可能影响比较。
5. 热点事件可能造成短期访问量异常。
6. 不同领域不能仅凭此表作商业排名。
7. 未验证对应语言的实际搜索竞争缺口。

## 四、原始数据

原始文件：
`research/evidence/2026-11-03-dewiki-pageviews-001.json`

SHA-256：`b530bc86c096c2dd1c45f7d11dfaafeaf9f15ef51ade0bf8e7fe6e0093594fc0`

原始数据包含每个主题的完整月度值、
统计口径和 Wikimedia API 请求地址。

## 五、商业研究结论

Wikimedia浏览量：VERIFIED。
Google搜索需求：UNKNOWN。
独立站可获得流量：UNKNOWN。
实际Page RPM：UNKNOWN。
长期广告净收益：UNKNOWN。

没有根据百科浏览量选择正式项目。

## 六、下一阶段

GOOGLE_TRENDS_SEARCH_INTEREST_PILOT

在统一地区与时间范围内，
测量不同主题的相对搜索兴趣。

优先选择跨语言语义明确的主题，
并区分一般知识查询与学习/工具查询。

继续比较技术与非技术领域，
不调整66-locale冻结范围。

不创建网站、不启动翻译、
不修改go-dev v2。
