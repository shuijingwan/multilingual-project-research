# HIS-C：BCcampus XML压缩包来源与可获取性门禁 001

核实日期：2026-11-06
阶段：HIS_C_XML_FILE_PROVENANCE_AND_DOWNLOAD_GATE
研究状态：RESEARCH_ONLY
正式第二项目：WORLD_HISTORY
网页发布格式：WEB_ONLY
原始输入倾向：OFFICIAL_FULLTEXT_HTML_FIRST；XML/EPUB作为结构化备选

## 一、可核实的原始出版元数据

Open Book Publishers出版社书目：https://www.openbookpublishers.com/books/10.11647/obp.0074

- 书名：History of International Relations: A Non-European Perspective
- 作者：Erik Ringmar
- 出版：2019-07-31
- DOI：10.11647/OBP.0074
- 出版社列出的XML ISBN：978-1-78374-778-8
- 出版社列出的PDF ISBN：978-1-78374-024-6
- 正文CC BY 4.0，另有第三方图像许可例外

状态：
`PUBLISHER_XML_FORMAT_LISTED=VERIFIED`
`PUBLISHER_XML_BYTES_OBTAINED=NO`

出版格式的ISBN只能确定某种版本的存在，**不是该格式文件已经下载或XML可供翻译的证明**。

## 二、BCcampus为同一本书提供独立的XML下载项

BCcampus（加拿大教育开放资源机构）条目：
https://collection.bccampus.ca/textbook/VfeV7FDQ/

网站显示：
- 书名和作者、Open Book Publishers、2019年出版信息；
- 许可标注 CC BY 4.0（另有例外）；
- PDF下载项约27.62MB；
- **XML下载项约17.94MB**；
- 用户点击XML下载指向机构CDN，而不是出版社网站。

本轮从BCcampus链接直接解析到确切链接：

https://cdn2.repo.bccws.ca/resources/textbooks/153/formats/Ringmar_History_of_International_Relations_xml_369715013b.zip

**该文件是ZIP压缩包**，不是扩展名为.xml的单一文件；在看到压缩包成员之前，不得推断里面是TEI、JATS、DocBook、Pressbooks结构还是其他XML文件格式。

web浏览访问该CDN资源：**HTTP403**；
本轮试图从受限本地执行环境访问该域名：**DNS解析失败**。

二者是不同执行环境的访问障碍，不能归纳为资源被撤回、下载被明确禁止，也不能证明用户自身网络访问失败。

`BCCAMPUS_XML_LISTING=VERIFIED`
`BCCAMPUS_ZIP_URL=VERIFIED`
`WEB_FETCH_STATUS=HTTP_403`
`EXECUTION_ENV_FETCH_STATUS=DNS_RESOLUTION_FAILED`
`ZIP_BYTES_OBTAINED=NO`
`ZIP_SHA256=UNKNOWN`
`XML_FILES_INSIDE_ZIP=UNKNOWN`
`XML_CHAPTER_COUNT=UNKNOWN`
`TEXT_COMPLETENESS=UNKNOWN`
`EDITION_PARITY_WITH_PUBLISHER_PDF=UNKNOWN`

## 三、数据来源许可与风险界限

- BCcampus目录的许可证元数据和出版社元数据相互支持原著正文的CC BY 4.0基础。
- 需要确认XML中的具体内容来自已核实的2019原书、作者和完整章节，而非不同版本/第三方增补。
- XML中如包含图像链接、内嵌媒体、地图或第三方作品，**不因XML格式或BCcampus托管而自动取得商业重用权**。
- XML压缩包不应提交到公开研究Git仓库；仅将来源链接、压缩包SHA、成员名/大小及少量审查结论记录到evidence。
- 与HIS-C既有PDF SHA `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`对照时，必须比较书名、作者、目录及首中末段落/章节结构，不能拿不同格式的文件SHA进行相等性要求。
- 任何版权不明媒体继续采用普通官方外链/替代/省略原则；不能把热链接当作商业许可。

## 四、下一项唯一低成本尝试

下一步仅由维护者本地终端**尝试下载这一份~18MB BCcampus ZIP**，并验证：
1. HTTP状态、最终URL、文件是否真实ZIP；
2. 精确字节数与SHA-256；
3. 安全列出压缩包成员路径及XML文件数量（不执行压缩包内容，不解压到工作树）；
4. 如下载可用，仅在安全限制下检查XML有无基本作者/标题/8章标记，禁止据此声称完整与PDF一致；
5. 若HTTP403、其他网络错误、非ZIP或损坏，则保留日志及状态；直接停止而不是编写爬虫或增加重试负担。

计划本地证据存放于`/tmp`，不修改go-dev、不创建站点、不批量翻译。

`RESULT=PARTIAL`
`STAGE=HIS_C_XML_FILE_PROVENANCE_AND_DOWNLOAD_GATE`
`SECOND_PROJECT=WORLD_HISTORY`
`PROJECT_DOMAIN_SLUG=world-history`
`BCCAMPUS_XML_DOWNLOAD_LINK=VERIFIED`
`BCCAMPUS_XML_BYTES=UNKNOWN`
`BCCAMPUS_XML_ARCHIVE_MEMBERS=UNKNOWN`
`PUBLISHER_XML_ISBN=978-1-78374-778-8`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_C_XML_LOCAL_DOWNLOAD_AND_STRUCTURE_PROOF`

核实网页日期：2026-11-06。研究仅引用出版方/大学机构的信息，不以网页下载按钮证明文件可用。
