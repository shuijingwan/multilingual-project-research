# 世界历史第二项目：仅发布网页与优先使用官方HTML源的决策和核查 001

核实日期：2026-11-06
阶段：HIS_WEB_HTML_SOURCE_PRIORITY_AND_ACCESS_PILOT
项目状态：RESEARCH_ONLY
第二项目：WORLD_HISTORY（正式选定）
项目域名：world-history；locale前缀严格复用go-dev正式生产映射

## 一、负责人新指示（本报告最高优先原则）

**世界历史及未来自建项目只向用户提供网页形式的内容。** 如果上游教材已经有合法开放的网页正文，优先将其作为内容提取/翻译输入；尽量复用标题、章节、表格、图片说明、脚注等内容结构，避免先将PDF反向拆为网页，也避免为每本教材重新设计一套阅读页面。

这里的“复用网页”必须拆开：

- **正文与语义结构**：在原著明确允许商业翻译改编的CC许可证范围内，可把被许可的文本、章节标题、表格、列表、脚注和相关必要结构作为内容数据进行转换。
- **出版平台的页面设计与技术资产**：HTML中混有导航、模板、CSS、JS、登录功能、追踪脚本、站点商标、特别授权的图库、图像CDN等；它们**不能因为文章正文开放就默认也允许复制和再发布**。
- **本站界面**：可以设计**一个跨三本书与各locale复用的极简阅读模板**，而不是每本书重新设计；复用go-dev已有的工程经验但**不修改go-dev项目**。不直接镜像上游页面视觉设计或整页HTML+CSS+JS。
- **目标交付**：始终是网页。XML、EPUB、Word若比HTML可靠，可作为转换源；PDF优先留为出版版权、排版、内容一致性证明和必要时的后备输入。用户并未授权翻译源只允许HTML，而是明确“有网页时最好”。

`PUBLISHED_FORMAT=WEB_ONLY`
`SOURCE_PRIORITY=OFFICIAL_FULLTEXT_HTML_FIRST`
`ALTERNATIVE_SOURCE=OFFICIAL_XML_EPUB_WORD_IF_NEEDED`
`PDF_ROLE=EDITION_LICENSE_EVIDENCE_AND_FALLBACK`
`COPY_SOURCE_WEBSITE_TEMPLATE=NOT_AUTHORIZED`
`COMMON_SITE_READING_TEMPLATE=DESIRED_MINIMAL`
`NO_NEW_ENGINEERING_AT_RESEARCH_STAGE=YES`

## 二、三本书网页正文的真实可访问性复核

### HIS-A：World History: Cultures, States, and Societies to 1500

OpenALG / Affordable Learning Georgia Manifold官方关联项目页：
https://alg.manifoldapp.org/projects/world-history

已验证：
- 12章目录可浏览。
- 直接点击第1章实际进入含**连续英文正文**的网页，而不是只有出版社书目元数据或嵌入PDF：
  https://alg.manifoldapp.org/read/world-history/section/26bcf032-404d-4c85-9f3b-6c0cafa5cc25
- 第1章页面包含`1.1 CHRONOLOGY`时间表、`1.2 INTRODUCTION`正文、引文/脚注、`1.3 QUESTIONS`问题清单、`1.4 KEY TERMS`术语、`1.5 HUMAN BEGINNINGS IN AFRICA`及`Map 1.1`等具有具体署名许可证的图片说明。
- HTML页面下的作品元数据明示CC BY-SA 4.0；但图片仍受各项具体授权约束。
- 项目同时列出`Download Accessible Word Doc`，可作为内容一致性校验/后备。
- 注意原文字中有“environ- ments”及年代等排版/历史编辑瑕疵，不能把网页可读性等同于可直接自动翻译无需审核。

判断：
`A_FULL_TEXT_HTML_CHAPTER_SAMPLE=VERIFIED`
`A_HTML_STRUCTURAL_ELEMENTS=VERIFIED_IN_CH1`
`A_ALL_12_CHAPTERS_HTML_FULLTEXT_COMPLETENESS=NOT_YET_VERIFIED`
`A_SOURCE_PRIORITY=HTML`
`A_WORD_BACKUP=LISTED_NOT_HASHED`

### HIS-B：World History Since 1500: An Open and Free Textbook

权威原始页：
https://dc.etsu.edu/etsu-oer/13/

已验证：
- 官方书目页提供**书目说明、作者、版权声明和PDF下载**，声称可以“viewed online”。
- 此页HTML**没有15章逐章全文正文**；不能把“出版社页面是HTML”误称“教材正文可直接以HTML提取”。
- 二级目录Open Textbook Library列出的可用技术格式是PDF；不是确定的官方HTML。
- 官方PDF入口用户本地curl HTTP 403，不能由此断言版权撤回或整书不可用。
- 尚未核实公开的官方Markdown/Word/XML/EPUB/逐章HTML或源码仓库。

判断：
`B_PUBLISHER_BOOK_LANDING_HTML=VERIFIED`
`B_FULL_TEXT_SEMANTIC_HTML=NOT_FOUND_IN_SAMPLE`
`B_PDF_DOWNLOAD_IN_USER_TERMINAL=HTTP_403`
`B_SOURCE_PRIORITY=FIND_OFFICIAL_HTML_OR_EDITABLE_MASTER_ELSE_PDF_FALLBACK`

### HIS-C：History of International Relations: A Non-European Perspective

出版社作品页：
https://www.openbookpublishers.com/books/10.11647/obp.0074

已验证：
- 出版社元数据明确列出独立HTML、XML、EPUB格式ISBN和Read Online入口。
- 出版社第1章页面：https://www.openbookpublishers.com/books/10.11647/obp.0074/chapters/10.11647/obp.0074.01
- **关键限制**：当前可读取的第1章页面仅展示章节标题、DOI、版权、作者和“Read Online / Download”控件，**没有实际第1章连续正文**。不能把章节入口网页存在误记为完整结构化HTML正文已经核验。
- 本轮尝试猜测的`books.openbookpublishers.com/10.11647/obp.0074.html`等URL不可用；不应假定已找到可抓取的实际HTML全文路径。
- 现已有用户本地官方PDF文件，其SHA256已核验（见下），可以保留为对照；更适合继续确认出版社提供的实际HTML/XML/EPUB入口是否可取得。

判断：
`C_HTML_FORMAT_LISTED=VERIFIED`
`C_CHAPTER_METADATA_HTML=VERIFIED`
`C_FULL_TEXT_HTML_PAYLOAD=NOT_YET_VERIFIED`
`C_XML_EPUB_FORMAT=LISTED_NOT_DOWNLOADED`
`C_SOURCE_PRIORITY=ACTUAL_HTML_TEXT_OR_XML_EPUB_IF_ACCESSIBLE`

**C从“页面声称Read Online”到“已取得可重用正文HTML”仍存在未解决的证据缺口，不能含糊。**

## 三、把“避免设计页面”落实为最小工程原则

高价值的源网页复用范围：
1. 逻辑章节、节、标题、正文段落、列表、时间表。
2. 引用、脚注、来源链接、图片caption与授权信息。
3. 三书各自独立的版权与来源元数据。

不建议作为翻译源直接复制：
- 出版商logo、网站页眉页脚、站点导航与注册/标注UI。
- 外部平台JavaScript/CSS/排版资源或Cookie/分析脚本。
- 授权不明的图库图片、封面、音视频。
- 需要平台API服务支持才能工作的组件。

工程原则：**一本书的内容数据与一个共用的阅读页面渲染器分开**。三本书不需要三套视觉设计；跨locale不需要逐语言重新设计结构。此为设计指导，不等于授权此轮新建渲染器或第二套翻译基础设施。

源网页可能有嵌入手工排版错误及修订差异，后续正式内容版本需有具体抓取记录或文件哈希，不能用URL本身冒充不可变源。

## 四、两份已有PDF证据继续保留

负责人本地已核验：
- HIS-A：52,210,563 bytes；SHA-256 `d034e3b6900a8f533b10760d9796b3b32f5299acda6b7d0b326965a37b469340`。
- HIS-C：28,279,108 bytes；SHA-256 `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`。
- HIS-B：官网PDF请求HTTP403；SHA未知。

旧阶段HIS_B_OFFICIAL_DOWNLOAD_RECOVERY不再是唯一必须先解决的阻塞。

## 五、正式停止线与下一步

本轮只核实**三本教材网页是否真的呈现正文、不是只有出版社书目或PDF查看器**。不批量镜像网站、不复制全部HTML、不下载整本图片、不创建网站。

`RESULT=PASS`
`STAGE=HIS_WEB_HTML_SOURCE_PRIORITY_AND_ACCESS_PILOT`
`SECOND_PROJECT=WORLD_HISTORY`
`FORMAL_PROJECT_SELECTED=YES`
`PUBLISHED_FORMAT=WEB_ONLY`
`OFFICIAL_HTML_FIRST=YES`
`A_CHAPTER_FULLTEXT_HTML=VERIFIED_SAMPLE`
`B_CHAPTER_FULLTEXT_HTML=NOT_FOUND_IN_SAMPLE`
`C_CHAPTER_FULLTEXT_HTML=NOT_YET_VERIFIED`
`SOURCE_WEBSITE_CODE_OPEN_LICENSE=NOT_ESTABLISHED`
`PDF_MANDATORY=NO`
`GO_DEV_MUTATION=NONE`
`RESEARCH_ONLY=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`NEXT=HIS_HTML_CHAPTER_CONTENT_AND_SOURCE_ACCESS_MINIMAL_GATE`

下一步只读核查：A首中末3章是否有真实连续HTML正文；C从Read Online入口能否取得全文HTML/XML/EPUB，不再把章节书目元数据当正文；B检索是否有权威 HTML 全文链接。若C需要浏览器登录/JS而不能简单读取，明确记为技术获取障碍，不启动为单本书构建复杂抓取基础设施。

核实来源（2026-11-06）：
- https://alg.manifoldapp.org/projects/world-history
- https://alg.manifoldapp.org/read/world-history/section/26bcf032-404d-4c85-9f3b-6c0cafa5cc25
- https://dc.etsu.edu/etsu-oer/13/
- https://open.umn.edu/opentextbooks/textbooks/world-history-since-1500-an-open-and-free-textbook
- https://www.openbookpublishers.com/books/10.11647/obp.0074
- https://www.openbookpublishers.com/books/10.11647/obp.0074/chapters/10.11647/obp.0074.01

不开启正式翻译、不建站、不新增DNS、不修改go-dev v2。
