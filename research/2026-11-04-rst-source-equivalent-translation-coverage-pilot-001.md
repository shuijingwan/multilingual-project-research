# Rust 六模块同源译本覆盖线索抽样 001

核实日期：2026-11-04
阶段：RST_SOURCE_EQUIVALENT_TRANSLATION_COVERAGE_PILOT
状态：RESEARCH_ONLY
目标范围：66 locales
抽样范围：10 locales × 6 modules
第二项目：NOT_DECIDED

## 一、证据边界

本报告记录已核实公开来源所披露的译本线索。
证据采集于2026-11-04，并非执行命令时重新抓取。

DIRECTORY_LISTED：列入官方翻译目录。
EXTERNAL_TRANSLATION_LINKED：官方仓库链接外部译本。
COMMUNITY_EXERCISES_LINKED：列入官方社区练习清单。
PLATFORM_REPORTED：非官方平台报告的翻译进度。
NOT_ESTABLISHED_IN_PILOT：本轮证据不足。

以上状态均不自动证明完整正文、翻译质量或版本同步。
特别是 NOT_ESTABLISHED_IN_PILOT 不等于不存在译本。

## 二、来源

- BOOK: https://doc.rust-lang.org/book/appendix-06-translation.html
- RBE: https://github.com/rust-lang/rust-by-example
- RUSTLINGS: https://rustlings.rust-lang.org/community-exercises/
- PLATFORM: https://rust-lang-translations.org/
- PLATFORM_REPO: https://github.com/rust-lang-translations/translations

## 三、60个源资料与locale组合

| 模块 | locale | 观察 | 来源 | 正文完整性 | 版本同步 |
| --- | --- | --- | --- | --- | --- |
| Rust Book | zh-CN | DIRECTORY_LISTED | BOOK | UNKNOWN | UNKNOWN |
| Rust Book | ja-JP | DIRECTORY_LISTED; PLATFORM_REPORTED_0.02% | BOOK; PLATFORM | UNKNOWN | UNKNOWN |
| Rust Book | ko-KR | DIRECTORY_LISTED; PLATFORM_REPORTED_99.62% | BOOK; PLATFORM | UNKNOWN | UNKNOWN |
| Rust Book | fr-FR | DIRECTORY_LISTED; PLATFORM_REPORTED_99.98% | BOOK; PLATFORM | UNKNOWN | UNKNOWN |
| Rust Book | de-DE | DIRECTORY_LISTED | BOOK | UNKNOWN | UNKNOWN |
| Rust Book | es-ES | DIRECTORY_LISTED | BOOK | UNKNOWN | UNKNOWN |
| Rust Book | id-ID | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Book | vi-VN | DIRECTORY_LISTED | BOOK | UNKNOWN | UNKNOWN |
| Rust Book | hi-IN | DIRECTORY_LISTED | BOOK | UNKNOWN | UNKNOWN |
| Rust Book | ru-RU | DIRECTORY_LISTED; PLATFORM_REPORTED_39.79% | BOOK; PLATFORM | UNKNOWN | UNKNOWN |
| Rust By Example | zh-CN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | ja-JP | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | ko-KR | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | fr-FR | EXTERNAL_TRANSLATION_LINKED | RBE | UNKNOWN | UNKNOWN |
| Rust By Example | de-DE | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | es-ES | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | id-ID | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | vi-VN | EXTERNAL_TRANSLATION_LINKED | RBE | UNKNOWN | UNKNOWN |
| Rust By Example | hi-IN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust By Example | ru-RU | EXTERNAL_TRANSLATION_LINKED | RBE | UNKNOWN | UNKNOWN |
| Cargo Book | zh-CN | PLATFORM_REPORTED_3.25% | PLATFORM | UNKNOWN | UNKNOWN |
| Cargo Book | ja-JP | PLATFORM_REPORTED_0.17% | PLATFORM | UNKNOWN | UNKNOWN |
| Cargo Book | ko-KR | PLATFORM_REPORTED_100.00% | PLATFORM | UNKNOWN | UNKNOWN |
| Cargo Book | fr-FR | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Cargo Book | de-DE | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Cargo Book | es-ES | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Cargo Book | id-ID | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Cargo Book | vi-VN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Cargo Book | hi-IN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Cargo Book | ru-RU | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | zh-CN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | ja-JP | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | ko-KR | PLATFORM_REPORTED_99.57% | PLATFORM | UNKNOWN | UNKNOWN |
| Rust Reference | fr-FR | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | de-DE | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | es-ES | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | id-ID | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | vi-VN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | hi-IN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rust Reference | ru-RU | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | zh-CN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | ja-JP | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | ko-KR | PLATFORM_REPORTED_99.79% | PLATFORM | UNKNOWN | UNKNOWN |
| Rustonomicon | fr-FR | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | de-DE | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | es-ES | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | id-ID | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | vi-VN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | hi-IN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustonomicon | ru-RU | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | zh-CN | COMMUNITY_EXERCISES_LINKED | RUSTLINGS | UNKNOWN | UNKNOWN |
| Rustlings | ja-JP | COMMUNITY_EXERCISES_LINKED | RUSTLINGS | UNKNOWN | UNKNOWN |
| Rustlings | ko-KR | COMMUNITY_EXERCISES_LINKED | RUSTLINGS | UNKNOWN | UNKNOWN |
| Rustlings | fr-FR | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | de-DE | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | es-ES | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | id-ID | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | vi-VN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | hi-IN | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |
| Rustlings | ru-RU | NOT_ESTABLISHED_IN_PILOT | — | UNKNOWN | UNKNOWN |

## 四、重要发现

Rust Book 官方目录列出多个目标语言译本，
但官方明确提示其中很多仍处于进行中。

Rust By Example 同时存在仓库内置翻译机制
和外部译本链接。日语构建说明与中文翻译指南
属于工作流证据，不能直接证明完整翻译。

Rust Translations 是非官方跨模块翻译平台。
它的百分比属于 SOURCE_REPORTED，
未独立验证完整正文、质量和版本一致性。

Rustlings 的社区练习必须逐项审查练习文件、
提示、测试、解答和版本对应关系。

平台统计为空、目录没有对应语言，
都不能推断目标语言不存在同源译本。

## 五、商业判断

同源竞争强度：PARTIALLY_OBSERVED
完整译本覆盖：UNKNOWN
各语言搜索需求：UNKNOWN
广告RPM：UNKNOWN
长期广告净利润：UNKNOWN

现有官方目录、内置翻译和多模块平台，
会降低部分语言单纯翻译的差异化空间。

必须优先比较用户价值、内容更新能力、
官方链接机会、搜索流量和维护成本，
而不是用未翻译语言数量衡量机会。

## 六、下一步

本轮仅为来源线索抽样，不是全文覆盖审计。

优先检查韩语 Cargo Book、Reference、
Rustonomicon、Rust Book 的实际正文与版本。

随后检查中文、日文 Rustlings 练习完整性，
以及 Rust Book 其他重点语言的同源译本。

如有竞争者已完整覆盖，应进一步检查质量、
维护状态和实际差异化空间，而不是重复翻译。

NEXT=RST_TARGETED_BODY_COMPLETENESS_CHECK
RUST_STATUS=RESEARCH_CONTINUE
SECOND_PROJECT=NOT_DECIDED

保持 RESEARCH_ONLY。
不启动翻译、不创建网站、不修改 go-dev。
