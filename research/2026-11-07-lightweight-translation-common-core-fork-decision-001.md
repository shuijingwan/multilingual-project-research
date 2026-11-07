# 世界历史轻量翻译流程与跨项目公共底层：Fork 方案决策边界 001

决策记录日期：2026-11-07  
状态：`RESEARCH_ONLY` / `PRE_LAUNCH_PLANNING`  
性质：设计方向与技术选型停止线，**不是实施批准、源代码迁移或工具选型最终结果**  
主项目：go-dev v2  
已选第二项目：`WORLD_HISTORY`（不改变正式选型）

## 一、负责人目标与核心取舍

负责人希望以世界历史为未来第一个实践项目，借鉴 go-dev 与 Azure Co-op Translator 的经验，建立**尽量轻量、能够在其他多语言项目中复用的底层能力**。公共仓库是否必要、是否依赖或 fork Co-op Translator，均延至有真实实施需求时再决定。

约束：
- 只有一位负责人，优先确定清晰、顺序化、可恢复的命令，不照搬 go-dev 在历史兼容、复杂 epoch、重复全局证明和多阶段基础设施上的全部复杂度。
- ChatGPT 与 Codex 可以作为文件交接的翻译执行者；初始设计**不得强制要求付费模型 API**。外部模型额度、政策与未来成本不预先保证。
- 不把「轻量」解释为取消来源身份、受保护文本还原、结构完整性、独立质量审核、已批准译文防覆盖及发布前版本检查。
- 不为了追求“全部自行维护”而重新编写成熟的 Markdown/XML/PDF 解析功能。

## 二、三个层次必须分离

1. **上游内容**：历史出版社 PDF/XML、将来 Rust/Python 教程或其他项目；其许可、版本和章节映射由各内容项目自行维护。
2. **通用翻译能力**：输入/输出格式、来源 SHA-256、可翻译/不可翻译内容识别、精确还原、完整性校验、候选与批准译文隔离、最小人工审校记录。其实现可以先在世界历史项目内部，未来按真实复用需求提取。
3. **项目专有部分**：PDF/XML 解析和章节建模、历史术语与媒体许可、代码示例与技术术语、站点模板/SEO/发布方式。不得为了“跨项目统一”把这些专有规则塞进公共底层。

跨项目统一的是**清晰的数据契约和少量稳定能力**，不等于所有站点共享同一种后端语言或同一套复杂生命周期。

## 三、Fork / 依赖 / 自有轻量底层比较

| 候选 | 特点 | 风险 | 当前判断 |
| --- | --- | --- | --- |
| 各项目分别 fork Co-op Translator 并改造 | 每个项目都有完整源码 | 每个项目都需解决同一批上游同步/冲突；大量重复版本维护 | **不推荐** |
| 单一 Co-op Translator fork，所有项目使用其发布版/固定 commit | 工具改动只维护一份，可统一同步上游 | 工具内部架构、提供方依赖、版本升级和自有补丁易耦合；不自动提供正式独立 QC | **条件性备选** |
| 各项目使用未经修改的 Co-op Translator 公开 Python API | 无需维护 fork，可能直接复用 Markdown/Notebook 分块、还原等 | Agent-assisted content 不自动提供全仓库同步元数据；外部库仍需锁版本与回归测试 | **可在小样本中优先验证** |
| 先做独立轻量 workflow，必要时提取自有公共底层 | 适配 ChatGPT/Codex 文件工作流、便于控制功能范围 | 仍需自行写少量 glue、保护与状态记录 | **当前优先设计方向** |

技术说明：**fork 是上游源码分支，不是每个业务仓库都应该继承的项目模板**。若日后 fork 有价值，只维护**一份公共 fork**；历史、Rust、地理等仍是独立业务仓库，通过固定版本的依赖/CLI/包调用共享实现。不要在每个项目复制或 fork 一份工具实现，也不要定时无验证地自动升级所有下游。

## 四、Co-op Translator 的实际适用边界

`VERIFIED`（2026-11-07）：其公开 API 明确提供：
- `start_markdown_agent_translation` / `finish_markdown_agent_translation`：宿主 Agent 翻译受保护的 Markdown 分块，再还原；不需要 Co-op 自身付费 API key，但消耗宿主 AI 使用额度。
- `translate_markdown_content` / `run_translation`：使用配置的模型服务商进行内容或仓库级翻译；标准批量模式通常需要 API 凭据。
- `run_review`：确定性结构/缺漏/链接检查，不等于有真实独立 Reviewer 的人工或语言语义质量批准。
- `TranslationStateProvider`：可选 Markdown 已批准基线与未变块复用；默认过期文件会整文件重译，持久化块级断点恢复不是其内建承诺。

文档将 `co_op_translator.api` 明确为稳定公开 API；较底层 `core`/`utils` 是实现细节，不应直接当成稳定扩展点。若确实要大量修改其内部代码，后续合并上游就可能增加冲突与回归维护工作。

`UNKNOWN`：实际多项目所需能力与 Co-op 当前 API 的匹配度、不同 locale 映射、历史官方 PDF/XML 提取、长期模型成本、fork 同步工时、是否能满足世界历史独立审校契约。未经受控样本不能宣称采用或拒绝任何一种技术方案。

来源：
- https://github.com/Azure/co-op-translator/blob/main/docs/api.md
- https://github.com/Azure/co-op-translator/blob/main/docs/agents.md
- https://github.com/Azure/co-op-translator/blob/main/docs/workflows.md
- https://github.com/Azure/co-op-translator/blob/main/LICENSE
- https://github.com/shuijingwan/go-tour-i18n/blob/main/docs/SHARED_TRANSLATION_UNIT_LIFECYCLE.md
- https://github.com/shuijingwan/multilingual-project-research/blob/main/research/2026-11-07-co-op-translator-reuse-gap-audit-001.md

## 五、最小流程原则（未来获准实施时）

原则性顺序：
1. 官方来源采集/格式提取；记录教材版本、章节身份、源 SHA-256 与媒体许可。
2. 规范化为章节/小节候选结构；保护脚注标识、不可翻译内容及链接；输出可重复生成的输入。
3. 人工选定 ChatGPT、Codex 或以后可用的执行者完成翻译；工具仅验证传回文件的内容与单元身份，不绑定具体模型提供方。
4. 精确还原和结构校验；不覆盖已批准译文；独立 Reviewer 核查语言与历史事实，需要时只修订受影响内容。
5. Git 保存被接受的译文及最少的审核证据（source hash、target hash、审核结论、实际模型/执行者及日期）；发布前验证所用源文/译文仍等于审核时版本。
6. 网站构建和部署由项目专有流水线承担，不混入通用翻译核心。

不默默牺牲质量边界，但不预建多层 epoch、跨项目历史重放、复杂 migration 状态机及全量重复校验。已有成熟解析库、格式工具或 Co-op 公开接口可作为可插拔候选，不为“零依赖”刻意自造。

## 六、何时才考虑公共仓库及 fork

**当前无需创建新仓库、新框架或 fork。** 世界历史正式开发至少等 go-dev v2 完成且得到单独授权。

实际出现第二个有明确共同需求的项目后，再依据以下条件决定：
1. 两个项目确实使用同一批稳定、语言/领域无关的接口，且迁出共享代码的收益超过新增版本管理与发布工作。
2. 先评估未修改的 Co-op 公开 API 是否足够；若够用，直接锁定外部版本，无需 fork。
3. 若确有无法通过 API/插件/外部适配解决的修改，评估向上游提交补丁或保持少量 patch；只有补丁无法上游化、且保留现有代码明显优于自有小实现，才建立**唯一公共 fork**。
4. 公共 fork 必须采用单一上游同步流程：评估 release、隔离分支合并、运行受控回归、发布固定版本；各业务项目**按需升级**，不跟随定时同步自动更新。
5. 若多数功能仅用到 Markdown 占位符、输入输出契约和独立审校流程，而 Co-op 全部依赖明显过重，则优先少量现成解析库加自有轻量核心，不以 fork 作为默认底座。

## 七、正式结论和停止线

`PREFERRED_DESIGN=LIGHTWEIGHT_PROVIDER_AGNOSTIC_WORKFLOW`  
`CROSS_PROJECT_REUSE_GOAL=YES`  
`SHARED_CORE_REPOSITORY=DEFERRED_UNTIL_PROVEN_NEED`  
`CO_OP_TRANSLATOR_ROLE=REFERENCE_OR_OPTIONAL_PUBLIC_API`  
`CO_OP_FORK=NOT_AUTHORIZED`  
`FORK_PER_PROJECT=NOT_RECOMMENDED`  
`SINGLE_SHARED_FORK=CONDITIONAL_FUTURE_OPTION`  
`AUTOMATIC_UPSTREAM_SYNC_TO_PRODUCTION=NO`  
`PAID_MODEL_API_REQUIRED=NO_FOR_INITIAL_DESIGN`  
`INDEPENDENT_REVIEW=REQUIRED`  
`GO_DEV_V2_MUTATION=NONE`  
`WORLD_HISTORY_IMPLEMENTATION=NOT_AUTHORIZED`  
`RESEARCH_ONLY=YES`

**下一项有价值的调查问题**：在未来获准实施时，找一段无敏感信息的 HIS-C 官方 XML 小样本，比较“现成解析库＋轻量文件交接”与“调用 Co-op Agent-assisted API”的实际工作量与质量门槛；不以研究报告代替真实实现验证。
