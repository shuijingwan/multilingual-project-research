# Co-op Translator 与世界历史 66 locale 静态兼容性门禁 001

- 核实日期：2026-11-10
- 阶段：CO_OP_TRANSLATOR_66_LOCALE_STATIC_COMPATIBILITY_GATE
- 结果：PARTIAL（代码映射静态清单完成；真实翻译兼容性尚未验证）
- 状态：RESEARCH_ONLY；WORLD_HISTORY 已选择但未获建站或翻译实施授权
- 方法：只读 Go locale 规划文件 + 下载微软官方语言支持 Markdown，按代码严格匹配及保守别名分类

## 1. 范围与证据身份

- Cross-project 目标 = Go 已冻结的 65 community locale + en-US，共 66；来源为 docs/LOCALE_ROADMAP.md，不改动 Go 工程。
- 官方当前 main 分支的 docs/supported-languages.md 中识别到 56 个语言代码。其条目不是 66 项的语言/地区覆盖保证。
- 此处比较的是官方 main 文档；不保证 PyPI 0.24.0 分发包内的数据与 main 完全一致。
- Roadmap SHA-256: b02ae9f7071a2c444ed180848622e410d6ea4185b3d70bcb09ad1af28fa0e18f
- Co-op language table SHA-256: 78210ebd3065ebaa8ef465a399f34bb11184f64703a88b8bac030a036d6db1be

来源：

- https://github.com/Azure/co-op-translator/blob/main/docs/supported-languages.md
- https://github.com/Azure/co-op-translator/blob/main/docs/api.md
- https://github.com/Azure/co-op-translator/blob/main/docs/mcp.md
- 本地只读：go-tour-i18n/docs/LOCALE_ROADMAP.md

## 2. 分类与结论

- DIRECT = 7：目标 locale 字符串与官方表代码一致；仍需验证实测质量。
- BASE_ALIAS_REVIEW = 51：基础语言代码存在，地区变体本身不是同一条目；翻译、地区口音、文件输出、SEO 必须另行审核。
- SPECIAL_REVIEW = 3：不是简单移除地区后可直接匹配，需要显式语言映射和人工批准。
- NO_MATCH = 5：官方表缺少对应基础语言代码；不得称为已支持；未来需要上游扩展、补充配置或独立翻译执行者。

需要专项处理的 3 个 SPECIAL_REVIEW：

- fil-PH → tl：Tagalog/Filipino 语言身份及表述差异不能自动合并。
- nb-NO → no：Norwegian Bokmål 与泛 Norwegian 语言标识需要核对。
- zh-SG → zh-CN：简体中文地区差异与具体词汇需要核对。

官方无对应基础代码的 5 个 NO_MATCH：

- gu-IN（Gujarati）
- ca-ES（Catalan）
- lv-LV（Latvian）
- kk-KZ（Kazakh）
- am-ET（Amharic）

## 3. 完整 66 locale 映射（原始规划顺序）

| 目标 locale | 类型 | Co-op 候选代码 | 处理要求 |
| --- | --- | --- | --- |
| en-US | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| zh-CN | DIRECT | zh-CN | 代码直接匹配；不等于翻译质量已验证 |
| ja-JP | BASE_ALIAS_REVIEW | ja | 地区变体可能合并；需评估用语与路径 |
| de-DE | BASE_ALIAS_REVIEW | de | 地区变体可能合并；需评估用语与路径 |
| fr-FR | BASE_ALIAS_REVIEW | fr | 地区变体可能合并；需评估用语与路径 |
| ko-KR | BASE_ALIAS_REVIEW | ko | 地区变体可能合并；需评估用语与路径 |
| es-ES | BASE_ALIAS_REVIEW | es | 地区变体可能合并；需评估用语与路径 |
| it-IT | BASE_ALIAS_REVIEW | it | 地区变体可能合并；需评估用语与路径 |
| nl-NL | BASE_ALIAS_REVIEW | nl | 地区变体可能合并；需评估用语与路径 |
| pt-BR | DIRECT | pt-BR | 代码直接匹配；不等于翻译质量已验证 |
| tr-TR | BASE_ALIAS_REVIEW | tr | 地区变体可能合并；需评估用语与路径 |
| sv-SE | BASE_ALIAS_REVIEW | sv | 地区变体可能合并；需评估用语与路径 |
| pl-PL | BASE_ALIAS_REVIEW | pl | 地区变体可能合并；需评估用语与路径 |
| zh-TW | DIRECT | zh-TW | 代码直接匹配；不等于翻译质量已验证 |
| id-ID | BASE_ALIAS_REVIEW | id | 地区变体可能合并；需评估用语与路径 |
| vi-VN | BASE_ALIAS_REVIEW | vi | 地区变体可能合并；需评估用语与路径 |
| ar | DIRECT | ar | 代码直接匹配；不等于翻译质量已验证 |
| th-TH | BASE_ALIAS_REVIEW | th | 地区变体可能合并；需评估用语与路径 |
| hi-IN | BASE_ALIAS_REVIEW | hi | 地区变体可能合并；需评估用语与路径 |
| bn-BD | BASE_ALIAS_REVIEW | bn | 地区变体可能合并；需评估用语与路径 |
| ur-PK | BASE_ALIAS_REVIEW | ur | 地区变体可能合并；需评估用语与路径 |
| uk-UA | BASE_ALIAS_REVIEW | uk | 地区变体可能合并；需评估用语与路径 |
| ro-RO | BASE_ALIAS_REVIEW | ro | 地区变体可能合并；需评估用语与路径 |
| cs-CZ | BASE_ALIAS_REVIEW | cs | 地区变体可能合并；需评估用语与路径 |
| ta-IN | BASE_ALIAS_REVIEW | ta | 地区变体可能合并；需评估用语与路径 |
| te-IN | BASE_ALIAS_REVIEW | te | 地区变体可能合并；需评估用语与路径 |
| ms-MY | BASE_ALIAS_REVIEW | ms | 地区变体可能合并；需评估用语与路径 |
| fil-PH | SPECIAL_REVIEW | tl | Filipino/Tagalog 并非完全同一语言规范，需要确认可接受程度 |
| el-GR | BASE_ALIAS_REVIEW | el | 地区变体可能合并；需评估用语与路径 |
| hu-HU | BASE_ALIAS_REVIEW | hu | 地区变体可能合并；需评估用语与路径 |
| bg-BG | BASE_ALIAS_REVIEW | bg | 地区变体可能合并；需评估用语与路径 |
| mr-IN | BASE_ALIAS_REVIEW | mr | 地区变体可能合并；需评估用语与路径 |
| ml-IN | BASE_ALIAS_REVIEW | ml | 地区变体可能合并；需评估用语与路径 |
| kn-IN | BASE_ALIAS_REVIEW | kn | 地区变体可能合并；需评估用语与路径 |
| es-419 | BASE_ALIAS_REVIEW | es | 地区变体可能合并；需评估用语与路径 |
| gu-IN | NO_MATCH | — | 官方表无相应基础语言代码 |
| pa-IN | BASE_ALIAS_REVIEW | pa | 地区变体可能合并；需评估用语与路径 |
| nb-NO | SPECIAL_REVIEW | no | Bokmål 与泛 Norwegian 代码不等价；需要人工核对 |
| da-DK | BASE_ALIAS_REVIEW | da | 地区变体可能合并；需评估用语与路径 |
| fi-FI | BASE_ALIAS_REVIEW | fi | 地区变体可能合并；需评估用语与路径 |
| sr-RS | BASE_ALIAS_REVIEW | sr | 地区变体可能合并；需评估用语与路径 |
| sk-SK | BASE_ALIAS_REVIEW | sk | 地区变体可能合并；需评估用语与路径 |
| hr-HR | BASE_ALIAS_REVIEW | hr | 地区变体可能合并；需评估用语与路径 |
| sl-SI | BASE_ALIAS_REVIEW | sl | 地区变体可能合并；需评估用语与路径 |
| lt-LT | BASE_ALIAS_REVIEW | lt | 地区变体可能合并；需评估用语与路径 |
| ca-ES | NO_MATCH | — | 官方表无相应基础语言代码 |
| et-EE | BASE_ALIAS_REVIEW | et | 地区变体可能合并；需评估用语与路径 |
| lv-LV | NO_MATCH | — | 官方表无相应基础语言代码 |
| sw-TZ | BASE_ALIAS_REVIEW | sw | 地区变体可能合并；需评估用语与路径 |
| kk-KZ | NO_MATCH | — | 官方表无相应基础语言代码 |
| fa-IR | BASE_ALIAS_REVIEW | fa | 地区变体可能合并；需评估用语与路径 |
| am-ET | NO_MATCH | — | 官方表无相应基础语言代码 |
| ru-RU | BASE_ALIAS_REVIEW | ru | 地区变体可能合并；需评估用语与路径 |
| pt-PT | DIRECT | pt-PT | 代码直接匹配；不等于翻译质量已验证 |
| fr-CA | BASE_ALIAS_REVIEW | fr | 地区变体可能合并；需评估用语与路径 |
| zh-HK | DIRECT | zh-HK | 代码直接匹配；不等于翻译质量已验证 |
| de-CH | BASE_ALIAS_REVIEW | de | 地区变体可能合并；需评估用语与路径 |
| de-AT | BASE_ALIAS_REVIEW | de | 地区变体可能合并；需评估用语与路径 |
| zh-SG | SPECIAL_REVIEW | zh-CN | 均为简体中文，但新加坡地区用语需单独审核 |
| en-GB | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| en-CA | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| en-AU | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| en-IN | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| en-SG | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| en-ZA | BASE_ALIAS_REVIEW | en | 地区变体可能合并；需评估用语与路径 |
| he | DIRECT | he | 代码直接匹配；不等于翻译质量已验证 |

## 4. 采用前的边界

- en-US 及其他英语地区必须先按历史教材正式源语言覆盖规则决定是否跳过；存在 en 基础代码不等于必须额外生成 7 个英文地区译本。
- es-419、de-AT、fr-CA 等地区变体的通用语言退化仍需语义和地区风格验收。
- NO_MATCH 不等于理论上完全无法生成译文；只代表本轮官方支持表中未列相应代码。
- 不自动修改 Co-op 内部 fonts/locale 配置；增加语言代码需要单独验证，不将上游主分支或包名视为稳定扩展协议。
- 这不是 Markdown 结构回环/独立 QC/模型翻译的运行测试；TranslationStateProvider 保留人工修改的运行结论仍为 UNKNOWN。
- 未安装 Co-op Translator；未购买或调用 API；未触发 Codex；未启动世界历史工程；未修改 go-dev。

## 5. 门禁与唯一后续验证问题

RESULT=PARTIAL
STAGE=CO_OP_TRANSLATOR_66_LOCALE_STATIC_COMPATIBILITY_GATE
TARGET_LOCALES=66
OFFICIAL_LANGUAGE_CODES=56
DIRECT=7
BASE_ALIAS_REVIEW=51
SPECIAL_REVIEW=3
NO_MATCH=5
GO_DEV_V2_MUTATION=NONE
CO_OP_INSTALLED=NO
CODEX_CALLS=0
RESEARCH_ONLY=YES
FORMAL_PROJECT_SELECTED=WORLD_HISTORY
IMPLEMENTATION_AUTHORIZED=NO
NEXT=ISOLATED_AGENT_ASSISTED_MARKDOWN_ROUNDTRIP_WHEN_DEPENDENCY_COST_APPROVED

最小后续问题：在成本受控的临时环境中，能否用人工提供的原样/模拟译文而不调用模型，借助公开 start/finish Markdown agent-assisted API 完成章节标题、脚注标记、代码和链接的结构回环？先证明这一点，再谈 66 语言翻译与 Fork。
