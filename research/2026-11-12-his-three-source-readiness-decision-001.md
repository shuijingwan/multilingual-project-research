# 世界历史三本教材：翻译源就绪性阶段决策

核查日期：2026-11-12

阶段：HIS_THREE_SOURCE_READINESS_DECISION

项目：WORLD_HISTORY

状态：RESEARCH_ONLY

## 一、研究目标

判断三本已选定教材是否具备合法、可靠、
可追溯且适合进一步结构化转换的原始翻译来源。

本报告区分原始来源可用性与正式翻译输入就绪性。
不批准大规模翻译、建站、DNS或部署。

## 二、逐书结论

### HIS-A：1500年以前世界史

- 官方出版社 PDF 已取得并验证 SHA-256。
- 官方关联 HTML 阅读版：12/12章通过基本访问与结构检查。
- HTML/PDF：134/144个八词片段匹配。
- 第8章存在少量未匹配片段。
- 正文授权基础：CC BY-SA 4.0，存在第三方素材例外。

结论：官方 HTML 可作为优先翻译源候选，
官方 PDF 作为版本与内容对照来源。

尚未证明全部HTML正文与PDF逐段一致。

### HIS-B：1500年以来世界史

- ETSU 官方 PDF 已取得并验证 SHA-256。
- 15/15章具备可提取正文。
- PyMuPDF4LLM 已生成15章Markdown研究候选。
- 13/15章通过既定页面文本重合度门槛。
- 第3、4章部分页面需复核。
- 已针对异常页35、38、54进行视觉检查，
  发现地图文字和复杂布局是重要差异来源。
- 15章发现11个已配对的图中文字块，
  涉及10页；不成对标记为0。
- 正文授权基础：CC BY 4.0，仅涵盖获该许可的原创内容。

结论：官方 PDF + PyMuPDF4LLM
可作为后续结构化翻译源的有条件候选。

尚未证明所有标题、脚注、表格、图片文字
均能正确分离与转换。
11个图中文字块不代表全书图片总数。

### HIS-C：国际关系史

- 出版社官方 XML ZIP 已取得并验证 SHA-256。
- 8/8章 XML 均存在且包含正文。
- 官方XML/PDF八词片段抽样：94/96匹配。
- 两个未匹配片段的原因仍未确定。
- 正文授权基础：CC BY 4.0，第三方媒体除外。

结论：官方 XML 可作为优先翻译源候选。
官方 PDF 作为版本与内容对照来源。

尚未证明全文、脚注、图表与XML/PDF完全一致。

## 三、统一决策

OFFICIAL_SOURCE_ORIGIN=VERIFIED_3_OF_3

SOURCE_FILE_BASIC_CHECK=PASS_3_OF_3

TRANSLATION_SOURCE_CANDIDATES=3_OF_3

SOURCE_REPLACEMENT_REQUIRED=NO_CURRENT_EVIDENCE

FULL_SEMANTIC_INTEGRITY=UNKNOWN

MEDIA_RIGHTS_FULL_AUDIT=NOT_DONE

BULK_TRANSLATION_AUTHORIZED=NO

目前三本教材均已有足够依据保留官方原始文件，
没有证据要求必须重新寻找替代来源。

但这不等于三本教材已经获得最终翻译输入批准。

## 四、未来正式准备时的停止线

1. 不能把图中文字线性提取结果当作普通正文。
2. 不能因正文CC许可推定全部图片可商业使用。
3. 章节、标题、脚注和表格需保留必要语义结构。
4. 若出现重大转换缺陷，再寻找官方替代格式。
5. 正式翻译与开发仍需要独立授权。
6. 不为少量排版差异无限开发转换工具。

## 五、现有研究证据

- research/2026-11-12-his-a-official-html-12-chapter-access-gate-001.md
- research/2026-11-12-his-a-html-pdf-sample-parity-001.md
- research/2026-11-12-his-c-official-xml-pdf-limited-parity-001.md
- HIS-B本地转换日志与图中文字边界核查日志。
- 既有三本教材官方来源、许可证及媒体审查报告。

本地 /tmp 日志为临时证据，不保证长期存在。
原始PDF/XML及大规模转换内容不提交公开仓库。

## 六、最终状态

RESULT=PASS

STAGE=HIS_THREE_SOURCE_READINESS_DECISION

DECISION=OFFICIAL_SOURCES_CONDITIONALLY_SUITABLE

THREE_SOURCE_FILES_REPLACEMENT=NOT_REQUIRED_NOW

WORLD_HISTORY_IMPLEMENTATION=NOT_AUTHORIZED

GO_DEV_MUTATION=NONE

RESEARCH_ONLY=YES
