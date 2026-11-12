# HIS-C 官方 XML 与 PDF：八章正文抽样一致性核查 001

核查日期：2026-11-12
阶段：HIS_C_XML_VS_OFFICIAL_PDF_LIMITED_PARITY_READONLY
项目：WORLD_HISTORY
状态：RESEARCH_ONLY

## 一、核查范围与来源身份

仅对已由出版方官方渠道获得的两份现有文件做本地只读核查；不重新下载、翻译、转换整书、复制图片或部署。

- 作品：*History of International Relations: A Non-European Perspective*，Erik Ringmar；出版方 Open Book Publishers。
- 出版方页面：https://www.openbookpublishers.com/books/10.11647/obp.0074
- 官方 XML ZIP：本地 `~/下载/obp.0074.zip`；`SHA256=ef00fa6df2eeffa73f05188e26f07810eb21f1a327bda0875efba94345bb82f0`。
- 官方 PDF：本地 `/tmp/mpr-his-pdf-Ny7smHlP/retry-1laUerGI/HIS-C.pdf`；`SHA256=7f8108b52874dfb07a5e3fd4f41a066e8e5324f9a8d71a5a073ca5364b7a7238`。
- 两份 SHA-256 均在本轮重新计算并与仓库记录的既有证据相符：`2/2 PASS`。临时文件路径仅记录本轮环境，不保证长期存在。

## 二、只读方法

1. 使用 Python `zipfile` 检查官方 ZIP，直接读取 `XML-edition/ch1.xml` 至 `ch8.xml`，使用 `xml.etree.ElementTree` 解析，不解压到仓库或执行档案内部代码。
2. 使用 `pdftotext -nopgbrk` 直接提取官方 PDF 全文到本地进程内存，没有写入提取后的全书文件。
3. 将 XML 元素可见文字（`itertext()`）与 PDF 提取文本转换为小写英文词序列；使用表达式 `[a-z]+(?:'[a-z]+)?` 切词，并统一部分连字符。
4. 每章按词序列中约 16%、22%、28%、34%、40%、46%、52%、58%、64%、70%、76%、82% 的位置各取连续 8 个词，在 PDF 规范化词序列全文中查找是否存在该短语。每章 12 个样本，共 96 个；这是**抽样包含性检查**，不是按章节位置逐段对齐。
5. 不保存或发布书籍正文及第三方媒体。章节编号与正文片段匹配不能证明 XML 与 PDF 完全同版、全段无缺失或全部引文、图表、脚注一致。

## 三、实际核查结果

| XML 章节 | 提取英文词数（本轮切词规则） | 八词片段命中 |
| --- | ---: | ---: |
| ch1 | 4,937 | 12/12 |
| ch2 | 14,876 | 11/12 |
| ch3 | 12,887 | 11/12 |
| ch4 | 13,180 | 12/12 |
| ch5 | 12,175 | 12/12 |
| ch6 | 10,645 | 12/12 |
| ch7 | 12,791 | 12/12 |
| ch8 | 11,969 | 12/12 |
| **合计** | — | **94/96** |

- `OFFICIAL_FILE_HASHES=VERIFIED`：官方 XML ZIP 和 PDF 的本地 SHA-256 均一致。
- `EIGHT_CHAPTER_XML_PRESENCE=VERIFIED`：`ch1.xml` 至 `ch8.xml` 均存在、能解析，并包含实质性文字。
- `SAMPLED_TEXT_OVERLAP=VERIFIED`：八章合计 94/96 个八词片段在官方 PDF 的提取文本中可找到。
- `UNMATCHED_SAMPLES=2`：ch2、ch3 各有 1 个片段未匹配，原因未查明；不能断言是真实原文差异，也不能忽略。
- `EXACT_FULLTEXT_PARITY=UNKNOWN`：未执行逐段、逐章完整对齐。
- `CHAPTER_STRUCTURE_AND_NOTES_FULL_AUDIT=UNKNOWN`：标题层次、表格、脚注和引用的完整迁移仍待验证。
- `MEDIA_RIGHTS_FULL_AUDIT=NO`：原著的正文 CC BY 授权不自动覆盖第三方图片；沿用既有逐项审查和不热链未授权媒体的政策。
- `READY_FOR_BULK_TRANSLATION=NO`：本轮仅完成有限核查，未批准正式翻译工程。

## 四、结论、停止线及后续

结果支持官方 XML 作为 HIS-C 未来结构化内容输入的**有力候选**：它具有可解析的八章正文，并在有限抽样下与官方 PDF 高度重合。但样本匹配率不能外推为 97.9% 的全文正确率或完整性保证。

两处未匹配仍是可追踪的未解决项；未来如正式准备内容，应在真实章节样本上核对其文本提取、表格/注释顺序或版本差异，不为本轮仅两个抽样异常启动大规模转换或复杂工具开发。

本轮只读执行，未修改 go-dev，未创建网站，未启动翻译或 DNS 变更。

```text
RESULT=PASS
STAGE=HIS_C_XML_VS_OFFICIAL_PDF_LIMITED_PARITY_READONLY
OFFICIAL_SOURCE_SHA256=2_OF_2_PASS
XML_CHAPTERS_PRESENT=8_OF_8
EIGHT_WORD_SAMPLE_MATCH=94_OF_96
UNMATCHED_SAMPLES=2
EXACT_FULLTEXT_PARITY=UNKNOWN
MEDIA_RIGHTS_FULL_AUDIT=NO
WORLD_HISTORY_IMPLEMENTATION=NOT_AUTHORIZED
RESEARCH_ONLY=YES
NEXT=HIS_A_OFFICIAL_HTML_12_CHAPTER_COMPLETENESS_GATE
```
