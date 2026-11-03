# 项目级商业可行性门槛 001

核实日期：2026-11-03
阶段：PROJECT_LEVEL_COMMERCIAL_FEASIBILITY_GATES
状态：RESEARCH_ONLY
第二个正式项目：NOT_DECIDED

## 一、研究对象

当前重点比较四类完整项目：

1. 国家、地理知识及交互式工具。
2. 世界历史与人文知识体系。
3. Shopify开发者学习与文档体系。
4. Rust完整学习与文档体系。

它们不是永久封闭候选名单。

Python、AI、OWASP、Ethereum、
其他开放数据与人文方向继续保留。

四个项目的排序不代表
预计广告收益或正式建设优先级。

## 二、商业决策范围

以整个66-locale项目为决策单位。

其中62个locale支持Google广告，
4个不支持，沿用已有核实结果。

不得修改冻结locale顺序。

可以分批调查市场，
但不能将少量语言样本
冒充完整66-locale市场结论。

跨地区语言替代必须单独考虑。

完整项目研究不等于
要求正式上线时一次完成66个版本。

## 三、六道商业门槛

G1：内容及数据商业授权

调查每个实际来源的许可、
翻译修改、独立托管、署名、
商标及第三方素材限制。

G2：长期真实需求

确认项目在整个目标语言范围内
存在可持续的搜索或工具使用需求。

不得使用单个Google Trends指数
替代整个项目的市场需求。

G3：有效供给缺口

核查官方、社区和成熟竞争网站
是否已经满足相关用户需求。

UNKNOWN不是已验证缺口。

G4：独立用户价值

确认能够提供比现有供给
更有价值的内容、导航、练习、
查询、比较或其他功能。

不能仅凭翻译页面数量
认定具有搜索竞争优势。

G5：开发与维护成本

考虑源内容范围、持续更新、
质量审核、版本迁移、
多语言共享及长期机会成本。

必须避免影响go-dev v2。

G6：可变现流量及净收益

调查独立站可获取的自然流量，
而不只是整个领域搜索热度。

Google广告支持不等于
网站自动通过AdSense审核。

实际Page RPM缺乏数据时为UNKNOWN。

最终以长期合法广告净收益为目标。

## 四、四个项目当前判断

### GEO：地理与交互式工具

授权：
Natural Earth地图数据公共领域；
Wikidata结构化数据CC0。

VERIFIED，仅限相应数据范围。

全球内容竞争：PARTIALLY_VERIFIED。
66-locale有效功能缺口：UNKNOWN。
独立工具差异化：UNKNOWN。
实际开发维护成本：UNKNOWN。
长期广告净收益：UNKNOWN。

决策：RESEARCH_CONTINUE。

主要问题：
现有工具尚未满足什么具体需求？
这些需求能否在多个目标语言市场
形成长期可变现流量？

### HIS：世界历史与人文知识

授权：
部分开放教材正文为CC BY 4.0。

具体来源：
https://www.openbookpublishers.com/books/10.11647/obp.0074

插图及第三方材料需单独核查。

整个历史知识体系的合法内容源：
NOT_YET_ESTABLISHED。

已有大型历史内容网站：
VERIFIED。

独立站可获取流量：UNKNOWN。
多语言内容竞争缺口：UNKNOWN。
长期广告净收益：UNKNOWN。

决策：RESEARCH_CONTINUE。

主要问题：
能否用合法、可信、长期稳定的
内容和数据形成有价值的完整知识体系？

### SHP：Shopify完整开发者文档

完整研究范围：
Apps、Storefronts、APIs、
CLI/SDK及Agents等开发者内容。

https://shopify.dev/docs

限定来源：
https://github.com/Shopify/theme-liquid-docs

部分仓库的MIT许可已有证据。

整个shopify.dev开发文档体系
商业翻译与独立再分发授权：
UNCLEAR。

Shopify服务及API许可条款
不能自动视为文档转载授权。

https://www.shopify.com/legal/terms
https://www.shopify.com/legal/api-terms

66-locale有效覆盖：UNKNOWN。
独立站可获取流量：UNKNOWN。
长期广告净收益：UNKNOWN。

决策：LICENSE_GATE_FIRST。

未经明确许可，
不启动官方完整文档翻译路线。

如主要官方文档不能合法复用，
可另行研究原创教程路线，
但需要重新评估开发成本与竞争价值。

### RST：Rust完整学习体系

Rust Book授权：
MIT / Apache-2.0。

https://github.com/rust-lang/book

Rust完整学习体系涉及
Book、Rust By Example、Cargo、
Reference、Rustlings、Nomicon等模块。

各来源授权必须分别核实。

已有社区译本：VERIFIED。
完整有效覆盖：UNKNOWN。
官方未来补齐风险：UNKNOWN。
持续更新成本：UNKNOWN。
可获取自然流量：UNKNOWN。

决策：RESEARCH_CONTINUE。

主要问题：
在整个66-locale范围内，
哪些真实内容缺口尚未被现有译本满足？

## 五、共同的搜索与广告风险

Google Search垃圾内容政策：
https://developers.google.com/search/docs/essentials/spam-policies

Google复制内容广告政策：
https://support.google.com/publisherpolicies/answer/11190248

即使内容商业授权明确，
仍须提供实质性用户价值。

批量翻译不自动产生SEO优势，
也不自动获得广告展示资格。

不得将搜索兴趣指数、
语言数量或文档数量
当成预计广告收入。

## 六、当前项目门槛结果

| 项目 | G1授权 | G2需求 | G3缺口 | G4价值 | G5成本 | G6回报 |
| --- | --- | --- | --- | --- | --- | --- |
| GEO | PARTIAL | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| HIS | PARTIAL | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| SHP | UNCLEAR | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| RST | PARTIAL | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

PARTIAL：
只核实部分实际数据或内容源。

UNCLEAR：
存在决定性的授权范围疑问。

UNKNOWN：
缺少足够证据作出确定判断。

本表不代表各项目的商业排名。

四个项目均未通过正式建设门槛。

第二项目：NOT_DECIDED。

## 七、继续调查的成本控制

优先调查能够明显改变决策的阻碍。

避免：
- 为66门语言重复核查已确认的广告支持情况。
- 继续无限扩充单个关键词样本。
- 将每个UNKNOWN强行填写为估算。
- 在版权边界不清时开始完整翻译。
- 过度设计第二套多语言工程。

不因为已经积累研究成果，
就认为必须启动第二项目。

## 八、下一阶段

SHOPIFY_MODULE_LICENSE_SCOPE_SCREENING

选择Shopify作为下一项
低成本前置阻碍验证，
不代表Shopify是商业排名第一。

只核查主要模块是否存在明确
允许商业翻译和独立再分发的
官方内容源或许可依据。

若仍然UNCLEAR，
明确保留阻碍并停止继续追查，
转而调查其他候选的需求缺口。

不要对全部页面逐项爬取，
不要启动正式翻译。

继续保持RESEARCH_ONLY。

go-dev v2仍然是当前主项目。
