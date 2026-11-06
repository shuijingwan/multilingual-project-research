# 世界历史第二项目：翻译源格式优先级纠正与PDF证据用途说明 001

核实日期：2026-11-06
阶段：HIS_STRUCTURED_SOURCE_BEFORE_PDF_RECOVERY_DECISION
状态：RESEARCH_ONLY
第二项目：WORLD_HISTORY
域名标识：world-history（locale前缀严格沿用go-dev生产身份）
源文件格式选择：仍属研究阶段，未授权正式翻译/建站

## 一、负责人提出的核心纠偏

负责人于2026-11-06提出：下载PDF到底是为了固定研究证据，还是要作为正式翻译源？三本教材是否原本就拥有可用的开放网站源码？

结论：

1. **PDF下载并计算SHA-256的主要目的**是固定出版版本、核实原著正文及素材授权、保留可复现证据。**它不是强制使用PDF作为翻译输入的决定。**
2. 教材正文采用CC BY / CC BY-SA等允许商业改编的许可证，与出版社网站软件、排版模板、原始Word/HTML/XML/EPUB源稿是否公开或独立授权，属于不同问题。**“开放教材”不意味着“网站代码和所有媒体开源”。**
3. 在正式翻译项目中，若能取得可靠的官方Word/XML/EPUB/HTML并验证其版本、章节完整性、素材权利，应优先它们；PDF可继续作为**出版证据和版式校对基准**。
4. 不再将`HIS-B_OFFICIAL_PDF_HTTP_403`当成阻碍其他来源格式调查的唯一下一步。**先审查三本书是否存在可取得的权威结构化来源**，再决定PDF下载问题是否值得花时间。

## 二、三本书的当前具体来源信号

### HIS-A：World History: Cultures, States, and Societies to 1500

官方出版页：
https://ung.edu/university-press/books/world-history-cultures-states-societies-to-1500.php

关联的Affordable Learning Georgia / OpenALG Manifold正文：
https://alg.manifoldapp.org/projects/world-history

证据：
- Manifold公开书目及章节导航：12章完整目录；
- “Start Reading”可逐章阅读并呈现标题、正文、图片署名、引用和表格；
- 书目页面**明确提供**“Download Accessible Word Doc”及“Download Accessible PDF”；
- 阅读页例证：https://alg.manifoldapp.org/read/world-history/section/26bcf032-404d-4c85-9f3b-6c0cafa5cc25
- 原生可编辑版本存在积极证据，但**尚未实际下载Word并核验其文件字节、章数或与出版PDF的一致性**。
- 教材正文CC BY-SA 4.0；图像逐项许可证例外仍适用。

`A_STRUCTURED_ONLINE_HTML=VERIFIED`
`A_ACCESSIBLE_WORD_DOWNLOAD_LISTED=VERIFIED`
`A_WORD_BYTES_SHA256=UNKNOWN`
`A_FORMAT_CONTENT_PARITY=UNKNOWN`
`A_PREFERRED_TRANSLATION_SOURCE_CANDIDATE=WORD_OR_HTML`

### HIS-B：World History Since 1500: An Open and Free Textbook

ETSU官方出版页：
https://dc.etsu.edu/etsu-oer/13/

证据：
- 官方明确显示“Download Full Text (150.9 MB)”的PDF下载入口；
- 官方描述称书可以下载为PDF或在线阅读，但当前没有核实到**独立的、可获取的HTML全文/Word/XML/EPUB或源码仓库**；在线阅读可能是PDF查看器，不能凭文案推断结构化HTML源存在；
- 当前curl到官方PDF入口返回403；
- 第三方Open Textbook Library目前只列PDF，而且其CC BY-SA标签**与ETSU官方CC BY 4.0说明不一致**，必须以确定具体出版版次的权利文档为优先，不能混用二级目录的错误或不同版次授权。

`B_OFFICIAL_PDF_URL=VERIFIED`
`B_HTTP_403_IN_LOCAL_CURL=VERIFIED`
`B_AUTHORITATIVE_STRUCTURED_SOURCE=NOT_FOUND_IN_SAMPLE`
`B_GITHUB_SOURCE_REPOSITORY=NOT_VERIFIED`
`B_PDF_MAY_BE_FALLBACK=YES`

### HIS-C：History of International Relations: A Non-European Perspective

出版方官方页：
https://www.openbookpublishers.com/books/10.11647/obp.0074

证据：
- 出版社列出**HTML ISBN 978-1-80064-498-4**，**XML ISBN 978-1-78374-778-8**，**EPUB ISBN 978-1-78374-025-3**，以及PDF ISBN；
- 出版社有逐章HTML阅读入口（例如Intro）：
https://www.openbookpublishers.com/books/10.11647/obp.0074/chapters/10.11647/obp.0074.01
- 已核实HTML阅读页存在，但具体书籍XML/EPUB下载文件是否能直接访问、结构、完整性及哈希**尚未验证**；
- 出版社确有开源出版软件及GitHub组织（https://www.openbookpublishers.com/open-software），但这**不是该书正文原稿已在GitHub开源的证据**。

`C_HTML_READING=VERIFIED`
`C_XML_EPUB_FORMAT_LISTED=VERIFIED`
`C_XML_EPUB_BYTES=UNKNOWN`
`C_BOOK_GITHUB_SOURCE=NOT_VERIFIED`
`C_PREFERRED_TRANSLATION_SOURCE_CANDIDATE=XML_OR_EPUB_OR_HTML`

## 三、已有PDF哈希证据仍然有效

项目负责人的本地只读验证，2026-11-06：

| 来源 | 当前已有本地PDF | 大小(bytes) | SHA-256 |
| --- | --- | ---: | --- |
| HIS-A | YES | 52210563 | d034e3b6900a8f533b10760d9796b3b32f5299acda6b7d0b326965a37b469340 |
| HIS-B | NO (HTTP403) | UNKNOWN | UNKNOWN |
| HIS-C | YES | 28279108 | 7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238 |

原始Evidence路径（仅维护者本机临时目录；不推断持久存在）：
`/tmp/mpr-his-pdf-Ny7smHlP/sha256.tsv`

这两份SHA说明已下载文件可重现**字节身份**，并不证明所有媒体取得商业再发布权利，也不强制PDF成为机器翻译原料。文件未提交公开Git仓库。

## 四、源文件优先级与下一步

目标是在不启动工程开发的情况下，最少操作选择最可维护的原始翻译输入：

`PREFERRED=AUTHORITATIVE_STRUCTURED_SOURCE`
`CANDIDATE_FORMATS=WORD,XML,EPUB,HTML`
`PDF_ROLE=EDITION_AND_LICENSE_EVIDENCE_PLUS_FALLBACK`
`BOOK_SITE_SOURCE_CODE_OPENNESS=NOT_ESTABLISHED_FOR_ALL_3`

源选择的低成本评估顺序：
1. HIS-A只读核实OpenALG “Accessible Word Doc”文件实际格式、有效文件头、文件大小、是否可识别12章；可另核对一个HTML章节与已取得PDF的对应内容。
2. HIS-C只读确认XML/EPUB是可下载的完整版本还是只有ISBN登记，并对单章HTML与当前PDF做章节级对应验证。
3. HIS-B查找确实可访问的官方可编辑文件或官方全文HTML；如不存在，保留PDF/浏览器手动下载作为退路，避免盲目重复403请求。
4. 对每一份候选源分别核实版权信息与第三方图片：**文件格式更友好不自动赋予文件中图片额外授权**。

**只有上游文件有实际字节且核验章节/内容对应之后，才能将某格式正式确定为翻译源；本轮仅作来源策略选择。**

`RESULT=PASS`
`STAGE=HIS_STRUCTURED_SOURCE_BEFORE_PDF_RECOVERY_DECISION`
`SECOND_PROJECT=WORLD_HISTORY`
`FORMAL_PROJECT_SELECTED=YES`
`A_PDF_SHA256_VERIFIED=YES`
`C_PDF_SHA256_VERIFIED=YES`
`B_PDF_HTTP_403=YES`
`A_WORD_AVAILABLE_AS_LISTED_FORMAT=YES`
`C_XML_EPUB_FORMATS_LISTED=YES`
`STRUCTURED_SOURCE_BYTES_VERIFIED=NO`
`MUST_DOWNLOAD_ALL_3_PDFS_BEFORE_TRANSLATION=NO`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_AUTHORITATIVE_STRUCTURED_SOURCE_FORMAT_PILOT`

不翻译、不建站、不修改go-dev，不新增DNS，不采购。
