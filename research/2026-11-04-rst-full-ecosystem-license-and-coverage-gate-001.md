# Rust 全生态商业授权与同源译本覆盖门禁 001

核实日期：2026-11-04
阶段：RST_FULL_ECOSYSTEM_LICENSE_AND_COVERAGE_GATE
状态：RESEARCH_ONLY
目标范围：66 locales
第二项目：NOT_DECIDED

## 一、研究范围

本轮研究六个 Rust 核心模块：

1. The Rust Programming Language（Rust Book）
2. Rust By Example
3. The Cargo Book
4. The Rust Reference
5. The Rustonomicon
6. Rustlings

研究对象是完整 Rust 学习体系，而非单一 Rust Book。

66 locales 是目标范围，不代表本轮已完成
66 locales 的同源译本覆盖调查。

必须区分：
- 官方源内容与第三方素材的许可证。
- 版权商业使用与广告平台准入。
- 独立托管与官方链接收录。
- 同源完整译本与一般同主题教程。
- 官方翻译清单与实际正文完整性。

## 二、六模块许可证门禁

| 模块 | 仓库 | 初步许可证 | 状态 |
| --- | --- | --- | --- |
| Rust Book | rust-lang/book | MIT OR Apache-2.0 | VERIFIED |
| Rust By Example | rust-lang/rust-by-example | MIT OR Apache-2.0 | VERIFIED |
| Cargo Book | rust-lang/cargo | MIT/Apache-2.0 主体 | VERIFIED |
| Rust Reference | rust-lang/reference | MIT OR Apache-2.0 | VERIFIED |
| Rustonomicon | rust-lang/nomicon | MIT OR Apache-2.0 | VERIFIED |
| Rustlings | rust-lang/rustlings | MIT | VERIFIED |

来源：

https://github.com/rust-lang/book
https://github.com/rust-lang/rust-by-example
https://github.com/rust-lang/cargo
https://github.com/rust-lang/reference
https://github.com/rust-lang/nomicon
https://github.com/rust-lang/rustlings

Rust Book LICENSE-MIT：
https://github.com/rust-lang/book/blob/main/LICENSE-MIT

Rustlings LICENSE：
https://github.com/rust-lang/rustlings/blob/main/LICENSE

Rust 官方许可说明：
https://rust-lang.org/policies/licenses/

判断：

主要原始仓库允许商业使用及再分发，
但必须遵守相应许可证与署名要求。

不得把仓库主许可证自动扩展到所有
第三方图片、字体、标志、嵌入服务或依赖。

Cargo 仓库存在第三方软件授权说明，
Cargo Book 正文、代码、相关素材的
实际再分发清单仍需在实施前细查。

Rustlings 的 MIT 许可不等于任何外部
交互服务或第三方资产均采用 MIT。

商业翻译的版权基础：VERIFIED
所有拟部署资产的完整许可清单：UNKNOWN

## 三、Rust Book 社区翻译与官方链接

官方 Appendix F：

https://doc.rust-lang.org/book/appendix-06-translation.html

状态：VERIFIED

官方已经收录多个社区翻译资源。

部分链接指向独立托管的网站，
例如乌克兰语和意大利语资源；
其他不少链接直接指向 GitHub 仓库。

因此：

COMMUNITY_TRANSLATION_LIST=VERIFIED
EXTERNAL_HOSTED_LINK_PRECEDENT=VERIFIED
NEW_TRANSLATION_SUBMISSION_PATH=VERIFIED
FUTURE_LISTING_ACCEPTANCE=UNKNOWN

官方贡献说明：

https://github.com/rust-lang/book/blob/main/CONTRIBUTING.md

官方表示欢迎翻译贡献，并可通过
Translations 标签或新 Issue 参与。

近期申请案例：

https://github.com/rust-lang/book/issues/4710
https://github.com/rust-lang/book/issues/4804

申请记录不等于已经批准。

官方链接收录也不代表获得
Rust 官方商业背书。

## 四、独立社区网站广告门禁

必须分成四个独立问题。

### A. 版权许可

MIT/Apache-2.0 允许商业再分发，
满足条款时并不因网站放广告而
自动丧失内容使用许可。

COPYRIGHT_COMMERCIAL_USE=VERIFIED

### B. Rust 商标

Rust Foundation 商标政策：

https://rustfoundation.org/policy/rust-trademark-policy/

禁止未经许可使网站看起来属于
Rust 官方、受官方认可或得到背书。

独立社区翻译网站应明确标注
非官方身份，并单独审查域名、
站点名称、Logo 和商业推广方式。

TRADEMARK_COMPLIANCE=REQUIRES_REVIEW

### C. 官方目录收录与广告

当前已核实独立社区翻译链接先例，
但没有足够证据证明官方已经批准
带 Google AdSense 广告的译本网站。

亦未核实针对该场景的一般性禁令。

OFFICIAL_AD_SUPPORTED_LISTING=UNCLEAR
AD_FREE_REQUIREMENT=UNCLEAR

不得以“未查到禁止规定”
推断官方已经同意放广告。

未来若申请收录，应明确询问：
商业广告是否影响官方链接收录。

### D. Google AdSense

Google Publisher Policies：

https://support.google.com/publisherpolicies/answer/11190248?hl=en

AdSense Program Policies：

https://support.google.com/adsense/answer/48182?hl=en

Google 不允许缺少实质附加价值的
简单镜像、复制、机械改写等内容
直接使用 Google 提供的广告。

合法翻译不自动获得 AdSense 准入。

应评估：
- 翻译质量与人工审核。
- 技术准确性及持续更新。
- 原创说明、交互功能或其他增值内容。
- 网站整体内容质量。
- 广告展示密度与用户体验。

ADSENSE_APPROVAL=UNKNOWN
COMMERCIAL_AD_REVENUE=UNKNOWN

## 五、其他模块的社区翻译机制

Rust By Example 官方仓库包含 po/
翻译资源，且提供本地构建翻译版的说明。

来源：
https://github.com/rust-lang/rust-by-example

不能只搜索独立翻译网站，
也需要核查官方仓库内置翻译。

对于 Cargo Book、Reference、
Rustonomicon、Rustlings：

本轮不能证明 66 locales 中
哪些存在完整、维护中的同源译本。

也不能直接套用 Rust Book 的
Appendix F 收录机制。

各模块均应独立确认：
- 官方是否提供翻译索引。
- 是否存在独立社区译本。
- 是否支持独立托管。
- 是否接受外部翻译链接申请。
- 是否存在带广告的已收录案例。

OTHER_MODULE_LINK_POLICY=UNKNOWN

## 六、同源译本竞争门禁

不得把存在一般 Rust 教程等同于
六个指定源资料均已有完整译本。

每个模块、locale、具体源版本
分别检查：

EXACT_FULL
EXACT_PARTIAL
EXACT_OUTDATED
FULL_STRUCTURE_VERIFIED
NOT_FOUND_IN_SAMPLE
UNKNOWN

目录完整不能直接证明正文完整。

Rustlings 应检查练习、解答、
测试结构及版本对应关系，
不能使用普通教材章节标准代替。

Rust Book Appendix F 已证明
多个语言存在直接同源竞争。

但是：

SIX_MODULE_FULL_TRANSLATION_COVERAGE=UNKNOWN
ALL_66_LOCALES_COVERAGE=UNKNOWN

不得将尚未找到完整译本的
语言自动认定为商业机会。

## 七、长期广告商业可行性

必须继续核查：

1. 原始技术资料的长期搜索需求。
2. 六模块的实际同源翻译覆盖。
3. 各语言的用户规模及广告市场。
4. 官方与搜索引擎流量入口。
5. 文档版本更新及同步维护成本。
6. 质量审核和交互能力的新增成本。
7. 与现有 Go 多语言基础设施的复用。

SEARCH_DEMAND=UNKNOWN
ORGANIC_TRAFFIC=UNKNOWN
AD_RPM=UNKNOWN
NET_AD_PROFIT=UNKNOWN

不使用虚构的搜索量、RPM 或收入。

官方链接只是潜在流量入口，
不是流量或广告收益保证。

## 八、阶段判断与下一步

RESULT=RESEARCH_CONTINUE

六个原始仓库具备较明确的
开放商业授权基础。

Rust Book 存在官方社区翻译入口，
但官方对带广告社区译本的收录态度
仍然 UNCLEAR。

尚不足以决定启动 Rust 体系翻译。

第二项目：NOT_DECIDED

NEXT=RST_SOURCE_EQUIVALENT_TRANSLATION_COVERAGE_PILOT

下一步以六模块为源资料，
抽样调查目标 locale：

- 官方译本、社区译本及内置翻译。
- 实际同源完整正文或练习。
- 原始版本及同步维护状态。
- 独立托管与官方链接类型。
- 已收录译本的广告展示证据。
- 实质性的多语言内容缺口。

必须将广告页面事实与官方政策
明确分开，不能相互替代。

保持 RESEARCH_ONLY。

不启动翻译。
不创建正式网站。
不修改 go-dev v2。
不购买域名。
