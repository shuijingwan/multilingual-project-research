# 世界历史第二项目：正文来源与图片许可边界冻结前研究 001

核实日期：2026-11-06
阶段：HIS_SOURCE_AND_MEDIA_LICENSED_SCOPE_FREEZE_RESEARCH
项目状态：RESEARCH_ONLY
正式第二项目：WORLD_HISTORY（OWNER_SELECTED=YES）
域名项目标识：world-history
locale命名：与go-dev正式生产前缀完全一致
主项目go-dev v2：优先级不变，未操作

## 1. 本轮目标与“冻结”的实际含义

项目负责人已**正式选择世界历史作为第二项目**，但尚未批准翻译、建站、DNS、部署或资产大批量处理。

本轮完成的内容：

- 核实三本教材的**出版社或学术机构来源**、年代、已知许可、版本锚点；
- 为正文、地图、照片、表格、封面、第三方引用等建立分类与停止线；
- 抽样验证**允许再利用的例子**和**不应直接转载的例子**；
- 划分已可列为来源范围的项目与**仍未完成的逐文件/逐图像审核**；
- 不将有限抽样夸大为全书已审核。

因此本轮是 **SOURCE_SCOPE_BASELINE_FROZEN=YES（按书名/出版社/ISBN/DOI层面固定初步来源）**，但 **EXACT_SOURCE_FILE_BYTES_FROZEN=NO**，也未取得每个素材文件的SHA/正式发布白名单。不得把“研究范围锁定”误称为“全书可直接出版”。

## 2. 三本来源与精确身份锚点

| ID | 书名 | 正式来源 | 出版版本可核实元数据 | 本站对应模块 | 正文权利基础 |
| --- | --- | --- | --- | --- | --- |
| HIS-A | World History: Cultures, States, and Societies to 1500 | University of North Georgia Press / GALILEO | 2016年秋，ISBN 978-1-940771-10-6；12章 | world-history-to-1500 | CC BY-SA 4.0，且有第三方例外 |
| HIS-B | World History Since 1500: An Open and Free Textbook | East Tennessee State University / Digital Commons | 原出版页建议引用年份2022；作者 John Rankin、Constanze Weise；15章；官方PDF约150.9MB | world-history-since-1500 | CC BY 4.0，**仅覆盖原创内容** |
| HIS-C | History of International Relations: A Non-European Perspective | Open Book Publishers | 2019-07-31；DOI 10.11647/OBP.0074；PDF ISBN 978-1-78374-024-6；216页（x+206） | international-relations | CC BY 4.0；许多图片另有权利 |

### 官方链接（主要版权证据，核实日期2026-11-06）

- A出版社原页：https://ung.edu/university-press/books/world-history-cultures-states-societies-to-1500.php
- A学术原始存储：https://oer.galileo.usg.edu/history-textbooks/2/
- A官方关联开放阅读版许可页（书内版权原文）：https://alg.manifoldapp.org/system/actioncallout/2262cd69-86e2-4b67-8123-77de71f78bd1/attachment/original-180d9cbf5d43c63515b9e3aa04e5a822.pdf
- B大学原始仓储：https://dc.etsu.edu/etsu-oer/13/
- C出版社目录及元数据：https://www.openbookpublishers.com/books/10.11647/obp.0074
- C学术馆藏前言版权文字：https://tile.loc.gov/storage-services/master/gdc/gdcebookspublic/20/19/45/28/64/2019452864/2019452864.pdf

在正式准备翻译前，须先选定一份**具体的出版文件**，记录来源URL、获取时间、文件大小、SHA-256、版次/修订日期、对应的出版许可证证据。

### 版本风险

A：官方目录2016，但出版社提供的PDF文件名含`082817`（可能代表2017年文件修订或命名，**不能仅由文件名认定正式新版本**）。本轮未建立所选原文文件哈希，故文本精确版本尚未冻结。

B：原始大学页面引用年份为**2022**，其他二级目录可能显示2023且标注不同许可证（如Open Textbook Library显示CC BY-SA），**优先依据ETSU本身的具体版本版权页和CC BY 4.0声明**，不可机械采纳目录授权。

C：有DOI与不同格式ISBN；如果网页HTML、PDF、XML有差异，正式翻译前需选择唯一主源版本或明确内容对照关系。

本轮没有下载整本教材、批量转换内容、创建正式内容页面。

## 3. 正文和翻译许可操作要求

- **HIS-A CC BY-SA 4.0**：对原著受此授权的内容进行翻译属于改编；允许商业使用，但翻译改编作品遵守署名、许可证链接、变更声明和**ShareAlike**要求。不得以本站独占条款、技术限制等抵触源许可。
- **HIS-B / HIS-C CC BY 4.0**：受许可覆盖的原著内容允许商业翻译和分发，需署名、许可证链接和标明修改；不意味着其夹杂的第三方作品全部获得同权。
- 三本书**同一站点不代表同一许可证**：各教材/章节标记实际适用许可，媒体再按各自权利标记；不要把HIS-A的SA要求误套为整个域名所有内容一律SA，也不要用HIS-B的CC BY覆盖A的改编翻译。
- 普通学术引文、参考书目、外部视频链接、出版社提供的封面、作者照片与图表，其版权状态分别核实；不可把教材自己**引用他人的文字或图像**等同于已获独立商业再分发授权。
- 不以“来源免费/许可开放”为依据省略来源署名、出版信息或必要的译文修改说明。

官方许可文本：
- https://creativecommons.org/licenses/by-sa/4.0/
- https://creativecommons.org/licenses/by/4.0/

## 4. 三书素材例外：具体证据与初步分类

### HIS-A

出版社声明**约350张图片与地图**，是总的描述性规模，不是审核完成的精确独立资产数量。

A书内版权页明确：
- 原出版社的CC BY-SA不覆盖从第三方取得且采用其他CC条款（包括ND）或仅获得特殊许可的素材；
- 编辑方相信多数图片/图表经合理调查属于公有领域或兼容CC，但这不是对每个素材的**独立可复制保证**。

抽样的`Map 1.1 | Early Hominid Fossil Sites`在书中标注：作者Corey Parson、Original Work、CC BY-SA 4.0。属于可在遵守具体署名和ShareAlike条件后使用的**有积极授权证据的样本**，非全书图像白名单。

状态：
- `A_TEXT_LICENSE=VERIFIED`
- `A_MEDIA_COUNT_PUBLISHER_DESCRIPTION=ABOUT_350`
- `A_MEDIA_RIGHTS=PARTIALLY_VERIFIED_IN_SAMPLE`
- `A_FULL_IMAGE_AUDIT=NOT_DONE`

### HIS-B

大学原版书内版权说明明确：CC BY 4.0只适用于这本书**原创内容**，绝大部分图片是非作者原创，**专门为教材创作的原创地图**例外，每张图另有版权与许可证信息。

抽样的**第三方公开版本PDF**与大学出版社原著、作者、2022年引文及版权文字相符；但官方站提供约150.9MB PDF，本轮未下载并校验完全一致性，故第三方PDF里的图片授权行记为`PROVISIONAL_MATCH_NEEDS_OFFICIAL_FILE_CONFIRMATION`。

具体例子：
1. `Costume 16th Century Europe`：页面写`iStock Standard License (purchased by ETSU)`，**这是ETSU购买的使用许可，不是保证其他商业翻译站可再次使用的授权**。在没有独立可用授权前`EXCLUDE_COPY`，必要时可保留原书来源链接。
2. `Tibetan Wall Fresco`：页面同样写iStock Standard License；同样`EXCLUDE_COPY`。
3. `Map of Europe in 1500`：页面标注Eren Yetkinler / Wikimedia Commons / CC BY-SA 3.0。属于**可能可商业再利用**的图像，但须从原始文件页核实确切版本、作者、许可及改编条件，不将本书CC BY4.0代替图片CC BY-SA3.0。
4. 原创地图：出版社版权说明提供积极线索；**具体某张图是否出版社确有权利以及署名要求**仍需逐项核实。

状态：
- `B_TEXT_LICENSE=VERIFIED`
- `B_THIRD_PARTY_STOCK_IMAGE_SIGNAL=VERIFIED_IN_BOOK_COPY`
- `B_COPYRIGHT_TRANSFER_OR_SUBLICENSE_FOR_ISTOCK=NOT_VERIFIED`
- `B_ORIGINAL_MAP_RIGHTS=PARTIALLY_VERIFIED_CATEGORY_ONLY`
- `B_FULL_IMAGE_AUDIT=NOT_DONE`

参考版权页所在PDF第三方公开副本（非本站拟用的权威主源文件）：
https://www.maktaba.org/download/file/2008/World_history_since_1500_John_rankin_constanze_weise.pdf

### HIS-C

出版方明确正文CC BY 4.0；书内版权页特别说明**许多图片有不同的再利用权利，需查List of Illustrations**。书目元数据报告**9幅插图、14个表格**，但不等于9+14项已全部核准商业转载。

封面署名出现Al-Idrisi历史地图（Wikimedia来源）及Anna Gatti封面设计；**历史地图本身、其照片/数字扫描、设计排版各自具有可能不同的权利**。仅有图片来源链接不能证明可以合法商业重用整张出版社封面。

状态：
- `C_TEXT_LICENSE=VERIFIED`
- `C_ILLUSTRATIONS_PUBLISHER_COUNT=9`
- `C_TABLES_PUBLISHER_COUNT=14`
- `C_MEDIA_RIGHTS=PER_ITEM_REVIEW_REQUIRED`
- `C_FULL_IMAGE_AUDIT=NOT_DONE`

## 5. 未来媒体资产状态和最简审核字段

避免构建第二套复杂翻译工程。本阶段只定义一份轻量级素材清单格式，可在选定最终源文件后实施。

建议每行记录：
`source_book_id,source_edition_sha256,chapter,asset_id,asset_kind,caption_or_name,original_credit,original_source_url,individual_license_url,commercial_reuse_status,modification_status,decision,evidence_url,checked_at`

`commercial_reuse_status`：
- `VERIFIED_COMMERCIAL_AND_ADAPTATION`：源文件+具体许可和权利基础可复核。
- `VERIFIED_COMMERCIAL_NO_ADAPTATION`：可原样发布但不能按需要修改，后续图中文字翻译仍不得直接做。
- `RIGHTS_UNCLEAR`：许可/来源/权属不明，禁止复制，保留外链。
- `COMMERCIAL_REUSE_PROHIBITED`：明确限制商业复制，禁止。
- `OWN_LICENSE_REQUIRED`：如专有图库图片，除非另获本站独立许可，禁止。
- `PUBLIC_DOMAIN_VERIFIED`：公有领域依据和管辖区条件有可复核证据。

`decision`：
- `KEEP_AS_IS`
- `KEEP_WITH_ATTRIBUTION`
- `ADAPT_WITH_LICENSE_COMPLIANCE`
- `LINK_ORIGINAL_ONLY`
- `REPLACE_WITH_SEPARATELY_LICENSED_ASSET`
- `OMIT`

对应翻译/改编要求：
- 同一图片的**权利来源审查可在跨locale复用**，但翻译图中文字/重绘地图可能构成独立改编，需额外许可核实。
- 图片的各语言caption/alt可翻译，不等于有权编辑图像像素本身。
- 与书中引述的一幅图片不同，视频或音频**外链通常无需复制媒体本身**，但要检查有效链接，不建立只带外链的低价值页面。

## 6. 先期内容范围与质量检查

### 已可决定的结构

- `world-history`项目单一内容体系、每locale一个独立子域名。65个已实现Go locale前缀只读派生，`en-US`作为跨项目目标无Go生产主机名，原英语教材是否官方覆盖另行按正文判断。
- 在每locale站内**三本书共用域名**，以三套清楚的模块和独立许可证告知区分。
- HIS-A 12章 + HIS-B 15章提供跨年代通史主线，共27章。HIS-C 作为单独国际关系/比较文明专题（不是第28章或前两本直接续篇）。
- 每本需保留作者、出版社、源URL、书版本、原许可、翻译/改编者、修改时间、图表归属说明。
- 教材含大量**年代和地图信息**；历史年份、地名转写、争议性边界、考古解释、宗教文明名称必须单独语言审核。特别注意A是2016教材，对2026年新考古观点及历史学争议不能无条件标为最新学界定论。

### 没有获得的授权

- 本报告未将三个教材整体或全部图片设为`READY_TO_TRANSLATE`。
- 正式选择的**具体字节版次**尚未取得HASH，`EXACT_SOURCE_FILE_BYTES_FROZEN=NO`。
- 原图商业可复用的总体比例、图像版权核查时间、历史语言审核工作量、实际SEO和广告RPM均`UNKNOWN`。
- 本轮没有新增正式站点域名DNS，不开发、不导入内容、不翻译。

## 7. 停止线

以下任何情形出现，**停止将对应素材加入可发布白名单**，不需要停止整个HIS项目：

1. 单图像只记录`used with permission`、`purchased by publisher`、`Standard License`或`All Rights Reserved`，却没有覆盖本站独立商业用途的权利：`LINK_ORIGINAL_ONLY`或`OMIT`。
2. 图像为CC BY-ND等不允许改编，且必须翻译图中文字才能使用：只讨论原样保留/换图，不能直接修改。
3. 出版方声明CC BY/CC BY-SA，而单图像有独立不同许可证：**以图像自己的许可证为准**。
4. 图表或教材正文的权利范围存在无法分离的混合来源：不直接复制，必要时回到原作者或权利持有人取得明确授权。
5. 某章核心图像大范围不可用，致使内容体验明显下降：**先评估替换图片的合理成本和章节是否值得继续**，避免无图堆砌低价值翻译。
6. 研究过程中发现上游文件大幅版本差异，必须先明确原版版本身份再谈批量翻译。
7. go-dev v2投入受影响、准备成本明显超过可接受范围：保持`RESEARCH_ONLY`，暂停后续大范围媒体清单审查。

## 8. 本阶段结论和真正唯一下一步

`RESULT=PASS`
`STAGE=HIS_SOURCE_AND_MEDIA_LICENSED_SCOPE_FREEZE_RESEARCH`
`SECOND_PROJECT=WORLD_HISTORY`
`FORMAL_PROJECT_SELECTED=YES`
`SOURCE_BOOKS=3`
`CHRONOLOGICAL_SURVEY_CHAPTERS=27`
`SOURCE_SCOPE_BASELINE_FROZEN=YES`
`EXACT_SOURCE_FILE_BYTES_FROZEN=NO`
`TEXT_LICENSE_BASE=VERIFIED_FOR_DEFINED_SOURCES`
`ALL_MEDIA_REUSE_RIGHTS=INCOMPLETE`
`HIS_A_MEDIA_SAMPLE=CC_BY_SA_MAP_CANDIDATE`
`HIS_B_MEDIA_SAMPLE=ISTOCK_EXCLUDE_AND_CC_SA_MAP_CANDIDATE`
`HIS_C_MEDIA_SAMPLE=ILLUSTRATION_LIST_REQUIRED`
`RIGHTS_REVIEW_CAN_BE_REUSED_ACROSS_LOCALES=YES`
`COMMUNITY_TRANSLATION_EXCLUDES_LOCALE=NO`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN`
`AD_PAGE_RPM=UNKNOWN`
`LONG_TERM_AD_NET_PROFIT=UNKNOWN`

`NEXT=HIS_EDITION_HASH_AND_MEDIA_MINIMAL_SAMPLE_PILOT`

**仅在研究仓库**内进一步选定三本书的权威原始下载文件，为这三份文件记录真实SHA256/版本，并每本抽查少数对理解核心内容重要的图像，初步估算需替换/许可审核的比例和人力成本。**不得因此启动批量图片审计、66语言翻译或建站**。

### 研究限制记录

本轮尝试使用浏览器PDF截图工具检查版权页，但3份长PDF中部分下载超过工具限制或超时，截图无法成功。因此正文版权核实以出版社HTML与PDF可读取的页内授权文字为证据；未冒称完成逐页视觉检查。图片素材具体样本取自可追溯的书内文字署名及权利行。B的部分具体图像实例来自未与150.9MB官方文件做字节一致性验证的公开副本，正式白名单仍须核对出版社原始版本。
