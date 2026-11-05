# Ethereum授权条款与同源译本覆盖抽样 001

核实日期：2026-11-05
阶段：ETH_TERMS_AND_SOURCE_EQUIVALENT_COVERAGE_PILOT
状态：RESEARCH_ONLY

候选：Ethereum Developer Learning & Documentation
目标语言：冻结66个locale
正式项目：NOT_DECIDED

## 一、研究目标

本阶段解决两个问题：

1. ethereum.org网站条款与开放内容许可证
   是否存在影响商业独立托管的限制。

2. 官方开发者文档的中文、德文译本
   是否具有实际正文内容，
   而不只是语言入口或翻译目录。

本阶段不启动翻译、建站或批量抓取。

## 二、官方条款

来源：
https://ethereum.org/terms-of-use/

核实日期：2026-11-05

### 2.1 内容许可

官方条款说明：

除另有标记外：

- 非代码内容：CC BY 4.0。
- 软件及代码：MIT。

状态：

DEFAULT_NON_CODE_LICENSE=VERIFIED
DEFAULT_CODE_LICENSE=VERIFIED

CC BY 4.0原文：
https://creativecommons.org/licenses/by/4.0/

CC BY 4.0允许在遵守许可证条件的情况下：

- 复制与再分发。
- 翻译和其他改编。
- 商业使用。

需要遵守署名、许可证链接、
修改说明及其他适用条件。

不得暗示原作者或许可人认可独立网站。

因此：

CC_BY_COMMERCIAL_ADAPTATION=VERIFIED

但上述判断仅适用于
确实受CC BY 4.0授权的材料。

不自动覆盖商标、
独立第三方权利或例外文件。

### 2.2 官方网站访问限制

官方Terms of Use明确将
网站使用者限定为个人使用用途。

状态：

PERSONAL_USE_ACCESS_CLAUSE=VERIFIED

条款同时限制未经授权的
自动化访问、监控或复制行为。

也包含对部分手动复制行为的限制。

状态：

AUTOMATED_SITE_COPYING_RESTRICTION=VERIFIED

因此不能把CC BY授权解释为
任意抓取ethereum.org网站的许可。

### 2.3 广告相关条款

官方条款包含未经书面同意
不得通过其网站传送广告或推广材料
等限制。

状态：

WEBSITE_ADVERTISING_RESTRICTION=VERIFIED

但是：

通过ethereum.org发送推广材料，
与在独立网站展示Google AdSense广告，
不是同一个具体行为。

当前没有证据证明该条款
直接禁止所有符合CC BY的内容
在独立网站上进行广告变现。

也没有证据足以证明
所有独立商业托管方式均无其他限制。

因此：

INDEPENDENT_AD_HOSTING_CLEARANCE=UNCLEAR

不得将其标记为禁止，
也不得直接标记为全面允许。

### 2.4 源码仓库与网站访问

官方GitHub仓库：
https://github.com/ethereum/ethereum-org-website

仓库许可证：
https://github.com/ethereum/ethereum-org-website/blob/dev/LICENSE

仓库LICENSE包含MIT许可证文本。

状态：

REPOSITORY_LICENSE=VERIFIED

官方文档源码位置：

https://github.com/ethereum/ethereum-org-website/tree/dev/public/content/developers/docs

当前需要进一步明确：

1. 仓库LICENSE对内容文件的具体适用范围。
2. 仓库中非代码内容与网站CC BY声明的关系。
3. 直接从GitHub取得授权内容的合法路径。
4. 文件级第三方材料与独立许可证。
5. 商标及视觉资产的独立限制。

不能因为仓库存在MIT LICENSE，
就将全部网站材料直接认定为MIT。

SOURCE_FILE_RIGHTS=PARTIALLY_VERIFIED
GITHUB_REUSE_PATH=UNCLEAR
THIRD_PARTY_ASSETS=UNCLEAR
TRADEMARK_USE=UNCLEAR

### 2.5 法律边界

需要区分：

- 内容版权授权。
- 网站访问合同。
- GitHub源码取得方式。
- 第三方素材权利。
- 商标使用。
- 独立网站广告展示。

开放许可证允许的版权行为，
与访问网站时可能承担的合同义务，
不能简单混为一谈。

当前未完成适用法律及具体合同解释。

法律结论：

LEGAL_INTERPRETATION=UNCLEAR

这不是正式法律意见。

## 三、官方翻译项目现状

来源：
https://ethereum.org/contributing/translation-program/

官方页面在本次核实时说明：

- 网站报告累计已有68种语言上线。
- Crowdin整页翻译提交已暂停。
- 现阶段主要转向术语审查。
- 已有社区翻译仍保留于网站。

状态：

REPORTED_LIVE_LANGUAGES=68
CROWDIN_FULL_PAGE_SUBMISSIONS=PAUSED

注意：

68种语言上线不等于
68种语言的全部开发者文档完整翻译。

也不代表官方完全停止
更新或维护多语言内容。

EXACT_FULL_COVERAGE=UNKNOWN
FUTURE_TRANSLATION_POLICY=UNKNOWN

## 四、同源译本抽样范围

本次只检查两篇原始文档：

A. Technical intro to Ethereum
B. Gas and fees

目标语言：

- 简体中文。
- 德语。

对照原文：

- 英语。

实际目标语言页面样本：

2篇原文 × 2种目标语言 = 4个译文页面。

SAMPLED_SOURCE_PAGES=2
SAMPLED_TARGET_LANGUAGES=2
SAMPLED_TRANSLATED_PAGES=4

该样本仅验证是否存在真实同源内容，
不是全站覆盖率统计。

## 五、Technical intro to Ethereum

英语原文：

https://ethereum.org/developers/docs/intro-to-ethereum/

中文：

https://ethereum.org/zh/developers/docs/intro-to-ethereum/

德语：

https://ethereum.org/de/developers/docs/intro-to-ethereum/

本次核查：

英语页面包含：

- 区块链基础。
- Ethereum定义。
- Ether。
- 智能合约。
- 术语与延伸阅读。

中文页面可确认：

- 存在中文标题。
- 存在实际中文正文段落。
- 包含与英语原文对应的主要主题。

德语页面可确认：

- 存在德语标题。
- 存在实际德语正文段落。
- 包含与英语原文对应的主要主题。

状态：

INTRO_ZH_ENTRY=VERIFIED
INTRO_ZH_LOCALIZED_BODY=VERIFIED
INTRO_DE_ENTRY=VERIFIED
INTRO_DE_LOCALIZED_BODY=VERIFIED

但未完成所有段落、
代码、图表与链接的逐项比较。

INTRO_EXACT_COMPLETENESS=UNKNOWN
INTRO_VERSION_PARITY=UNKNOWN

## 六、Gas and fees

英语原文：

https://ethereum.org/developers/docs/gas/

中文：

https://ethereum.org/zh/developers/docs/gas/

德语：

https://ethereum.org/de/developers/docs/gas/

本次核查：

三个语言页面均存在对应内容。

中文页面具有：

- Gas定义。
- 费用计算。
- 基础费用。
- 优先费用。
- Gas限额等技术内容。

德语页面具有：

- Gas定义。
- 费用计算。
- Gas限额等技术内容。

这说明实际翻译正文已经存在。

状态：

GAS_ZH_ENTRY=VERIFIED
GAS_ZH_LOCALIZED_BODY=VERIFIED
GAS_DE_ENTRY=VERIFIED
GAS_DE_LOCALIZED_BODY=VERIFIED

但未完成全部段落、
图表、技术数据和当前版本一致性检查。

GAS_EXACT_COMPLETENESS=UNKNOWN
GAS_VERSION_PARITY=UNKNOWN

## 七、抽样结果汇总

| 原始页面 | 中文正文 | 德语正文 | 完整度 |
| --- | --- | --- | --- |
| Technical intro | VERIFIED | VERIFIED | UNKNOWN |
| Gas and fees | VERIFIED | VERIFIED | UNKNOWN |

抽样结果说明：

中文、德语官方开发者文档
确实存在直接的同源翻译竞争。

不能再将这些语言简单认定为
缺少官方开发者文档。

但不能根据两篇文章，
推断整个开发者资料库完整覆盖。

不计算整体覆盖百分比。

## 八、商业竞争影响

官方具有以下竞争优势：

- 官方主域名。
- 已存在真实翻译正文。
- 原始内容直接维护。
- 开发者文档导航完整。
- 已积累大量社区翻译。

这提高了独立同源翻译项目
取得自然搜索流量的难度。

但是仍有待调查：

- 其他目标语言实际覆盖情况。
- 高级开发资料的翻译缺口。
- 版本滞后程度。
- 语言之间的覆盖差异。
- 是否存在可验证的搜索需求。

不能把官方翻译项目暂停，
直接解释成商业机会已经出现。

也不能因为两篇译文存在，
就淘汰全部66-locale候选机会。

## 九、风险与停止条件

本次发现的主要风险：

1. 网站访问条款与内容许可证
   需要进一步厘清适用边界。

2. 官方中文和德文文档
   已经具有实际内容竞争。

3. 内容涉及协议升级与技术变化，
   更新和审核成本可能较高。

4. 目标语言的搜索需求与广告收益
   尚无可靠量化证据。

商业独立托管未完成授权确认前，
不得启动大规模翻译或建站。

如果后续发现无法取得
合法、可持续的源内容使用路径，
应暂停这一候选的深入商业研究。

若合法路径明确，
再调查实际语言缺口与自然流量机会。

## 十、总体判断

ETH_STATUS=RESEARCH_CONTINUE

DEFAULT_CONTENT_LICENSE=VERIFIED
CC_BY_COMMERCIAL_ADAPTATION=VERIFIED

SITE_ACCESS_RESTRICTIONS=VERIFIED
SOURCE_REUSE_LEGAL_BOUNDARY=UNCLEAR
INDEPENDENT_AD_HOSTING_CLEARANCE=UNCLEAR

SOURCE_EQUIVALENT_TRANSLATIONS=VERIFIED_IN_SAMPLE
SAMPLED_TRANSLATED_PAGES=4

EXACT_FULL_TRANSLATION_COVERAGE=UNKNOWN
ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
ADS_RPM=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN

FORMAL_PROJECT_SELECTED=NO
SECOND_PROJECT=NOT_DECIDED

不进行商业收益排名。

## 十一、唯一下一研究阶段

NEXT=ETH_REPOSITORY_CONTENT_RIGHTS_AND_REUSE_PATH_GATE

下一阶段重点：

1. 从GitHub仓库进一步核对
   文档源文件与LICENSE之间的关系。

2. 查找官方对内容转载、翻译、
   独立托管及来源获取的明确说明。

3. 判断是否存在合法、可持续、
   不依赖违规抓取的内容获取路径。

4. 对第三方素材和商标制定排除边界。

5. 若公开证据仍有实质歧义，
   保持UNCLEAR，并决定是否需要
   向官方取得书面澄清。

在解决商业授权边界之前，
不扩大至66种语言的批量覆盖调查。

保持RESEARCH_ONLY。

不启动翻译。
不建立正式网站。
不部署服务。
不修改go-dev v2。
