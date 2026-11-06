# 世界历史三本教材：全部取得可用源的负责人要求与HIS-C EPUB阶段性验证

记录/联网核实日期：2026-11-06
阶段：HIS_THREE_SOURCE_COMPLETENESS_AND_C_EPUB_NEXT_GATE
项目状态：RESEARCH_ONLY
项目选择：WORLD_HISTORY（已正式选定）
域名：world-history；locale 与go-dev正式生产前缀一致
发布形式：WEB_ONLY

## 一、负责人要求（覆盖此前“某一源连续失败就长期停查”的宽泛建议）

负责人于2026-11-06明确：**三本已确定的教材必须全部取得可靠、完整、可追溯、适合作为网页翻译输入的内容源**。不能因为某个下载入口反复403，就把该书永久放下；应在成本可控的情况下变更合法获取渠道和格式，必要时联系原出版方。

这是**研究成果完成标准**，不是授权立即启动正式大规模翻译、网页建设、DNS或部署。仍遵守RESEARCH_ONLY及go-dev v2优先。

请区分“持续追求三本书的内容源都取得”与“对同一403链接无限次重试”：前者已成为目标，后者仍需停止线。

本项目使用以下逐书门禁：
- `SOURCE_BYTES_OR_FULLTEXT_ACCESS=YES`：成功获取合法且实际可访问的全文（HTML可按完整章节的正式网站作为输入；文档如EPUB/PDF需要实际下载）。
- `SOURCE_EDITION_PROVENANCE=VERIFIED`：与作者、出版方、许可和目标版本关联，记录入口/时间/哈希。第三方镜像需与出版方原版内容对照，不能自称官方二进制。
- `CONTENT_STRUCTURE_COMPLETE=VERIFIED`：核查预期章节完整、首中末正文存在、结构足以转换为网页，不因文件数多就认为章节完整。
- `MEDIA_RIGHTS_SEPARATELY_FILTERED=YES`：媒体使用许可独立审查，未获授权图片不复制、不热链接规避。
- `READY_FOR_TRANSLATION_INPUT=YES`：四项成立后才可能进入后续正式内容准备；即便达到此状态仍需负责人另行授权开发和翻译。

## 二、目前真实结果

| 教材 | 已有成果 | 尚缺少的验证 |
| --- | --- | --- |
| HIS-A 史前至1500 | UNG出版方PDF下载成功 52,210,563 bytes；sha256 `d034e3b6900a8f533b10760d9796b3b32f5299acda6b7d0b326965a37b469340`；OpenALG Manifold首/中/末三章HTML有真实连续正文 | 全12章网页版完整性、HTML/PDF对照、版本与媒体清单 |
| HIS-B 1500年以来 | ETSU官网书目明确15章、2022年与CC BY4.0；官方PDF自动请求HTTP403 | 尚未取得已核验的完整内容文件；需尝试可靠替代来源、对照出版社身份与章节，或联系ETSU请求可编辑原稿 |
| HIS-C 国际关系史 | 官方出版社PDF 28,279,108 bytes；sha256 `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`；**Open Library EPUB真实下载成功** 7,998,848 bytes，sha256 `50086b5d0e76623409096dcf5db247c4850b4bddcd05ba288187f5e24e2ac9bd` | 该EPUB虽有237压缩成员、1 OPF、218 XHTML/HTML，但须证实有完整正文、至少对应8个核心章节、是否为OCR派生，以及与出版社PDF版本一致性 |

HIS-C该EPUB为用户本地成功证据，目录：
`/tmp/mpr-his-c-epub-eDrnN6s1/HIS-C.epub`
`/tmp/mpr-his-c-epub-eDrnN6s1/structure.txt`

HIS-C PDF可读文件：
`/tmp/mpr-his-pdf-Ny7smHlP/retry-1laUerGI/HIS-C.pdf`
HIS-A PDF：
`/tmp/mpr-his-pdf-Ny7smHlP/HIS-A.pdf`

临时路径仅为维护者机器的证据位置，不保证永久存在。

**218 HTML/XHTML文件不意味着218章**；可能是分页、图表说明或扫描OCR页，需实际正文验证。`HIS_C_EPUB_STRUCTURE=PASS`但`HIS_C_EPUB_CONTENT_COMPLETENESS=UNKNOWN`。

## 三、HIS-B的替代来源：允许研究，但不能偷换权威身份

权威出版方：
https://dc.etsu.edu/etsu-oer/13/

新近公开检索（2026-11-06）结果：
1. Open Textbook Library的书目和15章目录：https://open.umn.edu/opentextbooks/textbooks/world-history-since-1500-an-open-and-free-textbook
2. 该开放教材目录的`PDF`按钮**重定向回ETSU官方站**，因此不是另一份可独立下载的镜像。
3. 第三方Maktaba有直接PDF下载候选：
   https://www.maktaba.org/download/file/2008/World_history_since_1500_John_rankin_constanze_weise.pdf
   PDF检索内容含ETSU原始出版机构、John Rankin/Constanze Weise、2022原始引文；能否由维护者网络实际下载和逐章对照未知。
4. Infobooks亦有该书PDF条目：https://infobooks.org/free-pdf-books/history/world-history/ ，描述约232页/29.03MB；该来源不是ETSU出版方，不能拿它的文件大小当作官版版本身份。

第三方PDF**可以作为合法来源书内容的研究性候选**，但不能把“源PDF上写ETSU”直接当作“已核实与ETSU官方150.9MB文件字节等同”。出版社PDF与第三方PDF文件大小不同也不必然表示正文不同，可能是图片压缩或分页等差异；必须比对版次、15章标题、正文样本、版权页、图片独立授权。

注意Open Textbook Library将该书标注`CC BY-SA`及2023，与ETSU官方`CC BY4.0`和2022不完全一致。**此处优先保留出版方具体版本的许可原文**，不同书目记录不能直接合并授权。

如果第三方版本质量/身份有问题，仍继续查找出版社网页原稿、机构图书馆其它公开档案，或通过ETSU官方开放教育部门索取可编辑原件；不为了避免继续调查而删除HIS-B。

## 四、当前最值得做的一个门禁

`NEXT=HIS_C_EPUB_CONTENT_QUALITY_AND_EDITION_PARITY`

理由：HIS-C EPUB已经在维护者机器，成本低，先确定它是不是完整8章的真正正文；检查是否是逐页OCR、是否存在严重乱码或章节遗漏，和已取得的出版社PDF一致度。

这不会延后HIS-B必须找到内容源的正式要求；只表示本轮只读核对已获得文件，然后继续B。为避免反复空转，下一报告应给HIS-B具体可操作的来源验证步骤。

### 最低验证项
- 检查 EPUB ZIP内的`mimetype`、OPF清单与spine实际排布；
- 将XHTML转换成纯文字做有限片段检查（不执行里面脚本、不批量写入研究仓库），查找8章核心标题、首中末章节实际段落；
- 如果本地有`pdftotext`，与出版社PDF抽样比对具有识别意义的原文句子；无此工具则标记`COMPARISON_UNAVAILABLE`而不是假装完成；
- 形成文件级 evidence、sha和`COMPLETE/PARTIAL/UNKNOWN`判定；
- 不创立新的完整翻译工程，不重新下载2份已有PDF，不复制版权不明图片。

`RESULT=PASS`
`STAGE=HIS_THREE_SOURCE_COMPLETENESS_AND_C_EPUB_NEXT_GATE`
`SECOND_PROJECT=WORLD_HISTORY`
`ALL_THREE_SOURCE_REQUIRED=YES`
`ALL_THREE_READY_FOR_TRANSLATION=NO`
`HIS_A_PDF_SHA256_VERIFIED=YES`
`HIS_C_PDF_SHA256_VERIFIED=YES`
`HIS_C_EPUB_SHA256_VERIFIED=YES`
`HIS_C_EPUB_STRUCTURE=PASS`
`HIS_C_EPUB_TEXT_COMPLETENESS=UNKNOWN`
`HIS_B_SOURCE_OBTAINED=NO`
`HIS_B_SOURCE_ACQUISITION_PRIORITY=ACTIVE`
`RESEARCH_ONLY=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_C_EPUB_CONTENT_QUALITY_AND_EDITION_PARITY`
