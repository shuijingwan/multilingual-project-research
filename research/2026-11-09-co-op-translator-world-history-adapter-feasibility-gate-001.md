# Co-op Translator × 世界历史：外层适配器可行性门禁 001

- 核实日期：2026-11-09
- 阶段：`CO_OP_TRANSLATOR_WORLD_HISTORY_ADAPTER_FEASIBILITY_GATE`
- 本轮判定：`PARTIAL`（静态证据充分支持优先尝试，尚不能宣称端到端可用）
- 已正式选定的第二项目：`WORLD_HISTORY`（不变）
- 当前执行状态：`RESEARCH_ONLY`
- 维护者偏好：优先使用持续维护的开源翻译框架，在**外层**封装项目专有规则；不直接移植 go-dev 全套基础设施。
- 方法：查阅 Co-op Translator 官方 GitHub 文档及仓库内既有研究记录；**未安装、未运行样本、未调用模型、未 Fork、未修改 go-dev**。

## 1. 问题与本轮结论

**问题**：能否利用 Co-op Translator 的公开 API，作为世界历史项目主要翻译引擎，并通过薄适配层承接教材来源、授权、独立审校及发布要求，而不重建 go-dev 的多层状态体系？

**回答**：`PARTIAL`。

- `VERIFIED`：Co-op Translator 提供明确的公开 `co_op_translator.api`、Markdown 内容级 API、仓库级 API、MCP agent-assisted 接口、术语上下文、相对链接重写与确定性 review。其基本能力与构建“薄适配层”的方向相符。[S1–S3]
- `VERIFIED`：默认仓库翻译按文件级来源哈希判断新旧，过期 Markdown 会整体重译；`TranslationStateProvider` 可由宿主保存已接受的源文/目标基线，以尝试保留未修改 Markdown 块的人工修订，但没有持久化块级断点恢复，并可能在歧义或不合法时回退整文件重译。[S2]
- `VERIFIED`：MCP 的 `start_markdown_agent_translation` 与 `finish_markdown_agent_translation` 支持将分块交给宿主 AI 翻译，Co-op 本身不需要付费模型 API Key；但宿主模型的额度/费用仍需另行考虑。此模式不是完整的仓库级元数据、增量状态及审校自动化。[S3]
- `VERIFIED`：仓库采用 MIT 许可；允许遵循条款使用、修改和再分发**工具源码**，不自动赋予第三方历史教材、图片、外部内容的商业再分发权。[S4]
- `UNKNOWN`：实际世界历史教材正文从官方 HTML、Word、EPUB、XML、PDF 转换为适合 Co-op 的 Markdown 后，其脚注、章节、引用、表格、链接和人工修改在真实运行中是否完整保留。
- `UNKNOWN`：用户既定的 66 个精确 locale 与 Co-op 语言代码逐一映射后的真实缺口、地区用语质量与输出目录支持。
- `UNKNOWN`：与“现成解析库 + 独立文件交接”的同样本对比中，Co-op 是否真正节省维护时间、审校时间或宿主模型额度。

`RESULT=PARTIAL` 是**研究门禁结果**，不是工具部署失败，也不是批准 Fork 或开发。

## 2. 分层边界：复用已有能力，而不是重新建立一套平台

| 层 | 首选责任边界 | 静态证据 / 缺口 |
| --- | --- | --- |
| 教材来源层 | 项目记录出版机构、具体版次、原文哈希、正文/媒体逐项许可证 | 世界历史已有单独来源与授权记录；Co-op 不负责版权筛查 [R3] |
| 输入适配层 | 从合法官方 HTML/Word/EPUB/XML 等来源形成可追溯的章节 Markdown；PDF 保留作校对/必要时回退 | **项目专有，非 Co-op 已解决**；不提前选择单一输入格式 [R3–R5] |
| 翻译引擎层 | 优先使用未修改的公开 Python API 或 MCP agent-assisted 分块与还原 | 公开接口已验证存在，真实可用性未测试 [S2–S3] |
| 轻量工作流层 | 最少的原文哈希、译文哈希、源/目标 locale、候选/接受状态、独立 QC 结论、执行者与日期 | Co-op 可提供部分增量和结构检查；外部仍负责接受与发布批准 |
| 发布层 | 逐语言目录、逐书署名/许可、SEO、每语言既定子域名、关于页翻译进度 | 与翻译引擎分离；不使用 Co-op 路径规则决定域名 [R6] |

建议最小流程：先确认教材来源与素材权利 → 在独立样本中转换为 Markdown → 调用 Co-op 公开接口翻译/还原 → 确定性结构校验 → **独立语义审校** → 人工接受与哈希记录 → 之后才可能由站点构建工具发布。

明确**不预先实现**：go-dev 的 TranslationUnit 全套精确生命周期、多层 authorization epoch、复杂 snapshot/successor 权威恢复、跨项目公共核心仓库、大规模自动同步机制。必要的来源身份、结构保护、独立审核与接受状态仍不可省略。

## 3. 公开 API 与选型条件

### 3.1 内容级 API

`translate_markdown_content` / `rewrite_markdown_paths`：项目自行决定读取源文、输出路径及保存译文；内容级接口**不自动管理**仓库元数据和状态。[S2]

`start_markdown_agent_translation` / `finish_markdown_agent_translation`：便于 ChatGPT、Codex 或其他 MCP 宿主模型承担语言生成，Co-op 负责受保护的 Markdown 分块、重建和结构处理；不得推断 ChatGPT Plus 可无限量或以同样方式调用该工作流。[S2–S3]

### 3.2 仓库级 API

`run_translation`：有干运行计划、`include/exclude`、`context_file`、`groups`、进度事件 `co-op.translation.event.v1`、`TranslationStateProvider` 等能力。其通常由 Co-op 自身使用配置的翻译提供方，**不能误认为仓库级 API 自动支持无 API Key 的宿主 Agent 全量翻译**。[S2]

`run_review`：只读确定性检查，官方标为 Beta；不能取代独立语言质量、历史年代/人名/事实核验，也不能推导独立审核已通过。[S2]

### 3.3 保留人工修订

`TranslationStateProvider` 是最有价值的可复用扩展点。它允许外部存储“已接受原文/译文”基线，记录候选，但**是否接受候选**属于宿主业务规则。对未变更顶层 Markdown 块可复用人工修订；发生歧义时可能整文件重译。它不等于跨文件翻译记忆或 go-dev 的严格审校状态机。[S2]

### 3.4 语言与许可

官方公开语言代码表覆盖 50 多个代码，包括 `zh-CN`、`ja`、`ko`、`de`、`pt-BR` 等，另有暂不支持项。与 go-dev 的 `ja-JP`、`de-DE`、`es-419` 等 66 个 locale **不得直接按字符串相等判断是否支持**；必须建立显式映射、地区变体质量检查及不支持代码处理。[S5][R1]

MIT 仅覆盖工具本身；三本历史教材按对应正文 CC BY / CC BY-SA 与例外分别管理，第三方图片不因处于开放教材中而自动可用。不得为了规避图片授权而内联热链。[S4][R3]

## 4. 世界历史三书的输入边界与风险

- `HIS-A`：已有出版社 PDF 版本哈希和部分官方 HTML 正文，但完整 12 章的正式网页结构/版次对照尚不能在本门禁宣布全部满足。
- `HIS-B`：官方 PDF 曾遇 HTTP 403，完整可验证正式翻译输入尚未闭环；Co-op **无法解决访问授权、下载或来源合法性问题**。
- `HIS-C`：有出版社 PDF 与第三方 EPUB 下载证据、BCcampus XML ZIP 目录线索；EPUB/XML 的章节完整性、版次一致性和真实正文仍需具体证据，不应将“找到 XML 下载项”写成“已取得完整 XML”。

上述以既有研究记录 [R3–R5] 为准；本轮没有再次下载大文件、提取全文、翻译或校对出版社源文件。

独立 QC 最小建议：章节/小节/脚注与引文数目、书中历史年代与专名、超链接、原文和译文哈希、样本人工审核结论；实现优先轻量，不设计多阶段复杂权威状态。

## 5. 实施路线与 Fork 停止线

`PREFERRED_ENGINE_BASELINE=CO_OP_TRANSLATOR_PUBLIC_API`：现在作为**优先研究基线**，而不是正式采用决定。

`PREFERRED_INTEGRATION=EXTERNAL_THIN_ADAPTER`：优先锁定上游发布版本、通过稳定公开 API 实现业务差异。不要依赖尚不稳定的 `core`/`utils` 内部细节。[S2]

`FORK=DEFERRED`：只有受控样本证明公开 API 确实存在无法绕开的核心缺口，且少量上游补丁或配置无法解决时，才比较维护**唯一公共 fork**的成本；不推荐每个业务项目各自 fork，也不建议未经测试自动同步上游到生产。[R2]

`SHARED_REPOSITORY=DEFERRED`：只在第二个项目确实复用同一薄适配层且收益超过额外维护成本时考虑。

`GO_DEV_V2_MUTATION=NONE`：研究不能改变当前 go-dev 的代码、配置、授权状态与优先级。

## 6. 下一项最小验证（本轮未执行）

未来得到明确实施/受控实验授权后，优先在**独立临时目录**用一小段已核实可合法研究的公开历史教材文本（或自编模拟 Markdown，避免版权不明素材）对比：

1. 源 HTML/EPUB/XML → 标准化 Markdown 的脚注、标题、链接与注释完整性；先做无模型静态验证。
2. 使用公开 agent-assisted 接口准备/还原分块，不直接调用付费 API；核对无损还原结构。
3. 在适用且额度明确的前提下，进行一门语言、一章节、少量片段的实际翻译和独立 QC；与简易文件交接方式比较人工工时。
4. 修改单一源段落，测试 `TranslationStateProvider` 对已接受译文的保留与回退。
5. 基于确切 66 locale 清单建立映射表，标记 `DIRECT`、`ALIAS_NEEDS_REVIEW`、`UNSUPPORTED`，逐项记录路径与地区规范。

**停止线**：不安装并长期维护第二套基础设施；不 Fork、不创建历史网站、不批量翻译、不购买 API、不覆盖已批准译文；不要以静态文档结论代替运行证据。

## 7. 当前决定与输出

```text
RESULT=PARTIAL
STAGE=CO_OP_TRANSLATOR_WORLD_HISTORY_ADAPTER_FEASIBILITY_GATE
EVIDENCE_MODE=OFFICIAL_DOCS_AND_EXISTING_REPOSITORY_REPORTS
API_EXTERNAL_ADAPTER_FEASIBILITY=SUPPORTED_IN_PRINCIPLE
WORLD_HISTORY_END_TO_END=UNVERIFIED
PREFERRED_ENGINE_BASELINE=CO_OP_TRANSLATOR_PUBLIC_API
PREFERRED_INTEGRATION=EXTERNAL_THIN_ADAPTER
FORK=DEFERRED
SHARED_REPOSITORY=DEFERRED
MODEL_API_REQUIRED_FOR_STATIC_GATE=NO
FORMAL_PROJECT_SELECTED=WORLD_HISTORY
IMPLEMENTATION_AUTHORIZED=NO
RESEARCH_ONLY=YES
GO_DEV_V2_MUTATION=NONE
NEXT=CONTROLLED_SINGLE_SAMPLE_ADAPTER_VALIDATION_WHEN_AUTHORIZED
```

## 8. 证据来源

官方（核实日期 2026-11-09）：

- [S1] https://github.com/Azure/co-op-translator
- [S2] https://github.com/Azure/co-op-translator/blob/main/docs/api.md
- [S3] https://github.com/Azure/co-op-translator/blob/main/docs/mcp.md
- [S4] https://github.com/Azure/co-op-translator/blob/main/LICENSE
- [S5] https://github.com/Azure/co-op-translator/blob/main/docs/supported-languages.md

本仓库既有研究：

- [R1] `research/2026-11-07-co-op-translator-reuse-gap-audit-001.md`
- [R2] `research/2026-11-07-lightweight-translation-common-core-fork-decision-001.md`
- [R3] `research/2026-11-06-his-source-and-media-licensed-scope-freeze-research-001.md`
- [R4] `research/2026-11-06-his-three-source-completeness-and-c-epub-next-gate-001.md`
- [R5] `research/2026-11-06-his-c-xml-file-provenance-and-download-gate-001.md`
- [R6] `research/2026-11-06-history-locale-subdomain-architecture-decision-001.md`

本轮是对既有“可选复用方案”的**新增具体项目优先级判断**；它不追溯修改 2026-11-07 的历史决策，也不是批准替换 go-dev 或创建世界历史生产工程。
