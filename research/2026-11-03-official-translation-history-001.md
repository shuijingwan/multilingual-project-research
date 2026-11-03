# 官方翻译覆盖历史变化核实 001

核实日期：2026-11-03
状态：RESEARCH_ONLY
正式立项：NONE

## 一、研究目的

评估官方未来补齐语言的竞争风险。

只使用可复核的历史快照，
不把翻译语言数量当作商业成功指标。

固定66个locale及既有排序不变。
62/4广告支持范围不重复调查。

## 二、Ethereum：语言配置收缩

官方仓库：
https://github.com/ethereum/ethereum-org-website

历史快照：
2025-11-03T17:37:25Z
commit:
cb085937d5ef210115f4830d272ad4442effb1e1
i18n.config.json：69个语言配置（含英语）
blob SHA：
0a934d637e78398fa5fdb534c6a4f814bb038f61

当前快照：
2026-11-03，dev分支
i18n.config.json：25个语言配置（含英语）
blob SHA：
bc5e72fa8b143d83017fe5850b7b53c1f1096e04

VERIFIED：
配置数量由69减少至25，净减少44。

历史源码：
https://github.com/ethereum/ethereum-org-website/blob/cb085937d5ef210115f4830d272ad4442effb1e1/i18n.config.json

当前源码：
https://github.com/ethereum/ethereum-org-website/blob/dev/i18n.config.json

官网翻译计划：
https://ethereum.org/contributing/translation-program/

注意：
配置减少不等于历史译文全部删除。
官方仍说明过去的翻译工作保留在网站中。

具体收缩原因及未来是否扩张：
UNKNOWN。

## 三、Microsoft：语言入口增长

官方仓库：
https://github.com/microsoft/generative-ai-for-beginners

历史快照：
2025-10-24T11:43:57Z
commit:
08b689b1c597886b46f47a3c670afe257a946a30
README翻译入口：49个
blob SHA：
98b76798077513494dacdf823672d9f16ddd5a1f

当前快照：
2026-11-03，默认分支
README翻译入口：54个
blob SHA：
92cc3d51203d4087685202b2299901914b864001

历史源码：
https://github.com/microsoft/generative-ai-for-beginners/blob/08b689b1c597886b46f47a3c670afe257a946a30/README.md

当前源码：
https://github.com/microsoft/generative-ai-for-beginners/blob/main/README.md

VERIFIED：
入口数量净增加5。

但部分语言代码进行了规范化，
不能直接认定新增5种完全不同的语言。

课程翻译完整性：UNKNOWN。
具体新增语言的有效覆盖：UNKNOWN。

官方已有自动化翻译维护机制。
对第三方重复翻译构成竞争风险，
但未来扩张概率仍为UNKNOWN。

## 四、Rust Book：社区译本目录扩展

官方仓库：
https://github.com/rust-lang/book

历史快照：
2025-10-19T01:17:58Z
commit:
2a103c67e0e946772182db84fc911dfe9fb812d7
目录条目：22

当前快照：
2026-11-03，默认分支
目录条目：25

新增目录项：
乌兹别克语、越南语、孟加拉语。

历史源码：
https://github.com/rust-lang/book/blob/2a103c67e0e946772182db84fc911dfe9fb812d7/src/appendix-06-translation.md

当前源码：
https://github.com/rust-lang/book/blob/main/src/appendix-06-translation.md

VERIFIED：
社区译本目录增加3条。

不能据此认定新增3个完整官方译本。
目录项也不代表质量或更新情况。

## 五、Python：尚无可比年度快照

官方仪表盘：
https://translations.python.org/

已核实：
2026-11-02的近期翻译完成率，
以及仪表盘公布的30天百分点变化。

但本轮没有取得
12个月前同口径的完整历史快照。

年度语言扩张趋势：UNKNOWN。

不能将近期30天增幅直接年化。

## 六、商业解释

本轮已观察到：

- Ethereum：配置数量明显收缩。
- Microsoft：翻译入口净增长。
- Rust Book：社区目录继续扩展。
- Python：存在近期翻译进度，但年度趋势未知。

官方多语言覆盖并非必然单向增长。

未来替代风险必须按项目评估。

不因官方曾支持很多语言，
直接认定其未来一定继续扩张。

不因官方当前暂停翻译，
直接认定缺口可以长期存在。

不根据上述历史记录推算广告收入。

## 七、研究停止线

本轮历史核实已取得三个项目的
可复核历史与当前快照。

不继续无限追查翻译治理细节。

后续若某项目进入深入调查阶段，
再核实其具体目标语言的长期风险。

下一阶段：
CROSS_DOMAIN_DEMAND_EVIDENCE_PILOT

优先回到跨领域搜索需求、
现有供给缺口及可获取流量研究。

RPM继续保持UNKNOWN。
正式项目继续保持NOT_DECIDED。

不翻译、不建站、不部署。
不修改go-dev v2。
