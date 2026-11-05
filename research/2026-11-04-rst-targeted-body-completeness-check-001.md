# Rust 同源译本正文完整性定向核查 001

核实时间：2026-11-05T01:38:39.242914+00:00
阶段：RST_TARGETED_BODY_COMPLETENESS_CHECK
状态：RESEARCH_ONLY
第二项目：NOT_DECIDED

## 一、韩语四模块

| 模块 | 有效条目 | 非空译文 | 异常条目 | 正文候选 |
| --- | ---: | ---: | ---: | ---: |
| book | 5036 | 5020 | 6 | 2931 |
| cargo | 7140 | 7140 | 2 | 4179 |
| reference | 6780 | 6779 | 0 | 2793 |
| nomicon | 1422 | 1422 | 3 | 769 |

统计仅覆盖成功解析的 PO 条目。
格式异常条目已经单独记录，未被计入有效条目。
因此非空译文比例不能作为全书完成率。

韩语正文候选通过字符特征筛选，
并记录首、中、末样本的 SHA-256。
该检查不证明语义质量或版本同步。

上游数据：
- book: https://raw.githubusercontent.com/rust-lang-translations/translations/master/translations/book/ko.po
- cargo: https://raw.githubusercontent.com/rust-lang-translations/translations/master/translations/cargo/ko.po
- reference: https://raw.githubusercontent.com/rust-lang-translations/translations/master/translations/reference/ko.po
- nomicon: https://raw.githubusercontent.com/rust-lang-translations/translations/master/translations/nomicon/ko.po

## 二、Rustlings 中文及日文

| locale | 社区文件 | 官方文件 | 同路径 | 缺少官方路径 |
| --- | ---: | ---: | ---: | ---: |
| zh-CN | 95 | 95 | 95 | 0 |
| ja-JP | 94 | 95 | 85 | 10 |

官方来源：https://github.com/rust-lang/rustlings
- zh-CN: https://github.com/SandmeyerX/rustlings-zh-cn
- ja-JP: https://github.com/sotanengel/rustlings-jp

本轮抽样检查实际练习文件，并记录内容哈希。
文件路径一致不代表练习内容版本完全一致。
不同路径也可能源于版本重组。
完整练习、提示和解答尚未逐项审核。

## 三、商业判断

韩语四模块存在大量实际非空翻译条目。
中日文 Rustlings 已存在实际练习竞争者。

FULL_BODY_COMPLETENESS=UNKNOWN
VERSION_SYNC=UNKNOWN
TRANSLATION_QUALITY=UNKNOWN
ORGANIC_TRAFFIC=UNKNOWN
AD_RPM=UNKNOWN
NET_AD_PROFIT=UNKNOWN

不得把机器统计数量直接解释为完整翻译。
不得将目录或代码文件数量直接等同于用户价值。

## 四、下一步

NEXT=RST_LANGUAGE_OPPORTUNITY_REASSESSMENT
RUST_STATUS=RESEARCH_CONTINUE
SECOND_PROJECT=NOT_DECIDED

下一阶段结合已确认的竞争者覆盖，
重新评估目标语言的商业机会与维护成本。

不启动翻译，不创建网站，不修改 go-dev。

机器证据：/tmp/mpr-rst-body-recovery-20261105T013839Z.json
