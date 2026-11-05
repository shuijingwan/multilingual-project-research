# 跨领域长期商业候选比较 001

核实日期：2026-11-05
阶段：CROSS_DOMAIN_CANDIDATE_COMPARISON
状态：RESEARCH_ONLY
项目目标：LONG_TERM_AD_NET_PROFIT
目标范围：66 locales
正式新项目：NOT_DECIDED

## 一、研究方法

本轮复用已归档研究证据，不重新搜集市场数据。
九个候选研究深度不相同，不进行收入排名。
PAUSED不等于REJECTED，OPEN不等于优先开发。

六道门槛：
G1合法授权；G2长期需求；G3有效竞争缺口；
G4独立用户价值；G5工程维护成本；
G6可获取自然流量与长期广告净收益。

## 二、统一比较矩阵

| ID | 候选方向 | 状态 | 授权基础 | 需求证据 | 核心障碍 |
| --- | --- | --- | --- | --- | --- |
| GEO | 地理交互工具 | PARKED | 部分开放数据许可明确 | PARTIAL | 缺乏可持续的功能差异化 |
| HIS | 世界历史与人文教材 | PAUSED | 三本具体教材许可明确 | PARTIAL | 具体教材需求与可获取流量 |
| SHP | Shopify开发文档 | PAUSED | 部分模块明确；官方整体不明确 | PARTIAL | 合法内容的独立搜索竞争力 |
| RST | Rust完整学习体系 | PAUSED | 六模块主要来源已核查 | PARTIAL | 新网站可获取自然流量 |
| OWASP | OWASP安全指南 | OPEN | Cheat Sheet Series采用CC BY-SA 4.0 | UNKNOWN | 专题搜索需求与有效译本缺口 |
| PY | Python官方学习资料 | OPEN | PSF许可证；具体素材待核查 | PARTIAL | 独立翻译站的差异化 |
| AI | AI基础与应用教育 | OPEN | 微软特定教程仓库采用MIT | PARTIAL | 已有大量翻译之外的实际价值 |
| ETH | Ethereum与合约开发 | OPEN | ethereum.org部分明确；其他待核查 | UNKNOWN | 具体来源许可与开发者需求 |
| DATA | 开放统计数据比较工具 | OPEN | 部分数据源CC0或CC BY 4.0 | UNKNOWN | 长期用户查询需求与差异化 |

PARTIAL仅代表存在局部需求线索，
不是完整项目市场需求已得到验证。

## 三、竞争与维护成本

| 候选 | 已知竞争情况 | 维护判断 |
| --- | --- | --- |
| GEO | 竞品已核实；独特价值未证实 | UNKNOWN |
| HIS | 同源及替代竞争已部分核实 | UNKNOWN |
| SHP | 已有官方与第三方供给 | 版本更新风险较高（ESTIMATE） |
| RST | 四市场竞争者已核实 | 持续版本维护（ESTIMATE） |
| OWASP | 已有安全参考资料竞争 | 重大安全更新不能延迟 |
| PY | 官方与第三方教程已存在 | 持续版本维护（ESTIMATE） |
| AI | 已有50多语言的课程翻译 | 技术更新较快（ESTIMATE） |
| ETH | 官方多语言与社区资料已存在 | 安全及版本维护风险 |
| DATA | 具体功能竞争尚未充分核实 | 数据更新及工具开发成本待估 |

维护判断中的ESTIMATE仅为定性风险。
不得解释为已经测量的工程成本。

## 四、共同商业证据缺口

全部候选都尚未证明：

- 66-locale整体有效市场需求。
- 足够明确的独立搜索竞争优势。
- 可以长期获得的自然搜索点击。
- 可验证的Page RPM及广告净收益。
- 投入和维护成本能被收益覆盖。

ORGANIC_TRAFFIC=UNKNOWN
PAGE_RPM=UNKNOWN
NET_AD_PROFIT=UNKNOWN
COMMERCIAL_RANKING=NOT_READY

不同候选的许可证只对实际来源成立。
不得把某个开源仓库的许可扩展到完整官网。
AdSense准入也不能从版权许可直接推出。

## 五、阶段性决策

GEO继续PARKED。
HIS、SHP、RST暂停连续深入研究，保留候选。
其他方向仍允许开展低成本专项调查。

本轮不批准任何正式新项目。
也不依据已有研究投入决定开发顺序。

## 六、下一轮研究选择

建议选择OWASP Cheat Sheet Series进行轻量试点。

理由：

1. 已有明确的具体授权来源。
2. 可以按具体安全主题调查长期查询需求。
3. 可以检查官方与社区译本的有效覆盖。
4. 初期不需要建设网站或翻译基础设施。

这只是研究轮换选择，不代表OWASP收益最高。
应同时保留开放统计数据工具等非技术候选。

OWASP下一轮仅选择少量代表性Cheat Sheets，
核查搜索意图、已有竞争、翻译覆盖及维护负担。
必须检查CC BY-SA相同方式共享、署名及素材例外。

若无法找到具体用户价值或流量证据，
应及时停止专项调查，不无限扩张研究范围。

NEXT=OWASP_SOURCE_SPECIFIC_DEMAND_AND_COVERAGE_PILOT
SECOND_PROJECT=NOT_DECIDED

## 七、证据追溯

- RST: research/2026-11-05-rst-search-competition-traffic-proxy-pilot-001.md (SHA-256: 9f98902ba37942f8a5ab77c33ec8c6ead2cb1240c1e119924593a0bb60a4408b)
- GEO: research/2026-11-04-geo-specific-user-value-gap-check-001.md (SHA-256: 49d8124fef38dfb69371ce586a898ca491a4216dd9199a501cd224eb4b7d383d)
- HIS: research/2026-11-04-his-source-specific-translation-coverage-pilot-001.md (SHA-256: f0b54a0a51e4888bd7b44a8c800e0ee8248eb4377a2c417f232127191a3377b0)
- SHP: research/2026-11-04-shopify-project-level-demand-feasibility-screen-001.md (SHA-256: 5d027a6e836493de5010ee70bc3ab72519ed46a85922cf5fb2aa7832d1838325)
- CROSS: research/2026-11-03-cross-domain-commercial-evidence-001.md (SHA-256: 5508ea5da2941304887de9fb1884daae23057a6f060032d5ed07845e8b2fc5ae)
- POOL: research/2026-11-04-cross-project-candidate-pool-review-001.md (SHA-256: d4adbd8921b6cda1c02102ec403c44abee4b7474207c0ec534db52b7333ddcd4)
- GATES: research/2026-11-03-project-level-commercial-feasibility-gates-001.md (SHA-256: 8d9962343b58c046ac779732a35ad916b0a6cdab8b59d7804925528539c8bcd0)
- TRENDS: research/2026-11-03-google-trends-search-interest-pilot-001.md (SHA-256: 9c08a0adfb39006c52cdc6c8f9257507973743982ea16cb9006142914eac0764)

补充官方来源：

- https://github.com/OWASP/CheatSheetSeries/blob/master/LICENSE.md
- https://github.com/microsoft/generative-ai-for-beginners
- https://datacatalog.worldbank.org/public-licenses

保持RESEARCH_ONLY。
不启动翻译、不创建网站、不修改go-dev v2。
