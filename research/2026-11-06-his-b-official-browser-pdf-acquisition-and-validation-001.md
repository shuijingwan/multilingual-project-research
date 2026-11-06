# HIS-B：官方浏览器下载成功、完整PDF取得与SHA核验 001

核实日期：2026-11-06
阶段：HIS_B_OFFICIAL_BROWSER_PDF_ACQUISITION_AND_VALIDATION
正式第二项目：WORLD_HISTORY
发布目标：WEB_ONLY
当前状态：RESEARCH_ONLY
文件来源：项目负责人通过Firefox访问东田纳西州立大学ETSU Digital Commons官方网页并手动下载，随后上传至研究会话供文件级核验

## 一、纠正既往403误判

此前用`curl`请求ETSU官方PDF：
https://dc.etsu.edu/cgi/viewcontent.cgi?article=1012&context=etsu-oer

维护者命令行返回`HTTP 403`。该状态只能证明**特定非浏览器HTTP请求被拒绝**，无法证明官方PDF不可取得、版权失效、网站禁止所有下载、应转向第三方镜像。不能未经服务器日志就指定根因（Referer、Cookie、防机器人、WAF或其他策略均未证实）。

负责人2026-11-06提供两张浏览器截图：
- ETSU官方书目页面 `https://dc.etsu.edu/etsu-oer/13/`，PDF下载入口显示“Download Full Text (150.9 MB)”；
- Firefox在相同ETSU域名的`cgi/viewcontent.cgi?article=1012&context=etsu-oer`中打开了实际PDF的封面；
- 负责人声明已经从官方站点下载成功，本地“下载”目录中有`World History Since 1500_ An Open and Free Textbook.pdf`，并将PDF文件上传到本研究会话。

**正式纠正**：`HIS_B_OFFICIAL_SOURCE_OBTAINED=YES`，`HIS_B_THIRD_PARTY_FALLBACK_REQUIRED=NO`。此前报告中`HIS_B_FULLTEXT_FILE_OBTAINED=NO`仅为过去时间点的真实状态，已被本报告替代。

## 二、上传文件经直接字节/元数据/文本检查

附件实际文件：`World History Since 1500_ An Open and Free Textbook.pdf`，经当前分析容器对附件的**实际完整字节**执行SHA-256、`pdfinfo`、PyMuPDF章节起始页抽查。

- `FILE_BYTES=158213579`
- `SHA256=fb20f23c3913fcaef68cc503a171e6debe2954775402e83b923722666721cc3b`
- `PDF_PAGE_COUNT=233`
- `PDF_VERSION=1.7`
- `PDF_TITLE=World History Since 1500: An Open and Free Textbook`
- `PDF_AUTHOR=John Rankin and Constanze Weise`
- `PDF_CREATOR=Appligent AppendPDF Pro 6.3`
- `PDF_PRODUCER=Prince 15.4.1 (www.princexml.com)`
- `PDF_METADATA_CREATION_DATE=2025-09-23T08:31:52-07:00`
- `PUBLISHER_CITATION_YEAR=2022`
- `PDF_LAST_PAGE=BLANK`
- `PDF_TEXT_EXTRACTION=SAMPLE_PASS`
- `CHAPTER_START_PAGES=15_OF_15_VERIFIED`

经目录定位后的**正式PDF页号**（不是书中章节内印刷页码）：
`CH1=8;CH2=22;CH3=34;CH4=46;CH5=58;CH6=66;CH7=85;CH8=100;CH9=120;CH10=132;CH11=147;CH12=162;CH13=178;CH14=188;CH15=214`。

这些页均含可提取的实际章节正文，且末尾仍有第15章文本；最后第233页为空白。**目录存在、15/15起始页及末章文本存在**为实质完整性的积极证据，但不是逐字符全书校验；图片版权分项审查也尚未完成。

官方书目显示150.9MB，其对应字节与本文件的158,213,579bytes约150.9MiB一致。这是文件容量的相互支持信号，**不是官网服务器独立发布的SHA校验值**。

## 三、版权与出版年份须严格分层

上传PDF前言：
- 书中推荐引用为Rankin / Weise，2022，East Tennessee State University；
- PDF的正文版权声明为`Creative Commons Attribution 4.0 International (CC BY 4.0)`；
- 权利说明明确：CC BY 4.0仅覆盖本书原创内容；绝大多数图片来自外部，逐图另列来源/许可；为教材制作的原创地图属于特别标注的原始内容；
- 具体示例：章节中有`iStock Standard License (purchased by ETSU)`，不能推定本站享有同一商用使用权；同时有`CC BY-SA`地图及`CC BY 4.0 | © ETSU`原创地图，可在独立证据核验后按各自许可证合规复用。

**出版年份2022与当前附件PDF元数据创建日期2025-09-23同时成立，并不代表已确认2025年内容修订。** 本轮没有取得出版社的版本历史或变更日志，故`EXACT_EDITION_CHANGE_HISTORY=UNKNOWN`。不得简单标记“这是2022年原始二进制”或“2025修订版”。冻结的是**此文件的实际SHA256字节身份**。

重要：PDF中的署名/许可证标记只是具体素材审计的候选证据，转载前应确认具体原图文件与改编条件；不以热链接规避未授权图片。

## 四、正式源文件获取顺序调整

负责人明确：世界历史三本教材都必须取得**合法、完整、可追溯**内容源；个人最终站点只提供网页形式，优先HTML，但并不排除PDF后备。

**新优先级：**

1. 首先查**出版社/官方机构真正的完整网页正文**，如HIS-A的OpenALG Manifold。
2. 有官方Word/XML/EPUB等结构化正式原稿时可优先。
3. 若官方只提供可下载PDF，`curl`失败但用户浏览器能下载，则**优先使用负责人浏览器下载的官方PDF**；必要时辅以用户提供的本地文件SHA验证，不继续消耗大量研究时间尝试改变403。
4. 只有官方可访问路径均不可行时，才启用第三方镜像作为研究后备；必须验证出版社身份、内容与权利，不得伪称“官方源”。

该顺序不授权复制出版社整页HTML/CSS/JS/商标，也不改变当前`LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`的图片许可界限。

## 五、三书现阶段内容源汇总

| 来源 | 已实际取得 | 仍待证明 |
|---|---|---|
| HIS-A | 出版方PDF，SHA `d034e3b6900a8f533b10760d9796b3b32f5299acda6b7d0b326965a37b469340`；首中末3章官方关联HTML正文可读 | 12/12章完整性、HTML对应版次及图片白名单 |
| HIS-B | **ETSU官方浏览器下载PDF，SHA `fb20f23c3913fcaef68cc503a171e6debe2954775402e83b923722666721cc3b`，15章起始正文抽查PASS** | HTML/可编辑源是否存在、正式网页转换的章节与图文分离质量；原版更新历史 |
| HIS-C | 出版社PDF，SHA `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`；Open Library EPUB，SHA `50086b5d0e76623409096dcf5db247c4850b4bddcd05ba288187f5e24e2ac9bd`，8/8标题信号、180/195八词抽样匹配PDF | EPUB逐章完全一致性及具体媒体授权 |

`ALL_THREE_BOOKS_FULL_TEXT_SOURCE_OBTAINED=YES`应解释为**三本书均已有可提取完整内容的实质性来源文件/可访问章节正文**。不得扩大为`ALL_THREE_READY_FOR_TRANSLATION=YES`，因为逐章完整性、来源格式质量和媒体授权仍需后续核实。

## 六、唯一下一步

`NEXT=HIS_B_LOCAL_OFFICIAL_PDF_IDENTITY_CONFIRMATION`

研究负责人在其真实本地计算机上对`~/下载/World History Since 1500_ An Open and Free Textbook.pdf`计算SHA-256，与上述上传附件SHA进行比对，并核实文件未改变；随后才能把这份PDF作为确定的HIS-B文件级源身份锁定（不需要再次上传150MB）。

如果文件名或下载文件夹不同，则记录实际路径而非瞎猜。该操作只读，不复制大PDF到公开Git仓库。

下一轮再规划三本书网页内容提取/章节完整度**小样本**，不提前启动批量翻译或建站。

## 七、正式状态

`RESULT=PASS`
`STAGE=HIS_B_OFFICIAL_BROWSER_PDF_ACQUISITION_AND_VALIDATION`
`SECOND_PROJECT=WORLD_HISTORY`
`SOURCE_BOOKS=3`
`HIS_B_OFFICIAL_BROWSER_DOWNLOAD=VERIFIED_BY_USER_SCREENSHOTS`
`HIS_B_UPLOADED_FILE_SHA256=fb20f23c3913fcaef68cc503a171e6debe2954775402e83b923722666721cc3b`
`HIS_B_UPLOADED_FILE_BYTES=158213579`
`HIS_B_PDF_PAGES=233`
`HIS_B_CHAPTER_STARTS=15_OF_15_PASS`
`HIS_B_EXACT_2022_BINARY_VERSION=UNCLEAR`
`HIS_B_CONTENT_SOURCE_OBTAINED=YES`
`HIS_B_PDF_SOURCE_FORMAT=PDF_BACKUP`
`ALL_THREE_BOOKS_CONTENT_SOURCE_OBTAINED=YES`
`ALL_THREE_READY_FOR_TRANSLATION=NO`
`OFFICIAL_BROWSER_MANUAL_DOWNLOAD_FALLBACK=ACCEPTED`
`THIRD_PARTY_PDF_REQUIRED_FOR_HIS_B=NO`
`PUBLISHED_FORMAT=WEB_ONLY`
`RESEARCH_ONLY=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_B_LOCAL_OFFICIAL_PDF_IDENTITY_CONFIRMATION`

官方核实URL（2026-11-06）：
https://dc.etsu.edu/etsu-oer/13/
https://dc.etsu.edu/cgi/viewcontent.cgi?article=1012&context=etsu-oer
