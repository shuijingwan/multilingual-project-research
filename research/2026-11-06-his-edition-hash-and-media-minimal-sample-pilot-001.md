# 世界历史三本教材：权威源文件 SHA 与重要素材最小抽样 001

核实日期：2026-11-06
阶段：HIS_EDITION_HASH_AND_MEDIA_MINIMAL_SAMPLE_PILOT
状态：RESEARCH_ONLY
正式第二项目：WORLD_HISTORY
重要结论：**PARTIAL**（权威源身份与少量媒体许可可核实，原始文件SHA尚未取得）
域名：world-history，locale前缀与go-dev正式生产主机名完全一致
翻译/建站/DNS：NONE

## 一、本阶段的验证界限

本轮只读取出版方网页、正式出版/馆藏来源和个别图片**原始授权页面**，未进行任何源码导入、批量素材采集、翻译或部署。

对出版版本的 bibliographic identity 和对**精确 PDF 文件字节的 sha256**，必须区分：

- `BIBLIOGRAPHIC_IDENTITY=VERIFIED`：出版方、出版年份、ISBN/DOI、提供下载的官方来源。
- `OFFICIAL_BINARY_URL=VERIFIED_OR_RESOLVED`：知道下载入口或真实链接，但不代表成功下载。
- `EXACT_PDF_SHA256=UNKNOWN`：本阶段运行环境无法成功下载、校验三份完整的出版原件，**不得编造值、用Git blob SHA/ISBN/下载URL代替哈希**。
- `MEDIA_RIGHTS=VERIFIED_IN_SELECTED_SAMPLES`：部分图片在具体原始权利页面有许可/公有领域证据，**不等于全书可转载**。

此前 `SOURCE_SCOPE_BASELINE_FROZEN=YES`仅代表三本书名称及出版来源研究范围已确定；本轮 `EXACT_SOURCE_FILE_BYTES_FROZEN=NO`，这是明确的下一道门槛。

## 二、三份主源版本、候选下载路径及已知失败

### HIS-A：World History: Cultures, States, and Societies to 1500

出版社权威页面：
https://ung.edu/university-press/books/world-history-cultures-states-societies-to-1500.php

出版方下载链接（来自上述权威页面）：
https://web.ung.edu/media/university-press/World%20History%20Textbook-082817.pdf

- 出版年份2016、ISBN 978-1-940771-10-6；PDF文件名含082817，**不据文件名推断正式修订年份**。
- 正文CC BY-SA 4.0，第三方图片与其他许可/特殊允许除外。
- 网络PDF访问工具曾以“Content length is too large: 52210563”拒绝请求，未取得完整PDF；此处52,210,563是**访问工具返回的内容长度信息**，不是本站本地核验出的下载字节数。
- web PDF可读取书内文字与图片归属；截图工具访问失败，**不能视作完成视觉逐页校验**。

`A_OFFICIAL_PDF_URL=VERIFIED`
`A_LOCAL_PDF_SHA256=UNKNOWN`

### HIS-B：World History Since 1500: An Open and Free Textbook

ETSU原始来源：
https://dc.etsu.edu/etsu-oer/13/

网站“Download Full Text”指向：
https://dc.etsu.edu/cgi/viewcontent.cgi?article=1012&context=etsu-oer

- 原出版方推荐引注年份2022，作者John Rankin和Constanze Weise，15章，CC BY 4.0正文（仅适用原创内容）。
- 大学显示PDF约150.9MB；当前PDF访问工具对下载链接返回403，不代表出版社已撤销下载或禁止再分发；可能与工具访问环境有关。
- 第三方公开副本内容中出现iStock标准许可标记，但**本轮未验证其与2022权威原版字节或版本一致**；必须在最终文件核对前把该样本当成已观察到的**风险线索**，非完整权属清单。

`B_OFFICIAL_PDF_ENTRY=VERIFIED`
`B_DIRECT_FETCH_IN_CURRENT_TOOL=403`
`B_LOCAL_PDF_SHA256=UNKNOWN`

### HIS-C：History of International Relations: A Non-European Perspective

出版社权威页：
https://www.openbookpublishers.com/books/10.11647/obp.0074

出版社正式元数据：2019-07-31，DOI 10.11647/OBP.0074，PDF ISBN 978-1-78374-024-6，216页，9幅插图与14个表格。

**出版社长期存档合作方 Cambridge University Library / Thoth Archiving Network**：
https://thoth-arch.lib.cam.ac.uk/items/0cdf5338-b4e5-466d-bc26-95a26990d272

该机构页面明确列“Published version (26.97 MB)”，公开下载指向：
https://thoth-arch.lib.cam.ac.uk/bitstreams/4e701ba0-3d2f-477a-b82c-f77830e1a31f/download

但当前工具经该下载链接收到502，**没有取得完整PDF，也没有SHA**。

个别正式出版章节PDF可从出版社主机读取：
https://books.openbookpublishers.com/10.11647/obp.0074.05.pdf

此为**章节文件**，不能据其哈希代替整本书的官方文件哈希，也不代表整书已获完整素材授权。

`C_PUBLISHER_DOI_METADATA=VERIFIED`
`C_PUBLISHER_ARCHIVE_RECORD=VERIFIED`
`C_ARCHIVE_PDF_CURRENT_TOOL_FETCH=502`
`C_LOCAL_PDF_SHA256=UNKNOWN`

## 三、小规模图片与地图样本

**注意**：部分图注证据是PDF正文或二级副本的署名，只有查到原始图片权利页才有更强证据；所有结果仅适用于该图/对应原图版本。

| 样本 | 所属书 | 出版书内或原始权利线索 | 本轮证据与状态 | 后续处理 |
| --- | --- | --- | --- | --- |
| A-1: Map 1.1 Early Hominid Fossil Sites | HIS-A | 书内注明Corey Parson，Original Work，CC BY-SA 4.0 | `BOOK_CAPTION_LICENSE_VERIFIED`，尚未独立锁定图片原始文件SHA | 可进入逐图审核候选，标明作者、ShareAlike，不能直接当作全部可发布图像 |
| A-2: Map 1.2 The Spreading of Homo sapiens | HIS-A | 书内注明NordNordWest、Wikimedia Commons、Public Domain | `BOOK_CAPTION_PD_CLAIM_VERIFIED`；未核实对应Commons精确文件页/法域 | 不贸然列为所有司法辖区完全无权利限制 |
| B-1: 欧洲1500年地图（Europe 1500.png） | HIS-B（第三方副本图注关联） | Eren Yetkinler / Wikimedia Commons；Commons原图授权CC BY-SA **4.0** | `ORIGINAL_FILE_LICENSE=VERIFIED`；第三方PDF提及的3.0与Commons原图当前4.0存在**版本差异/指代歧义，待比对图像一致性** | 如果确认采用的是该Commons原图，按原图版本CC BY-SA4.0、作者/修改说明重新核准；不把书的CC BY4.0套给它 |
| B-2: iStock历史图片 | HIS-B（第三方书本副本） | “iStock Standard License (purchased by ETSU)” | `INDEPENDENT_COMMERCIAL_REUSE=NOT_VERIFIED` | 不能因ETSU曾购买许可就本站复用；默认`LINK_OR_REPLACE` |
| C-1: Tabula Rogeriana.jpg（出版社封面所引用的地图） | HIS-C | 出版社书内说明 Al-Idrisi地图、Wikimedia来源；Commons页面标记Public Domain Mark并讨论Konrad Miller 1929复制 | `ORIGINAL_COMMONS_FILE_PD_CLAIM=VERIFIED`，各司法辖区适用性与具体衍生版本仍需核实 | 可研究**直接使用原始地图文件**，但不可据此复用Open Book Publishers整个封面设计 |
| C-2: 出版社封面布局/设计 | HIS-C | 原书版权页署名Anna Gatti设计 | `COVER_DESIGN_COMMERCIAL_REUSE=UNKNOWN` | 封面设计与原始公有领域地图分离；不复制整张设计封面 |

### 图片原始权利与出版社证据URL

A原始出版社PDF（封面版权页、Map1.1与Map1.2书内注记）：
https://web.ung.edu/media/university-press/World%20History%20Textbook-082817.pdf

B欧洲1500年图（CC BY-SA4.0，来源：Wikimedia Commons原图）：
https://commons.wikimedia.org/wiki/File:Europe_1500.png

C地图（Commons公有领域声明，但注意法律管辖区差异）：
https://commons.wikimedia.org/wiki/File:TabulaRogeriana.jpg

C出版页面：
https://www.openbookpublishers.com/books/10.11647/obp.0074

世界历史图片许可策略（已有决定）：
`research/2026-11-06-his-unlicensed-media-hotlink-policy-001.md`

**未获具体可复制/可嵌入商业授权时，不使用热链接绕开许可证，优先指向官方原图页面或寻找已授权替代品。**

## 四、进度评价及成本边界

本轮不同来源素材覆盖深度和图像数量严重不匹配，抽样**不能估算全书可用图片占比、审核人时或总维护成本**：

- HIS-A出版社称约350图，不是已经审查350项。
- HIS-B含大量独立授权及专有图片，未知总数和可保留比例。
- HIS-C书目列9幅插图、14表格，样本没有覆盖其全套图片权利目录。

不能把三本不同来源的6个样本相加后换算“合法图片复用率”。当图片用于地图地名、政治边界或时间线，除了版权还需历史/语言准确性审核。

## 五、阻塞、证据归档与下一步唯一操作

本轮运行环境无法完整下载PDF：
- 外部Web PDF工具对A因文件长度拒绝；B官方链接返回403；C出版合作存档下载返回502。
- 当前本地容器没有可用的公网访问路径。
- 因此`EXACT_SOURCE_FILE_SHA256=UNKNOWN_FOR_ALL_3`，并非已经完成`FILE_BYTES_FREEZE`。

**下一步由项目维护者本地终端执行一次小范围下载+哈希证据采集**，强制：
1. 官方/出版社存档URL优先、禁止默默替换成第三方镜像。
2. 同时保存精确URL、UTC时间、有效文件头PDF、大小和sha256到`/tmp` evidence；不在公共Git仓库提交大PDF。
3. HTTP403、502、超时或HTML验证码不能当作已下载PDF；记录`FAILED`并保留证据，不伪造sha。
4. 下载可独立成功；任一失败不影响其余两本；终端只输出摘要与`===== FINAL =====`。
5. 如果三份均已取得，可以选择以后只读媒体抽样；不自动批量审计图片或启动翻译。

`RESULT=PARTIAL`
`STAGE=HIS_EDITION_HASH_AND_MEDIA_MINIMAL_SAMPLE_PILOT`
`SECOND_PROJECT=WORLD_HISTORY`
`SOURCE_BOOKS=3`
`BIBLIOGRAPHIC_IDENTITY=VERIFIED`
`OFFICIAL_DOWNLOAD_PATHS_IDENTIFIED=3`
`OFFICIAL_PDF_BYTES_VERIFIED=0`
`EXACT_SOURCE_FILE_SHA256=UNKNOWN_FOR_ALL_3`
`SELECTED_MEDIA_SAMPLES=6`
`MEDIA_FULL_CORPUS_REUSE_RIGHTS=UNKNOWN`
`MEDIA_SAMPLE_GLOBAL_REUSE_RATE=NOT_ESTIMABLE`
`RESEARCH_ONLY=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_OFFICIAL_PDF_LOCAL_HASH_EVIDENCE_COLLECTION`
