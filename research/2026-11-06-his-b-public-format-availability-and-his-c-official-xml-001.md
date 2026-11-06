# HIS-B公开源格式核查与HIS-C官方XML取得记录

核实日期：2026-11-06
阶段：HIS_B_PUBLIC_FORMAT_AVAILABILITY_AND_HIS_C_OFFICIAL_XML
状态：RESEARCH_ONLY
正式第二项目：WORLD_HISTORY
本站发布格式：WEB_ONLY
内容输入许可与来源：OFFICIAL_SOURCE_ONLY

## 一、HIS-B是否只有PDF？

目前**公开可核实**的信息：
- East Tennessee State University官方书目 https://dc.etsu.edu/etsu-oer/13/ 只提供PDF下载，网页上的“viewed online”不等于正文HTML。
- University of Minnesota Open Textbook Library：https://open.umn.edu/opentextbooks/textbooks/world-history-since-1500-an-open-and-free-textbook ，`Formats Available: PDF`。
- MERLOT：https://www.merlot.org/merlot/viewMaterial.htm?id=773417474 ，`Technical Format: PDF`。
- 针对书名与两位作者的HTML/XML/EPUB/Word/Pressbooks/GitHub原稿公开检索，**未找到该书可验证的完整官方结构化源**。

`HIS_B_PUBLIC_OFFICIAL_FORMAT=PDF_VERIFIED`
`HIS_B_OFFICIAL_FULLTEXT_HTML=NOT_FOUND_IN_SAMPLE`
`HIS_B_OFFICIAL_XML=NOT_FOUND_IN_SAMPLE`
`HIS_B_OFFICIAL_EPUB_OR_WORD=NOT_FOUND_IN_SAMPLE`
`HIS_B_OTHER_FORMAT_IMPOSSIBLE=NO`

理由：**未找到公开版本**和**出版社未保留或无法提供其它格式**是两个不同结论。负责人已从ETSU官方使用浏览器下载233页PDF，且本地SHA核对PASS，因此完整官方文本来源已经取得，不因此影响项目方向。

### 可能存在的原始结构化文件

HIS-B官方PDF的本地元数据`Producer=Prince 15.4.1`。Prince官方说明其PDF输入通常可以是HTML或XML（https://www.princexml.com/doc/prince-input/）。

这只是**制作流程有结构化输入的积极线索**，**不证明ETSU确实保留了该次生成的原始文件，也不证明原始文件公开或可商用分发**。如果未来希望避免PDF转HTML结构提取的成本，最有价值的下一调查是询问ETSU数字馆藏或原作者是否可提供官方Word、HTML、XML或电子书排版源稿。ETSU出版文件中有数字馆藏联系入口`digilib@etsu.edu`，但发送询问须由负责人决定，未发送邮件。

### 合理的路线

1. **已获取的官方PDF始终保持正式输入候选**，不要为搜寻不存在证据的HTML延误所有后续准备。
2. 优先询问ETSU是否可以提供官方可编辑源，若有即按其真实文件URL和SHA验证。
3. 如果没有，使用当前**官方PDF转换成自己的语义HTML**，仔细核验双栏阅读顺序、章节、脚注、表格、图片版权；**从官方PDF转换出来的HTML仍是官方原著内容的衍生处理**，不违反`TRANSLATION_SOURCE_OFFICIAL_ONLY`，但质量需独立核验。
4. 不使用第三方镜像的正文替代官网原版，不因curl403放弃浏览器手动下载。

## 二、HIS-C来自官方出版社的XML已经实际下载成功

2026-11-06负责人从Open Book Publishers官方页面下载：
https://www.openbookpublishers.com/books/10.11647/obp.0074
文件：`~/下载/obp.0074.zip`

维护者本地报告：
```
RESULT=PASS
STAGE=HIS_C_OFFICIAL_XML_STRUCTURE_PROOF
ZIP_BYTES=18366184
ZIP_SHA256=ef00fa6df2eeffa73f05188e26f07810eb21f1a327bda0875efba94345bb82f0
ARCHIVE_MEMBERS=132
UNCOMPRESSED_BYTES=19534238
ZIP_VALID=YES
XML_FILES=14
HTML_XHTML_FILES=0
XML_PARSED=14
CHAPTER_ELEMENT_SIGNALS=0
TITLE_SIGNAL=True
AUTHOR_SIGNAL=True
EXTRACTED_SAMPLE_WORDS=103296
STRUCTURE=PASS
FULL_TEXT_COMPLETENESS=UNKNOWN
OFFICIAL_PDF_PARITY=NOT_YET_CHECKED
```

**不要把`CHAPTER_ELEMENT_SIGNALS=0`误报成正文没有章节。** 压缩包确有`XML-edition/ch1.xml`至其他章命名，且14个XML均通过解析；简单脚本仅找`chapter`标签和带`type=chapter`的div，可能漏掉实际原稿采用的标签结构。下一步应检查XML标签和命名空间、实际章文件是否涵盖出版社声明的8章，以及首中末正文与出版社PDF的内容对应。

`HIS_C_OFFICIAL_XML_ORIGIN=VERIFIED_BY_USER_DOWNLOAD`
`HIS_C_XML_SHA256_VERIFIED=YES`
`HIS_C_XML_STRUCTURAL_PARSE=PASS`
`HIS_C_XML_CONTENT_COMPLETENESS=UNKNOWN`
`HIS_C_XML_PUBLISHER_PDF_PARITY=UNKNOWN`
`HIS_C_OPENLIBRARY_EPUB_TRANSLATION_AUTHORITY=NO`

## 三、下一步与停止线

`NEXT=HIS_C_XML_CONTENT_AND_OFFICIAL_PDF_PARITY_REVIEW`

先完成已获得的出版社官方XML与出版社官方PDF的有限章级一致性证明，避免因HIS-B官方原稿公开性UNKNOWN而无限搜寻。

HIS-B是否还有官方Word/HTML/XML的唯一高价值补查是**向ETSU数字馆藏咨询**，非继续泛搜第三方镜像；如果无法取得，官方PDF转HTML是合规的后备方案。

`RESULT=PASS`
`STAGE=HIS_B_PUBLIC_FORMAT_AVAILABILITY_AND_HIS_C_OFFICIAL_XML`
`SECOND_PROJECT=WORLD_HISTORY`
`HIS_B_PUBLIC_VERIFIED_FORMAT=PDF_ONLY_FOUND`
`HIS_B_OTHER_FORMATS=UNKNOWN_NOT_PROVEN_NONEXISTENT`
`HIS_B_OFFICIAL_PDF_OBTAINED=YES`
`HIS_C_OFFICIAL_XML_OBTAINED=YES`
`HIS_C_OFFICIAL_XML_SHA256=ef00fa6df2eeffa73f05188e26f07810eb21f1a327bda0875efba94345bb82f0`
`TRANSLATION_SOURCE_OFFICIAL_ONLY=YES`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`NEXT=HIS_C_XML_CONTENT_AND_OFFICIAL_PDF_PARITY_REVIEW`
