# HIS-C：BCcampus XML 下载403停止线与Open Library EPUB替代源评估 001

核实日期：2026-11-06
阶段：HIS_C_XML_403_STOP_AND_EPUB_FALLBACK_GATE
项目：WORLD_HISTORY（第二项目已正式选择）
状态：RESEARCH_ONLY
项目域名标识：world-history；locale前缀严格对应Go正式生产映射
最终发布内容形式：WEB_ONLY
工程原则：现成完整HTML优先，非网页结构化源只作为网页内容转换输入；少量样式优化优先于重做页面

## 1. 维护者本地实际执行证据

正式前驱研究：
`research/2026-11-06-his-c-xml-file-provenance-and-download-gate-001.md`

维护者2026-11-06给出的精确结果：

```
RESULT=PARTIAL
STAGE=HIS_C_XML_LOCAL_DOWNLOAD_AND_STRUCTURE_PROOF
DOWNLOAD=FAILED
HTTP=403
EVIDENCE=/tmp/mpr-his-c-xml-qJKQx7yt
LOG=/tmp/mpr-his-c-xml-qJKQx7yt/full.log
```

下载失败的是BCcampus公开目录中XML选项对应的ZIP：
https://cdn2.repo.bccws.ca/resources/textbooks/153/formats/Ringmar_History_of_International_Relations_xml_369715013b.zip

结论：
- `BCCAMPUS_XML_ZIP_URI=VERIFIED`
- `BCCAMPUS_XML_USER_TERMINAL_HTTP=403`
- `BCCAMPUS_XML_BYTES=NOT_OBTAINED`
- `XML_FILES_INSIDE_ARCHIVE=UNKNOWN`
- `FULL_TEXT_COMPLETENESS=UNKNOWN`
- `BCCAMPUS_XML_RETRY=PAUSED`

HTTP403不是明确版权禁止或资源不存在的法律/内容证据，但当前不值得继续轮换Referer/UA、反复盲试或专门建立抓取器。

## 2. 原出版社仍是最高身份/许可权威

Open Book Publishers：
https://www.openbookpublishers.com/books/10.11647/obp.0074

- Erik Ringmar，2019年，DOI 10.11647/OBP.0074。
- ISBN：PDF 978-1-78374-024-6、HTML 978-1-80064-498-4、XML 978-1-78374-778-8、EPUB 978-1-78374-025-3。
- CC BY 4.0正文，部分图片另有授权。
- 出版社章节目录有8章；当前可直接读取的官方章节入口仍主要是书目及Read Online控件，**真实HTML连续正文未获验证**。
- 负责人已有出版社PDF字节证据：28279108 bytes，SHA256 `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`。

不能把XML/EPUB ISBN列表当作可下载的出版方源文件，更不能把PDF SHA用来证明EPUB内容一致。

## 3. 新发现：Open Library/Internet Archive EPUB可用的公开索引入口

Open Library记录：
https://openlibrary.org/books/OL28354015M/History_of_International_Relations

机构：Internet Archive旗下Open Library。该书目明确：
- 作者Erik Ringmar，出版社Open Book Publishers，2019；
- Internet Archive item `b7790cae-1901-446e-b529-b5fe393d8061`；
- `PDF`、`Plain text`、`ePub`、`DAISY`公开下载入口；
- ISBN 9781783740246，与出版社PDF版本号一致。

**已通过Open Library中的下载项链接确立的ePub URL**：

https://archive.org/download/b7790cae-1901-446e-b529-b5fe393d8061/b7790cae-1901-446e-b529-b5fe393d8061.epub

本轮Web访问该URL时跳转到archive.org节点（dn720002.ca.archive.org）后未能访问，**未取得EPUB字节**。这只是另一种内容来源候选，不代表该EPUB真正可由本地下载，亦不能证明它是出版社原生EPUB：

- Internet Archive的EPUB可能是扫描/OCR派生格式，出现分页断裂、章节标题误识、文本乱码、引用错位、插图文字问题。
- 实际ZIP包、OPF目录、HTML/XHTML正文、章数、字符质量、与官方PDF内容对照均未核验。
- Archive保管的原著许可仍以出版社原版及各素材的具体授权为准；档案本身的网页代码或图片不自动获得许可。

当前状态：
`OPENLIBRARY_2019_BOOK_MATCH=VERIFIED_BIBLIOGRAPHIC`
`OPENLIBRARY_EPUB_LINK=VERIFIED`
`OPENLIBRARY_EPUB_BYTES=UNKNOWN`
`OPENLIBRARY_EPUB_ORIGIN_NATIVE_OR_OCR=UNKNOWN`
`OPENLIBRARY_EPUB_FULL_TEXT=UNKNOWN`
`OPENLIBRARY_EPUB_EDITION_PARITY=UNKNOWN`

## 4. 保持内容来源与网页输出的正确关系

- 项目最终仍只提供HTML网页，不能因发现EPUB而改成需要用户下载电子书。
- 优先使用有连续正文且许可清晰的官方HTML（HIS-A已抽样3章成功）。
- HIS-C如果无法实际取得官方完整HTML/XML，可尝试对已公开可取得的EPUB做轻量阅读结构验证；结果不合格立即停止该路线，保留用户已验证的出版社PDF为版次和内容对照依据。
- EPUB内容通常可包含XHTML，但“文件扩展名EPUB”本身不等于自动具有准确的可翻译语义结构，更不是原站页面模板源码。
- 只允许按原著和具体图像许可处理商业翻译；未知第三方素材继续`LINK_ORIGINAL_PAGE_ONLY_OR_OMIT`，不通过热链接规避授权。

## 5. 下一步最小门禁（不启动工程）

`NEXT=HIS_C_OPEN_LIBRARY_EPUB_LOCAL_PROOF`

**唯一下一步**：维护者本地仅尝试该一份Open Library EPUB：
1. 记录请求状态、最终URL、文件字节数和SHA256；失败保留HTTP错误证据。
2. 利用Python标准库`zipfile`在**不解压、不执行内部代码**的条件下确认EPUB的`mimetype`、`META-INF/container.xml`、.opf、.xhtml/.html成员数量及受限范围样本。
3. 如果合法ZIP却没有清楚的文本结构，标记`FORMAT_UNSUITABLE`或`QUALITY_UNKNOWN`，不盲目开发OCR转换管线。
4. 禁止下载整本书图片、批量镜像、正式翻译、部署、DNS修改，禁止修改go-dev。
5. 对XML直链403设置停止线，只有找到可靠的官方新来源或用户提供正常可取得文件时再复开。

## 六、本轮结论

`RESULT=PASS`
`STAGE=HIS_C_XML_403_STOP_AND_EPUB_FALLBACK_GATE`
`SECOND_PROJECT=WORLD_HISTORY`
`BC_CAMPUS_XML=BLOCKED_HTTP_403`
`XML_RETRY=PAUSED`
`OPENLIBRARY_EPUB_URL=VERIFIED`
`OPENLIBRARY_EPUB_BYTES=UNKNOWN`
`PUBLISHED_FORMAT=WEB_ONLY`
`HIS_C_PDF_SHA256_VERIFIED=YES`
`FORMAL_PROJECT_SELECTED=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_C_OPEN_LIBRARY_EPUB_LOCAL_PROOF`

不由于某一转换源访问失败重新选择第二项目，不进行高成本绕过访问限制工作。
