# Shopify 合法翻译与官方链接模块覆盖调查 001

核实日期：2026-11-04
状态：RESEARCH_ONLY
阶段：SHOPIFY_LICENSED_VS_EXTERNAL_MODULE_COVERAGE
正式项目：NOT_DECIDED

## 一、调查目标

研究完整 Shopify 开发者学习体系中：

- 哪些资料有明确商业翻译许可。
- 哪些学习环节需要链接官方。
- 合法资料是否足够形成有价值的本站内容。

采用既定策略：

LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS

不要求原创补齐。
不等待 Shopify 整站统一授权。
不翻译没有明确授权的官方网页。

目标范围：冻结的66个locale。
广告支持范围：沿用62/4结论。

## 二、已核实的官方源码仓库

| 来源 | 核实commit | 仓库许可 |
| --- | --- | --- |
| theme-liquid-docs | f7a1b07e | MIT |
| shopify-app-js | 9ad9d704 | MIT |
| hydrogen | 5c721108 | MIT |
| cli | 1fc6b148 | MIT |
| theme-extension-getting-started | 8e83d541 | MIT |
| shopify-ai-toolkit | a3d20f8d | MIT |

来源：

https://github.com/Shopify/theme-liquid-docs
https://github.com/Shopify/shopify-app-js
https://github.com/Shopify/hydrogen
https://github.com/Shopify/cli
https://github.com/Shopify/theme-extension-getting-started
https://github.com/Shopify/shopify-ai-toolkit

已核实各仓库根目录的许可证文本。

许可证允许符合条件的商业复制、
修改及分发，并要求保留版权
和许可声明。

这些许可仅适用于实际被覆盖的内容。

不自动覆盖外部网页、图片、
商标或其他许可证例外。

## 三、Apps

开放资料：

shopify-app-js

具体目录：
packages/apps/shopify-api/docs/guides/

已观察到10个Markdown指南，
包括OAuth、Webhooks、Billing、
Session Storage等。

另有API客户端和应用框架资料。

theme-extension-getting-started
提供应用扩展示例。

但部分示例及教程可能对应旧版本，
必须检查当前适用性。

完整应用创建、开发、部署与发布：
尚无完整合法内容覆盖证据。

官方入口：
https://shopify.dev/docs/apps

结论：PARTIAL_VERIFIED。
缺失环节：EXTERNAL_LINK。

## 四、Storefronts / Themes / Liquid

开放资料：

theme-liquid-docs

具体内容：

data/filters.json
data/tags.json
data/objects.json

具有明确的结构化参考资料。

Theme Extension仓库
也提供部分可研究的代码示例。

但完整主题开发、发布、
性能优化及全部主题功能教程，
不能由上述资料证明已经覆盖。

官方入口：
https://shopify.dev/docs/storefronts/themes

结论：PARTIAL_VERIFIED。
缺失环节：EXTERNAL_LINK。

## 五、Hydrogen / Headless

开放资料：

hydrogen

已观察到：

- README及开发说明
- 20个Hydrogen技能目录
- 开发示例与模板
- 部分生成的技术参考内容

这些资料与Hydrogen实际实现关联紧密。

但AI Agent技能不是
面向普通开发者的完整教材。

当前主分支对应新的
2026-10 Hydrogen开发体系。

历史教程和旧框架版本
必须分开处理。

官方入口：
https://shopify.dev/docs/storefronts

结论：PARTIAL_VERIFIED。
缺失环节：EXTERNAL_LINK。

## 六、APIs

开放资料：

shopify-app-js中的API客户端、
使用指南和参考文件。

hydrogen中的Storefront API
客户端与相关技术资料。

shopify-ai-toolkit中的
部分GraphQL和API开发参考。

但不能据此认为：

Admin、Storefront、Customer Account、
Functions、Payments及其他API
的完整官方Reference
均获得独立转载授权。

官方入口：
https://shopify.dev/docs/api

结论：PARTIAL_VERIFIED。
完整API参考：EXTERNAL_LINK。

## 七、Tools / CLI

开放资料：

cli

已观察到：

docs/cli/ 下15个Markdown文件。

另外存在：

docs-shopify.dev/generated/

需要特别注意：

部分docs/cli文件主要用于
CLI项目贡献者和内部开发，
并非面向Shopify应用开发者的教程。

不能将这15个文件直接算成
15篇可用于本站的终端用户教材。

官方入口：
https://shopify.dev/docs/api

结论：PARTIAL_VERIFIED。
面向用户的完整教程：UNKNOWN。
缺失环节：EXTERNAL_LINK。

## 八、Agents

开放资料：

shopify-ai-toolkit

当前仓库采用MIT许可。

已观察到：

skills/shopify/references/

其中有23个Markdown参考文件，
覆盖部分Shopify开发领域。

另有UCP相关技能资料。

主要用途是指导AI开发工具，
不能等同于完整的人类学习课程。

注意：

Shopify/agent-skills是另一个仓库，
本轮没有找到仓库根目录LICENSE。

不得把shopify-ai-toolkit的MIT许可
套用至agent-skills。

官方入口：
https://shopify.dev/docs/agents

结论：PARTIAL_VERIFIED。
完整Agents学习教程：EXTERNAL_LINK。

## 九、覆盖结果

| 模块 | 有授权资料候选 | 完整本站学习覆盖 |
| --- | --- | --- |
| Apps | YES | UNKNOWN |
| Themes / Liquid | YES | UNKNOWN |
| Hydrogen | YES | UNKNOWN |
| APIs | YES | UNKNOWN |
| Tools | YES | UNKNOWN |
| Agents | YES | UNKNOWN |

六个模块均有至少一个
可进一步核查的开放资料来源。

但这不意味着六个模块都已经
具有完整、当前、适合学习的译文来源。

完整学习节点数量：UNKNOWN。
合法可翻译节点数量：UNKNOWN。
必须外链节点数量：UNKNOWN。

因此暂不计算翻译覆盖百分比。

不能用仓库数、技能目录数、
JSON条目数代替学习页面数。

## 十、商业可行性判断

决定：
CONDITIONAL_CONTINUE

采用：

授权翻译 + 官方链接。

无需原创教程补齐。

现阶段获得的积极证据：

1. 合法内容来源不仅限于Liquid。
2. Apps、APIs、CLI等也有部分开放文档。
3. Hydrogen存在较广的开发资料。
4. Agents有部分MIT授权资料。

主要风险：

1. 多数资料只是局部模块。
2. 部分资料面向库维护者或AI。
3. 技术内容版本变化频繁。
4. 外部链接不形成本站内容PV。
5. 官方搜索竞争较强。
6. 66-locale有效需求缺口仍未确认。

合法内容主体是否足够有价值：
UNKNOWN。

独立站长期可获取流量：
UNKNOWN。

Page RPM：UNKNOWN。
长期广告净收益：UNKNOWN。

本轮没有批准正式开发。

## 十一、下一阶段

SHOPIFY_PROJECT_LEVEL_DEMAND_FEASIBILITY_SCREEN

下一轮不再简单增加开源仓库数量。

应从整个66-locale项目角度调查：

- 有授权的参考资料是否对应真实搜索意图。
- 目标语言现有免费学习资源的竞争。
- 用户是否愿意访问独立翻译网站。
- 官方链接占比较高时的流量损失。
- 长期更新及质量审核的总体成本。

如缺少明显可获取流量机会，
及时停止深入调查。

不启动大规模翻译。
不编写原创教材。
不建立正式网站。
不修改go-dev v2。
