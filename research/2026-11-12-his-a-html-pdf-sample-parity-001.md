# HIS-A 官方 HTML 与 PDF 正文抽样一致性核查

日期：2026-11-12

STAGE=HIS_A_HTML_PDF_CHAPTER_SAMPLE_PARITY_GATE

## 一、研究范围

针对已通过可访问性检查的 HIS-A 官方关联 HTML
十二章，与官方出版方 PDF 进行有限正文抽样对照。

原书：World History: Cultures, States, and Societies to 1500

出版社：University of North Georgia Press

不修改原文，不翻译，不复制图片，不建设网站。

## 二、十二章检查结果

| 章节 | HTML提取词数 | 八词片段匹配 | 状态 |
| --- | ---: | ---: | --- |
| 01 | 7458 | 12/12 | PASS |
| 02 | 16369 | 11/12 | PASS |
| 03 | 19188 | 12/12 | PASS |
| 04 | 21708 | 12/12 | PASS |
| 05 | 16826 | 11/12 | PASS |
| 06 | 19756 | 11/12 | PASS |
| 07 | 12067 | 12/12 | PASS |
| 08 | 14004 | 9/12 | REVIEW |
| 09 | 12944 | 11/12 | PASS |
| 10 | 12226 | 11/12 | PASS |
| 11 | 10764 | 12/12 | PASS |
| 12 | 18941 | 10/12 | PASS |

CHAPTERS_PASS=11/12

EIGHT_WORD_SAMPLE_MATCH=134/144

RESULT=PARTIAL

## 三、第八章诊断

第八章共有三个完整八词片段未匹配。

| 位置 | 最长连续短片段匹配 |
| --- | --- |
| 18% | 5/8 |
| 24% | 6/8 |
| 66% | 5/8 |

短片段匹配说明存在局部文本重合，
但不能证明完整原文一致。

可能存在文本提取、排版或版本差异，
具体原因尚未确定。

CH08_ROOT_CAUSE=UNDETERMINED

## 四、证据等级与限制

- VERIFIED：十二章 HTML 已通过此前可访问性检查。
- VERIFIED：本轮 134/144 个八词片段匹配。
- VERIFIED：官方 PDF SHA-256 检查通过。
- UNKNOWN：HTML/PDF 全文逐段一致性。
- UNKNOWN：第八章三个未匹配片段的实际原因。
- UNKNOWN：全书第三方媒体的商业使用授权状态。

抽样结果不能证明全书正文完整一致，
也不能直接换算成全文准确率。

## 五、研究决定

当前不继续为少量未匹配片段开展高成本排查。

保留 HIS-A 官方 HTML 作为未来结构化内容输入候选，
正式使用前仍需执行必要的章节结构、
版权及版本一致性审核。

本轮不批准翻译、开发、部署或 DNS 修改。

RESEARCH_ONLY=YES

PROJECT_LAUNCH_AUTHORIZED=NO

GO_DEV_MUTATION=NONE

NEXT=HIS_B_OFFICIAL_PDF_STRUCTURE_READINESS_GATE
