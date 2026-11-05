# OWASP 三主题译本竞争与搜索意图缺口试点 001

核实时间（UTC）：2026-11-05T06:36:35.281194+00:00
阶段：OWASP_TRANSLATION_COMPETITION_AND_SEARCH_INTENT_GAP_PILOT
状态：RESEARCH_ONLY
第二项目：NOT_DECIDED

## 一、研究范围

三篇原始安全指南：SQL、XSS、Authentication。
正文抽样语言：英语、简体中文、日语。
目标项目仍为66 locales。

本轮未调查全部66 locales。

## 二、同源内容存在性

| 主题 | locale | 网页 | 正文存在 | 版本状态 |
| --- | --- | --- | --- | --- |
| SQL | en | https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html | VERIFIED | CURRENT_SOURCE |
| SQL | zh-CN | https://cheatsheetseries.owasp.ac.cn/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html | VERIFIED | UNKNOWN |
| SQL | ja-JP | https://jpcertcc.github.io/OWASPdocuments/CheatSheets/SQLInjectionPrevention.html | VERIFIED | HISTORICAL_V1 |
| XSS | en | https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html | VERIFIED | CURRENT_SOURCE |
| XSS | zh-CN | https://cheatsheetseries.owasp.ac.cn/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html | VERIFIED | UNKNOWN |
| XSS | ja-JP | https://jpcertcc.github.io/OWASPdocuments/CheatSheets/XSSPrevention.html | VERIFIED | HISTORICAL_V1 |
| AUTH | en | https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html | VERIFIED | CURRENT_SOURCE |
| AUTH | zh-CN | https://cheatsheetseries.owasp.ac.cn/cheatsheets/Authentication_Cheat_Sheet.html | VERIFIED | UNKNOWN |
| AUTH | ja-JP | https://jpcertcc.github.io/OWASPdocuments/CheatSheets/Authentication.html | VERIFIED | HISTORICAL_V1 |

九个网页已通过HTTP及正文字符存在性检查。
JSON保存网页哈希、字节数与核查结果。

字符数量不能证明全文完整或翻译质量。
不同版本的章节数量也不能直接比较。

## 三、中文竞争

中文站点：
https://cheatsheetseries.owasp.ac.cn/

SQL、XSS、Authentication均存在中文正文。
但内容是否与当前官方英文版同步：UNKNOWN。

网站与OWASP官方的关系：UNCLEAR。
官方链接收录状态：UNKNOWN。

ZH_CN_SAME_SOURCE_BODY=VERIFIED
ZH_CN_EXACT_COMPLETENESS=UNKNOWN
ZH_CN_VERSION_SYNC=UNKNOWN

## 四、日语历史译本

JPCERT/CC维护的历史译本入口：
https://jpcertcc.github.io/OWASPdocuments/

三篇均存在日语正文。
网站明确说明属于迁移前V1快照，
页面出现自2016年起未更新的提示。

JA_JP_HISTORICAL_TRANSLATIONS=VERIFIED
JA_JP_CURRENT_TRANSLATION_COVERAGE=UNKNOWN

历史版本不应计为最新完整译本。
但也不能因此认定市场一定需要新译本。

## 五、其他语言证据边界

已发现西班牙语OWASP Developer Guide：
https://devguide.owasp.org/es/

Developer Guide与Cheat Sheet Series
不是同一个文档体系。

不能将前者翻译计为后者的同源覆盖。

本轮未穷尽调查法语、西班牙语及其他语言。
OTHER_LOCALES_EXACT_COVERAGE=UNKNOWN

## 六、搜索意图调查框架

SQL：参数化查询、SQL注入预防。
XSS：输出编码、跨站脚本防御。
AUTH：安全身份认证、多因素认证。

这些是待验证搜索意图，不是搜索量。

对应的替代竞争包括官方文档、
PortSwigger安全学院及其他安全教程。

https://portswigger.net/web-security

必须区分防御实践与攻击测试学习意图。

SEARCH_INTENT_HYPOTHESES=3
ABSOLUTE_SEARCH_VOLUME=UNKNOWN
LOCALIZED_SERP_RANKINGS=UNKNOWN
ORGANIC_TRAFFIC=UNKNOWN
PAGE_RPM=UNKNOWN
NET_AD_PROFIT=UNKNOWN

## 七、商业判断

已确认中、日语存在同源译本竞争。
其中日语样本明显属于历史版本。

译本时效性是潜在差异化方向，
但持续安全审核也会增加维护成本。

目前没有足够的搜索流量和广告收益证据
证明独立多语言网站值得启动。

OWASP_STATUS=RESEARCH_CONTINUE
SECOND_PROJECT=NOT_DECIDED

## 八、下一步及停止线

NEXT=OWASP_SEARCH_DEMAND_DIFFERENTIATION_STOP_GATE

仅检验少量语言市场的实际搜索需求、
搜索意图与独立网站差异化可能性。

如果没有发现可以改变商业决策的证据，
则暂停OWASP连续深入调查。

不启动翻译、不创建网站、不修改go-dev。
