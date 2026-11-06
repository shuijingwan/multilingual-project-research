# 世界历史：HIS-C EPUB正文一致性抽检通过与 HIS-B 完整源获取优先

日期：2026-11-06
阶段：HIS_C_EPUB_CONTENT_QUALITY_AND_EDITION_PARITY
项目：WORLD_HISTORY（第二项目正式选定）
状态：RESEARCH_ONLY
目标发布：WEB_ONLY
域名命名：world-history，locale严格沿用go-dev正式生产映射

## 一、HIS-C的本地可复验证据

负责人本地报告（2026-11-06）：
- `EPUB_SHA256=50086b5d0e76623409096dcf5db247c4850b4bddcd05ba288187f5e24e2ac9bd`
- `XHTML_FILES=218`
- `EXTRACTED_ENGLISH_WORDS=97807`
- `CHAPTER_TITLE_SIGNALS=8/8`
- `PDF_ENGLISH_WORDS=95596`
- `EPUB_PDF_8_WORD_MATCHES=180/195`
- `EDITION_PARITY=SAMPLING_ONLY`
- `CONTENT_REVIEW=PASS`

文件来源：
- HIS-C EPUB：Internet Archive / Open Library下载备选，`/tmp/mpr-his-c-epub-eDrnN6s1/HIS-C.epub`
- HIS-C出版方PDF：Open Book Publishers，`/tmp/mpr-his-pdf-Ny7smHlP/retry-1laUerGI/HIS-C.pdf`，SHA256 `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`
- 本轮检查日志：`/tmp/mpr-his-c-quality-MQiN7Cax/full.log`

结果解释：
1. 本地EPUB结构和可提取英文文本质量具积极证据，原著8个章节标题信号已出现。
2. 180/195约92.3%的八词片段能匹配出版方PDF，提示很高的文本重合；不能据此证明全文无缺章、全部段落一一对应、内容不是OCR、版次完全同一或媒体具有商用许可证。
3. `PDF_ENGLISH_WORDS=95596`与`EPUB_ENGLISH_WORDS=97807`存在差异，可能是页眉、目录、格式/文本提取差异或内容差异，当前证据不能判明。
4. 该结构化EPUB原则上可转换为网页HTML/XHTML，但正式发布前仍需要章节级质量审查以及作者/版权/媒体分项核对。

`HIS_C_EPUB_DOWNLOAD_AND_SHA=VERIFIED`
`HIS_C_EPUB_XHTML_STRUCTURED_TEXT=VERIFIED`
`HIS_C_CHAPTER_SIGNALS=8_OF_8`
`HIS_C_TEXT_PARITY=HIGH_SAMPLE_OVERLAP`
`HIS_C_EXACT_FULL_BOOK_PARITY=UNKNOWN`
`HIS_C_MEDIA_RIGHTS_FULL_AUDIT=NO`

## 二、三本书完整来源为明确必达目标

负责人明确要求三本教材**都取得合法、完整、可追溯的文本内容源**，不能因为HIS-B官方入口curl HTTP403而放弃该书。

当前：
- HIS-A：出版社PDF已取得、首中末3章HTML正文可访问，剩余全章与版次对应待后续验证。
- HIS-B：ETSU官方PDF curl HTTP403，**尚未取得本地可核验完整源文件**。本阶段是最高优先待办。
- HIS-C：出版社PDF及Open Library EPUB都已取得，结构及文本重合抽样通过，逐章完全一致尚待审核。

不要求三书使用相同源格式：正式输出只提供网页；可优先完整HTML，随后XML/EPUB/Word，必要时用PDF转换成HTML结构，避免人为删除选定教材。

## 三、HIS-B来源证据：官方权利基准与一个直接PDF候选

权威出版页（2026-11-06复核）：
https://dc.etsu.edu/etsu-oer/13/

该页明确：
- 原著 `World History Since 1500: An Open and Free Textbook`
- `John Rankin`、`Constanze Weise`
- 官方推荐书目信息：`2022`
- `15`章
- 作品正文在原出版页标注`CC BY 4.0`（不自动涵盖第三方图片/地图）。
- PDF下载当前维护者网络HTTP403。

公开第三方候选：
https://www.maktaba.org/download/file/2008/World_history_since_1500_John_rankin_constanze_weise.pdf

搜索结果可读到类似原始2022出版版权页与ETSU来源，但本轮访问此链接可能超时或出现网站维护页面，**尚未实际验证文件字节和全文完整性**。并非ETSU出版社的权威下载地址，也不能把其URL当成经过版权和版本校验的最终翻译源。

另有美国University of Minnesota Open Textbook Library书目：
https://open.umn.edu/opentextbooks/textbooks/world-history-since-1500-an-open-and-free-textbook

这里列完整15章标题，但许可/年份标注为2023及CC BY-SA，与ETSU出版方2022/CC BY有所出入；目前不能用该书目替代出版社版权页权威，或将该目录PDF入口当成已验证的独立下载镜像。

## 四、唯一下一步：HIS-B候选PDF实际获取与内容门禁

`NEXT=HIS_B_ALTERNATE_PDF_LOCAL_DOWNLOAD_AND_TEXT_GATE`

由维护者本地终端单次尝试Maktaba公开候选；如果下载成功：
1. 记录实际HTTP返回、最终URL、实际PDF magic、文件大小和SHA256。
2. 使用`pdfinfo`检查真实页数（如工具有提供）；使用`pdftotext`检查标题作者和英文字符量。
3. 检查原书目录和`Chapter 1`至`Chapter 15`的**标题信号**，但目录出现15章不等于每章完整正文；不得宣称CONTENT_COMPLETE=YES。
4. 若下载返回HTML维护页、404、403、超时、不可解析PDF，标记`FAILED`保留日志；继续寻找合法渠道或联系ETSU作者/图书馆索取结构化原稿，而不是对同一坏URL无限重试。
5. 第三方源如成功，未来还要以ETSU官方2022本和具体版权页对照正文与图像，才能作为正式翻译源。
6. 不重新下载已校验的HIS-A/HIS-C，不下载全书额外图片、不建站、不启动翻译/部署、不修改go-dev。

### 汇总

`RESULT=PASS`
`STAGE=HIS_C_EPUB_CONTENT_QUALITY_AND_EDITION_PARITY`
`SECOND_PROJECT=WORLD_HISTORY`
`ALL_THREE_SOURCE_REQUIRED=YES`
`HIS_C_EPUB_STRUCTURE=PASS`
`HIS_C_EPUB_PDF_EIGHT_WORD_OVERLAP=180_OF_195`
`HIS_C_EXACT_COMPLETENESS=UNKNOWN`
`HIS_B_AUTHORITY=ETSU_2022_CC_BY_4_0`
`HIS_B_FULLTEXT_FILE_OBTAINED=NO`
`HIS_B_ALTERNATE_CANDIDATE=MAKTABA_PDF`
`HIS_B_ALTERNATE_BYTES=UNKNOWN`
`FORMAL_PROJECT_SELECTED=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_B_ALTERNATE_PDF_LOCAL_DOWNLOAD_AND_TEXT_GATE`
