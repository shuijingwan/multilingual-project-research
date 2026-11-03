# 跨目标语言有效内容缺口抽样 001

核实日期：2026-11-03
状态：RESEARCH_ONLY
阶段：CROSS_LOCALE_EFFECTIVE_GAP_SAMPLING
正式项目：NOT_DECIDED

## 一、研究范围

从冻结的66个locale中抽样：

- fr-FR：法语
- id-ID：印尼语
- vi-VN：越南语
- hi-IN：印地语

上述locale均在既定Google广告支持范围内。

本轮仅检查少量官方及社区内容来源，
不是66个locale的完整覆盖审计。

最终商业目标为长期广告净收益。

## 二、Python官方文档

来源：
https://translations.python.org/

按Python官方仪表盘核实：

| locale | core | overall |
| --- | ---: | ---: |
| fr-FR | 28.21% | 22.23% |
| id-ID | 46.70% | 2.86% |
| vi-VN | 44.44% | 1.29% |
| hi-IN | 0.00% | 0.01% |

状态：VERIFIED。

core代表特定核心模块，
overall代表整套文档。

翻译完成率较低，
说明官方尚未完成全部文档。

但官方已有翻译流程与贡献者。

第三方教程供给、未来扩张风险、
可获取自然流量继续为UNKNOWN。

不得因官方文档不完整
直接决定独立翻译建站。

## 三、Rust Book社区翻译

来源：
https://doc.rust-lang.org/book/appendix-06-translation.html

官方目录已列出：

- 法语
- 越南语
- 印地语

当前目录未列出印尼语。

状态：VERIFIED。

该目录记录的是社区译本，
不代表官方完整托管或保证更新质量。

印尼语未列出，
不代表整个互联网没有印尼语教程。

完整Rust学习体系的有效覆盖：
UNKNOWN。

## 四、Ethereum官方开发文档

当前官方语言配置：
https://github.com/ethereum/ethereum-org-website/blob/dev/i18n.config.json

已核实四门语言开发文档入口：

法语：
https://ethereum.org/fr/developers/docs/

印尼语：
https://ethereum.org/id/developers/docs/

越南语：
https://ethereum.org/vi/developers/docs/

印地语：
https://ethereum.org/hi/developers/docs/

状态：VERIFIED。

四门语言均有本地化开发文档入口。

完整章节覆盖和版本同步：
UNKNOWN。

不能仅因为目标locale存在，
就认定官方文档已经全部翻译。

## 五、世界历史竞争与商业授权

World History Encyclopedia翻译目录：
https://www.worldhistory.org/trans_/

本轮核实的目录数据：

- 法语：4830篇译文
- 印尼语：150篇译文
- 印地语：11篇译文
- 越南语：未列入该目录

该目录列出48种翻译语言。

这些只是单一竞争网站的统计。

越南语未列出不等于
越南语世界历史资料不存在。

官网商业资料：
https://www.worldhistory.org/static/about/

官方公布2024年页面浏览量
约8931万，并说明其经营模式
包括广告、会员和捐赠。

状态：VERIFIED，官方自报。

这不是新网站可复制的收入预测。

网站版权及使用条款：
https://www.worldhistory.org/static/terms-of-use/

该站通常采用带有NonCommercial
限制的Creative Commons许可。

条款还明确限制大规模转载，
包括通过翻译进行的再发布。

因此不得直接使用该站文章
建设商业广告翻译网站，
除非另外取得明确有效的授权。

世界历史仍可继续研究，
但应优先寻找商业使用许可清晰的
开放教材、公开数据或原创内容路线。

## 六、地理交互式工具

印尼语现有工具：
https://www.dodothinks.online/id/

越南语现有工具：
https://flagquizzes.com/vi/capitals/world/

印地语现有工具：
https://mapnesia.com/hi/

状态：VERIFIED。

上述网站提供相应语言的
地理、国家、首都或地图练习内容。

法语及四门语言的完整市场覆盖：
UNKNOWN。

这些例子证明：
不能直接假设非英语地理市场
缺少互动产品。

需要调查具体功能缺口，
而不是机械翻译一个已有工具。

## 七、跨领域综合结论

Python：
官方覆盖差异显著，
但部分语言存在持续翻译机制。

Rust：
存在社区翻译，
官方目录不是整个市场的完整清单。

Ethereum：
抽样四门语言已有官方文档入口。

世界历史：
发现明确的多语言市场供给、
官方报告的可观流量和广告经营实践，
但所调查竞争网站的文章
不适合未经授权用于商业翻译。

地理工具：
抽样语言存在交互式竞争供给。

## 八、尚未获得的数据

以下全部保持UNKNOWN：

- 对应语言的实际关键词月搜索量。
- 新建独立网站可获取的自然流量。
- 各语言全部竞争网站的有效覆盖。
- 历史开放教材在四门语言中的译本覆盖。
- 候选项目的实际Page RPM。
- 预计广告收入及长期净收益。

不通过名义语言差额推算市场规模。

## 九、下一阶段

LOCALE_TOPIC_OPPORTUNITY_SHORTLIST

从已调查领域中选择少量
具有明确内容范围和实际用户意图的
locale-topic组合继续深入研究。

优先考虑：

1. 搜索需求有证据。
2. 具体内容供给缺口有证据。
3. 商业授权明确。
4. 官方替代风险可接受。
5. 开发及维护成本可控。

不要求强行选定第二个项目。

66-locale范围与顺序不变。
62/4广告支持结论直接沿用。

不启动翻译、建站或部署。
不修改go-dev v2。
