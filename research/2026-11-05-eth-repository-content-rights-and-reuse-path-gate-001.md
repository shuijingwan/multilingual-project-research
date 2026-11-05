# Ethereum文档源码权利与商业复用路径核查 001

核实日期：2026-11-05
阶段：ETH_REPOSITORY_CONTENT_RIGHTS_AND_REUSE_PATH_GATE
状态：RESEARCH_ONLY

候选：Ethereum Developer Learning & Documentation
目标语言：冻结66个locale
正式项目：NOT_DECIDED

## 一、研究目标

本阶段不重复一般性许可介绍。

重点判断：

1. 能否直接从公开GitHub仓库取得文档源码。
2. 源码仓库MIT许可证是否覆盖全部内容。
3. 官方CC BY声明能否支持商业翻译。
4. 网站访问条款是否影响独立托管。
5. 第三方素材是否存在独立版权限制。
6. 是否具备合法、可持续的复用路径。

商业目标仍然是：

LONG_TERM_AD_NET_PROFIT

不得将开放源码等同于
完整的商业建站授权。

## 二、官方来源

网站使用条款：

https://ethereum.org/terms-of-use/

网站介绍及许可证说明：

https://ethereum.org/about/

源码仓库：

https://github.com/ethereum/ethereum-org-website

仓库LICENSE：

https://github.com/ethereum/ethereum-org-website/blob/dev/LICENSE

开发者文档目录：

https://github.com/ethereum/ethereum-org-website/tree/dev/public/content/developers/docs

仓库技术文档：

https://github.com/ethereum/ethereum-org-website/blob/dev/docs/stack.md

CC BY 4.0：

https://creativecommons.org/licenses/by/4.0/

以上为本阶段主要一手来源。

## 三、官方内容授权

ethereum.org使用条款明确区分：

- 非代码内容：默认CC BY 4.0。
- 代码内容：默认MIT。

除非另有标记。

状态：

DEFAULT_NON_CODE_LICENSE=VERIFIED
DEFAULT_CODE_LICENSE=VERIFIED

CC BY 4.0允许：

- 复制。
- 再分发。
- 翻译及改编。
- 商业使用。

条件包括：

- 适当署名。
- 提供许可证链接。
- 说明修改。
- 不暗示官方认可。
- 遵守其他适用条款。

因此：

CC_BY_COMMERCIAL_TRANSLATION=VERIFIED

但必须限定在
确实获得CC BY授权的内容范围。

不得扩展为全部网站素材、
商标和第三方权利均已清晰授权。

## 四、GitHub仓库LICENSE

官方仓库LICENSE包含MIT文本。

核查来源：

https://github.com/ethereum/ethereum-org-website/blob/dev/LICENSE

该许可证允许符合条件的
软件复制、修改与商业再分发。

状态：

REPOSITORY_MIT_LICENSE=VERIFIED

但存在适用范围问题：

网站官方使用条款已明确区分
非代码内容和代码内容。

所以不能单纯依据
仓库根目录存在MIT许可证，
将全部Markdown、图片、
音视频及第三方素材
统一解释为MIT。

需要同时考虑：

- 仓库许可证。
- 网站内容许可证。
- 文件级特殊标记。
- 第三方来源及署名。
- 其他适用权利。

FULL_REPOSITORY_CONTENT_RIGHTS=UNCLEAR

## 五、源码获取路径

官方README：

https://github.com/ethereum/ethereum-org-website/blob/dev/README.md

官方README提供了
通过Git克隆仓库、
创建Fork以及提交PR的操作说明。

状态：

PUBLIC_GIT_REPOSITORY=VERIFIED
GIT_CLONE_DOCUMENTED=VERIFIED

仓库公开可读，
开发者文档Markdown源码可直接定位。

示例源码：

https://github.com/ethereum/ethereum-org-website/blob/dev/public/content/developers/docs/intro-to-ethereum/index.md

https://github.com/ethereum/ethereum-org-website/blob/dev/public/content/developers/docs/gas/index.md

因此：

DIRECT_SOURCE_ACCESS_PATH=VERIFIED

通过GitHub公开仓库取得源文件，
与对ethereum.org网站进行批量抓取，
属于不同的技术访问路径。

但README说明的Fork和Clone流程，
主要服务于开源协作。

它本身不能单独证明
独立商业内容网站已经
获得所有必要权利。

INDEPENDENT_COMMERCIAL_REUSE_PATH=UNCLEAR

若未来使用GitHub获取内容，
仍须遵守GitHub适用条款、
文件许可证及第三方权利要求。

当前不运行批量Clone或内容导入。

## 六、网站访问条款

官方条款：

https://ethereum.org/terms-of-use/

已确认包括：

- 访问者个人使用条件。
- 对自动化访问和复制的限制。
- 对部分手动复制行为的限制。
- 商标及关联暗示限制。

状态：

SITE_ACCESS_RESTRICTIONS=VERIFIED

需要区分：

A. 通过ethereum.org访问网页。

B. 从公开GitHub仓库获取源文件。

C. 依据有效开放许可证
   翻译并独立托管特定内容。

这些行为不应自动视为同一行为。

CC BY许可属于版权授权。

网站Terms of Use还可能
构成独立的访问合同义务。

二者之间的适用关系
需要进一步确认。

不能仅根据网站限制，
认定所有独立商业翻译违法。

也不能仅根据CC BY，
断言网站访问条款完全无关。

SITE_TERMS_VS_CONTENT_LICENSE=UNCLEAR
INDEPENDENT_AD_HOSTING_CLEARANCE=UNCLEAR

## 七、具体文档源码核查

本次检查两个源文件。

### 7.1 Technical intro to Ethereum

路径：

public/content/developers/docs/intro-to-ethereum/index.md

文件包含：

- Markdown正文。
- 语言及标题元数据。
- 内部文档链接。
- 外部第三方示例链接。
- 视频组件引用。

状态：

MARKDOWN_SOURCE=VERIFIED
THIRD_PARTY_REFERENCES=VERIFIED

正文默认许可具有官方声明依据。

但是外部链接和视频内容
不因出现在Markdown中，
就自动取得相同再分发授权。

EXTERNAL_MEDIA_RIGHTS=UNCLEAR

### 7.2 Gas and fees

路径：

public/content/developers/docs/gas/index.md

文件包含：

- Markdown正文。
- 技术计算示例。
- 图片引用gas.png。
- 第三方作品改编说明。

该页面图片注明：

示意图改编自
Ethereum EVM illustrated。

原始资料链接：

https://takenobu-hs.github.io/downloads/ethereum_evm_illustrated.pdf

这是一个需要单独审查
来源和授权的明确样本。

状态：

MARKDOWN_SOURCE=VERIFIED
DERIVED_DIAGRAM_SIGNAL=VERIFIED
DIAGRAM_REUSE_RIGHTS=UNCLEAR

不得直接将该图片
纳入未来商业译站。

本次没有核实原始PDF
是否允许商业改编及再分发。

## 八、第三方素材处理规则

若未来开展正式项目，
应为内容资产区分：

TEXT：
具有明确开放许可的正文。

CODE：
具有明确软件许可证的代码。

IMAGE：
图片、示意图、截图。

MEDIA：
视频、音频及外部嵌入。

TRADEMARK：
Logo、品牌和相关标识。

EXTERNAL：
第三方转载、引用或改编资料。

不同资产应分别确认使用权限。

不允许把整页默认CC BY
直接当成所有素材授权结论。

当前建议：

- 优先研究纯文本内容。
- 外部视频只保留合法链接。
- 不复制不明授权图片。
- 对第三方代码另行核实。
- 不复用官方Logo和品牌视觉。
- 独立站点不得暗示官方认可。

上述属于拟议的风险控制方案，
不是已批准的建站实施方案。

## 九、商业复用必要条件

未来考虑独立翻译网站前，
至少应满足：

1. 原文具有明确商业授权。
2. 合法取得源文件。
3. 保留必要署名和许可证信息。
4. 明确标记翻译及修改。
5. 不复制未获授权的第三方素材。
6. 不侵犯商标或造成官方关联误导。
7. 对网站条款与获取方式的冲突
   有足够清晰的依据。
8. 符合广告平台和其他适用政策。

本阶段未完成全部条件。

COMMERCIAL_DEPLOYMENT_READY=NO

## 十、商业竞争与维护判断

官方已提供中文、德文
开发者文档的实际译文正文。

上一阶段抽样：

SAMPLED_TRANSLATED_PAGES=4

不能因源码获取路径存在，
就认为独立翻译网站
能够获得自然搜索流量。

也不能因为CC BY允许商业使用，
就认为广告变现具有可行性。

目前：

SEARCH_DEMAND=UNKNOWN
ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN
AD_PAGE_RPM=UNKNOWN
MAINTENANCE_COST=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN

官方已有译文与更新机制，
依然是重要的直接竞争风险。

## 十一、证据状态汇总

| 事项 | 状态 |
| --- | --- |
| 官方默认非代码许可 | VERIFIED |
| CC BY商业翻译权利 | VERIFIED |
| 仓库MIT文本 | VERIFIED |
| 公开GitHub源码路径 | VERIFIED |
| 直接克隆协作流程 | VERIFIED |
| 全部文件统一授权 | UNCLEAR |
| 第三方图片授权 | UNCLEAR |
| 官网访问条款适用边界 | UNCLEAR |
| 独立广告网站完整授权 | UNCLEAR |
| 真实自然搜索流量 | UNKNOWN |
| 长期广告净收益 | UNKNOWN |

## 十二、当前决策

ETH_STATUS=RESEARCH_CONTINUE

SOURCE_ACCESS_PATH=VERIFIED
DEFAULT_CONTENT_LICENSE=VERIFIED

INDEPENDENT_COMMERCIAL_REUSE_PATH=UNCLEAR
THIRD_PARTY_ASSET_RIGHTS=UNCLEAR
INDEPENDENT_AD_HOSTING_CLEARANCE=UNCLEAR

FORMAL_PROJECT_SELECTED=NO
SECOND_PROJECT=NOT_DECIDED

现有证据不足以批准正式开发。

但也不足以断定
Ethereum开发者文档
完全不适合商业翻译。

后续调查需要设置停止线，
避免持续投入而不能解决
关键授权问题。

## 十三、下一阶段

NEXT=ETH_COMMERCIAL_REUSE_CLARIFICATION_STOP_GATE

下一阶段优先：

1. 复核官方是否已有
   独立商业翻译、托管或复用说明。

2. 明确GitHub源文件获取
   与官网访问限制之间的边界。

3. 判断排除第三方素材后，
   纯文本商业翻译是否具备
   足够明确的许可依据。

4. 如果关键问题仍然不明，
   整理少量精确问题，
   考虑向官方请求书面澄清。

5. 设置调查停止条件，
   决定继续、暂停或淘汰。

不将法律上的UNCLEAR
冒充商业许可已经被拒绝。

不因许可证理论上兼容，
就跳过官方翻译竞争和流量调查。

不开展66语言批量SEO调查。

保持RESEARCH_ONLY。

不翻译内容。
不建设正式网站。
不部署服务。
不修改go-dev v2。
