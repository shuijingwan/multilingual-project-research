# 世界历史项目：HTML正文可用性小样本门禁与轻量阅读界面决策 001

核实日期：2026-11-06
STAGE=HIS_HTML_CHAPTER_CONTENT_AND_SOURCE_ACCESS_MINIMAL_GATE
SECOND_PROJECT=WORLD_HISTORY
FORMAL_PROJECT_SELECTED=YES
PROJECT_DOMAIN_SLUG=world-history
LOCALE_PREFIX_RULE=EXACT_GO_DEV_PRODUCTION_HOST_PREFIX
STATUS=RESEARCH_ONLY

## 一、项目负责人新增的网页呈现取舍

项目负责人确认：

1. 最终商业网站仅提供网页阅读内容。
2. HIS-A 原有 OpenALG/Manifold 阅读页当前体验可以接受。
3. 将来可能只需让正文阅读区域**加宽、接近全屏**，改善排版与阅读体验。
4. **不排除重新设计一个新网页模板**：如果原始HTML页面的视觉与功能确实不适合本站；但不预先为了设计而投入大量前端工程。
5. 核心优先级是减少不必要的页面设计和内容格式转换工作。

正式记录为 **`HTML_SEMANTIC_CONTENT_FIRST` + `MINIMAL_READING_STYLE_ADJUSTMENT_FIRST` + `REDESIGN_ONLY_IF_USER_VALUE_JUSTIFIES`**。

不可混淆：
- 原著的CC BY / CC BY-SA许可所覆盖的**正文及其语义结构**可用于符合条款的翻译与转换；
- OpenALG/Manifold等出版社/平台的站点CSS、JS、字体文件、导航组件、商标、特定图像等，不因正文开放就自动取得可复制/可商用授权；
- 可用一套**自己设计/合法取得许可的极简通用模板**展示三本书与各locale，不需要复制原站代码或每本重新设计一个网站；
- 是否重用网页HTML需要剔除原站导航、注册、登录、评论、动态脚本和未获授权素材，并区分第三方内容权利；
- 如果源网页正文排版出错、章节不完整或依赖动态脚本，就优先采用XML、EPUB、Word等有结构的等价源，PDF继续作为出版校对证据及退路；
- 这项设计选择不授权启动正式网页开发，也不直接修改go-dev项目代码。

## 二、HIS-A：首、中、末三章的实际连续HTML正文核验

官方关联 OpenALG Manifold出版/阅读入口：
https://alg.manifoldapp.org/projects/world-history

其目录列12章，网页有可直接打开的章节独立URL。

| 来源章节 | 源URL | 实际观察 | 最小门禁 |
| --- | --- | --- | --- |
| 1. Prehistory | https://alg.manifoldapp.org/read/world-history/section/26bcf032-404d-4c85-9f3b-6c0cafa5cc25 | 网页具有完整可读英文正文片段与年代列表、章节内部标题、注脚、引用、地图图注等 | `PASS_HTML_BODY` |
| 6. The Roman World from 753 BCE to 500 CE | https://alg.manifoldapp.org/read/world-history/section/4d7ec664-d071-461c-a731-5cfce715d00b | 网页直接呈现罗马历史章节正文，含年代、问题、术语、插图署名（如图6.1注明CC BY-SA 3.0） | `PASS_HTML_BODY` |
| 12. Western Europe and Byzantium circa 1000–1500 CE | https://alg.manifoldapp.org/read/world-history/section/9064f59c-5d0d-447d-a52f-722553a8cc15 | 网页有实质章节正文与长篇结构，并非只有目录/书目信息 | `PASS_HTML_BODY` |

**限制**：这里的PASS表示各抽样页实质连续正文可读、结构存在；不是验证全文与官方PDF逐字符一致、网页图片授权全部审完、12/12章都逐章复核，或HTML字节已冻结。

OpenALG阅读界面另有字体、明暗主题和Margins等外观设置。可借鉴其读者任务，但不能直接套用其CSS/JS代码。

`HIS_A_CHAPTER_SAMPLES=3`
`HIS_A_SAMPLED_FULLTEXT_HTML=3_OF_3`
`HIS_A_ALL_CHAPTER_HTML_COMPLETENESS=UNKNOWN`
`HIS_A_SAMPLED_STRUCTURES=HEADINGS,CHRONOLOGY,FOOTNOTES,READING_QUESTIONS,KEY_TERMS,CAPTIONS`
`HIS_A_PREFERRED_WEB_SOURCE=YES`

## 三、HIS-C：出版目录HTML与可取得HTML全文仍非同一回事

出版社正式书目：
https://www.openbookpublishers.com/books/10.11647/obp.0074

出版社明确列：
- HTML ISBN 978-1-80064-498-4
- XML ISBN 978-1-78374-778-8
- EPUB ISBN 978-1-78374-025-3

但其当前章节入口：
https://www.openbookpublishers.com/books/10.11647/obp.0074/chapters/10.11647/obp.0074.01

当前可直接读取的网页只有章节标题、DOI、作者和“Read Online / Download”等元数据，**没有完整的章节连续正文**。不能因此将HIS-C标记为HTML网页原稿已取得。

本轮新增重要发现：

加拿大公益高等教育开放教材机构BCcampus的开放教材目录存在该书对应条目：
https://collection.bccampus.ca/textbook/VfeV7FDQ/

BCcampus列出：
- 在线阅读：指向Open Book Publishers；
- PDF（约27.62MB）；
- **XML格式（约17.94MB）**，实际链接指向机构CDN下`Ringmar_History_of_International_Relations_xml_369715013b.zip`。

其目录列作者Erik Ringmar、出版社Open Book Publishers、2019、CC BY 4.0（有特别声明的个别素材除外）。

**严格保留证据等级**：
- 该XML是第三方教育机构提供的**已登记格式和下载入口**，不是已下载成功的出版方原始XML。
- 当前浏览器抓取工具尝试该链接得到HTTP403，**不代表用户浏览器一定无法下载**；不能称XML正文结构已核实。
- 该XML或许是重要低成本后备来源，但须在以后核验真实文件、章节点、2019出版版次、出版社PDF内容对应及第三方素材权利；不能直接认定其与出版社源文件字节一致。

`HIS_C_PUBLISHER_HTML_ISBN=VERIFIED`
`HIS_C_CHAPTER_METADATA_HTML=VERIFIED`
`HIS_C_READABLE_CHAPTER_FULLTEXT_HTML=NOT_VERIFIED`
`HIS_C_BCCAMPUS_XML_ENTRY=VERIFIED`
`HIS_C_XML_BYTES_SHA256=UNKNOWN`
`HIS_C_BCCAMPUS_XML_TOOL_FETCH=HTTP_403`
`HIS_C_BCCAMPUS_EDITION_PARITY=UNKNOWN`

## 四、HIS-B：出版社HTML只有书目，没有逐章正文

原始机构页面：
https://dc.etsu.edu/etsu-oer/13/

- 当前页面有书名、作者、CC BY 4.0声明、出版建议引文和可下载PDF入口（约150.9MB）。
- 页面本身**没有15章逐章连续正文**；“viewed online”可以指PDF查看器，不应凭网页可以打开就推断内容是HTML。
- 没有核实可编辑Word、XML、EPUB或逐章HTML正式来源，仍`NOT_FOUND_IN_SAMPLE`。
- 官方PDF curl HTTP403，先前来源恢复调查已降级为备选，不用重复盲试；仍可继续寻找其他大学正式镜像或上游可编辑资源。

`HIS_B_PUBLISHER_METADATA_HTML=VERIFIED`
`HIS_B_TRUE_CHAPTER_FULLTEXT_HTML=NOT_FOUND_IN_SAMPLE`
`HIS_B_STRUCTURED_EDITABLE_SOURCE=UNKNOWN`
`HIS_B_OFFICIAL_PDF_CURL=HTTP_403`

## 五、阅读界面设计最低成本边界

**规划顺序，尚不开发：**

1. 用原著确有商业授权的文本与标题等结构作为内容数据来源；保留脚注、表格、来源和权限元信息，依当前来源差异建立单次可复用的基础阅读格式。
2. 用**一套适用于三本书的合法、自有或适当许可的网页阅读模板**，先控制几项可观察的样式：正文最大宽度、字号/行高、标题层级、目录显示、图片及表格适配、移动端、双向文字和RTL。
3. 可提供“舒适宽度 / 宽屏阅读”等选项；“全屏”不表示必须占满全部显示器宽度，过长行宽可能降低阅读体验。
4. 只有在具体原网页结构影响到脚注、表格、图片、历史年代准确展示或移动端阅读且不能用少量样式修正时，才投入页面重做。
5. 不以复制出版社网页CSS/JS作为实现捷径；不为多个教材建立相互独立的UI工程。

本阶段没有对具体浏览器的原站渲染做像素级定量测量，亦没有正式读者测试；`READER_UX_QUANTITATIVE_EVIDENCE=UNKNOWN`。

## 六、后续唯一有价值的小步骤

`NEXT=HIS_C_XML_FILE_PROVENANCE_AND_DOWNLOAD_GATE`

先只做**HIS-C的BCcampus XML下载来源与真实文件获取可行性小样本调查**：
- 校验是否可直接以用户本地浏览器取得；
- 若可取得，记录大小/sha256、XML文本章节个数、作者与版次是否与出版方2019原书一致；
- 注意CDN返回的`.zip`不等于直接可解析`.xml`，应先看压缩包安全及结构；
- 不下载全网媒体、不翻译、不创建页面；
- 若持续403，保留`BLOCKED`并回到出版社原始HTML/EPUB或PDF方案，不为了第三方镜像建立复杂抓取器。

同时保留HIS-B后备源调查，但不与C并行开展大规模任务。

## 七、汇总

`RESULT=PASS`
`STAGE=HIS_HTML_CHAPTER_CONTENT_AND_SOURCE_ACCESS_MINIMAL_GATE`
`SECOND_PROJECT=WORLD_HISTORY`
`PUBLISHED_FORMAT=WEB_ONLY`
`PROJECT_DOMAIN_SLUG=world-history`
`GO_DEV_LOCALE_PREFIX=EXACT`
`HIS_A_HTML_SAMPLE=3_OF_3_PASS`
`HIS_A_ALL_12_CHAPTERS_AUDITED=NO`
`HIS_B_HTML_SOURCE=NOT_FOUND_IN_SAMPLE`
`HIS_C_HTML_FULLTEXT=NOT_VERIFIED`
`HIS_C_BCCAMPUS_XML_DOWNLOAD_LINK=VERIFIED`
`HIS_C_XML_BYTES=UNKNOWN`
`STYLE_POLICY=MINIMAL_ADJUSTMENT_FIRST_REDESIGN_ONLY_IF_NEEDED`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_C_XML_FILE_PROVENANCE_AND_DOWNLOAD_GATE`
