# 世界历史三部教材：官方来源身份核对与翻译原稿约束 001

核实日期：2026-11-06
阶段：HIS_THREE_BOOK_OFFICIAL_SOURCE_PROVENANCE_GATE
SECOND_PROJECT=WORLD_HISTORY
PROJECT_DOMAIN_SLUG=world-history
PUBLISHED_FORMAT=WEB_ONLY
RESEARCH_ONLY=YES

## 一、负责人新增强约束

负责人明确：**正式翻译输入文件必须从对应教材原出版社或官方授权发布渠道获得；不以社区镜像、第三方归档副本作为权威源，即使文本相似、结构完整、哈希可靠也不例外。**

如果官方下载无法通过脚本进行，但负责人浏览器可以下载，**优先采用手动官网下载、记录具体URL和SHA256**；不要因curl返回HTTP403就断言文件不可取得，也不要先去下载第三方镜像。

本规则不表示第三方内容必然错误，只是本项目正式翻译的来源可信度硬性约束。研究中的第三方文件仍可用作只读非权威比较，但不得未经与官方原文核对就直接进入翻译输入。

## 二、三本教材已获取PDF来源逐项确认

|ID|出版机构/官方网站|先前真实文件获取路线|SHA256|官方来源结论|
|---|---|---|---|---|
|HIS-A|University of North Georgia Press, `ung.edu`|从官方出版社页面链接的 `web.ung.edu/media/university-press/World%20History%20Textbook-082817.pdf` 经用户本地curl成功下载| `d034e3b6900a8f533b10760d9796b3b32f5299acda6b7d0b326965a37b469340` | `OFFICIAL_PUBLISHER_PDF=VERIFIED`|
|HIS-B|East Tennessee State University Digital Commons, `dc.etsu.edu`|用户使用Firefox打开官方 `dc.etsu.edu/cgi/viewcontent.cgi?article=1012&context=etsu-oer`，手动下载后上传会话，用户本地文件与会话验证哈希一致| `fb20f23c3913fcaef68cc503a171e6debe2954775402e83b923722666721cc3b` | `OFFICIAL_INSTITUTION_PDF=VERIFIED`|
|HIS-C|Open Book Publishers, `www.openbookpublishers.com`|用户之前本地脚本从出版社自有主机 `books.openbookpublishers.com/10.11647/obp.0074.pdf` 下载成功，并在后续只读复核确认sha| `7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238` | `OFFICIAL_PUBLISHER_PDF=VERIFIED`|

对应权威出版社页面（2026-11-06复核）：

- HIS-A https://ung.edu/university-press/books/world-history-cultures-states-societies-to-1500.php
- HIS-A PDF https://web.ung.edu/media/university-press/World%20History%20Textbook-082817.pdf
- HIS-B https://dc.etsu.edu/etsu-oer/13/
- HIS-B PDF https://dc.etsu.edu/cgi/viewcontent.cgi?article=1012&context=etsu-oer
- HIS-C https://www.openbookpublishers.com/books/10.11647/obp.0074
- HIS-C PDF https://books.openbookpublishers.com/10.11647/obp.0074.pdf

上述官方PDF来源判断根据用户前驱真实下载指令、用户本人浏览器截图及下载文件哈希与出版方页面，不是单凭文件标题或CC版权标记推断官方身份。SHA仅提供本地二进制身份，不是出版社官网公布的SHA校验值，亦不意味着所有插图获授权。

## 三、必须纠正：HIS-C EPUB下载自第三方归档

前驱用户本地：
- EPUB 7,998,848 bytes，SHA256 `50086b5d0e76623409096dcf5db247c4850b4bddcd05ba288187f5e24e2ac9bd`；
- 下载URL `https://archive.org/download/b7790cae-1901-446e-b529-b5fe393d8061/b7790cae-1901-446e-b529-b5fe393d8061.epub`；
- 来源为Internet Archive / Open Library而**不是Open Book Publishers**。
- EPUB包含218 XHTML/HTML文件、8/8章名信号，与出版社PDF 180/195八词片段抽样匹配。

即便这些数据支持内容质量，也**不满足负责人最新`TRANSLATION_SOURCE_OFFICIAL_ONLY=YES`规则**。

因此：
- `HIS_C_OPENLIBRARY_EPUB_OFFICIAL=NO`
- `HIS_C_OPENLIBRARY_EPUB_TRANSLATION_AUTHORITY=NO`
- `HIS_C_OPENLIBRARY_EPUB_RESEARCH_COMPARISON_ONLY=YES`
- `HIS_C_PUBLISHER_PDF_TRANSLATION_SOURCE_CANDIDATE=YES`

HIS-C出版社有正式EPUB、XML、HTML格式ISBN，但本研究未实际下载并校验出版社对应EPUB或XML文件：
`HIS_C_OFFICIAL_EPUB_BYTES=UNKNOWN`
`HIS_C_OFFICIAL_XML_BYTES=UNKNOWN`

**官方手动获取入口**：
https://www.openbookpublishers.com/books/10.11647/obp.0074

网站提供Download入口；如果用户希望减少PDF转HTML成本，可先尝试在此官方页面下载EPUB/XML，记录最终URL、文件字节、SHA256和具体版本。**不要猜测尚未验证的直链文件名**。若该格式无法从官方取得，则现有官方PDF仍可作为正式源候选，最终通过可追溯转换提取结构。

HIS-A的官方关联OpenALG/Manifold网页正文3章抽检通过；正式使用时仍需将具体网页内容对应到官方出版版本，不能把网站模板CSS/JS、商标和第三方图像等同于CC正文许可。HIS-B只有官方PDF已取得，暂未取得官方HTML全文。

## 四、未来三书源内容可用性真正门禁

- `OFFICIAL_ORIGIN=YES`：来自确证的出版机构/出版社官方提供的具体内容源；归档版本需有出版社明确官方指向/授权渠道证据，不因“大学/非营利”自动当官方。
- `BYTE_IDENTITY=YES`：本地原件文件大小和SHA256；对网页抓取则来源URL、获取时间、内容摘要和版本关联。
- `TEXT_STRUCTURE_INTEGRITY=PASS`：章节与正文结构完整，可可靠转换为目标HTML；可使用PDF作为输入但需核查双栏阅读顺序。
- `MEDIA_LICENSE_AUDIT=PER_ITEM`：逐素材许可，不把正文CC许可证自动用于图库素材；未获商用授权的图片不复制、不热链接规避。
- `TRANSLATION_LAUNCH_AUTHORIZED=NO`：研究结束不自动产生开工授权，go-dev v2仍优先。

### 目前结果与下一步

`RESULT=PASS`
`STAGE=HIS_THREE_BOOK_OFFICIAL_SOURCE_PROVENANCE_GATE`
`SECOND_PROJECT=WORLD_HISTORY`
`ALL_THREE_OFFICIAL_PDFS_OBTAINED=YES`
`OFFICIAL_PDF_SHA256_VERIFIED=3_OF_3`
`TRANSLATION_SOURCE_OFFICIAL_ONLY=YES`
`HIS_C_ARCHIVE_ORG_EPUB_TRANSLATION_AUTHORITY=NO`
`HIS_C_OFFICIAL_EPUB_OR_XML=NOT_YET_OBTAINED`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`RESEARCH_ONLY=YES`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_C_OFFICIAL_EPUB_OR_XML_OPTIONAL_ACQUISITION`

**后续最省力的一步**：负责人如想利用EPUB/XML减少网页转换工作，可使用Open Book Publishers官方Download入口手动取得格式并校验；这属于对已存在**官方PDF**的补充优化，而不是三书官方原著仍缺失。
