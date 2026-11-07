# Azure Co-op Translator 与 go-dev 工程复用边界初筛 001

核实日期：2026-11-07  
阶段：CO_OP_TRANSLATOR_REUSE_GAP_AUDIT  
状态：`RESEARCH_ONLY`  
目的：判断开源工具能否降低未来多语言工程重复开发，**不是对 go-dev 的替换/迁移授权**。

## 一、主要结论

`VERIFIED`：Azure/co-op-translator 是可运行的 Python 多语言文档翻译工具，仓库根许可证为 MIT。它已经提供 Markdown/Jupyter Notebook 翻译、图片文字翻译、源文件哈希/过期检测、长文档分块与重试、结构和 URL 保护、相对链接重写、CLI/Python API/MCP/GitHub Actions、可并行的文件/语言处理和确定性维护检查。因此，go-dev 的**部分通用基础功能存在同类成熟实现**，不能宣称全部工作都是前所未有。

`VERIFIED`：本次检查 Co-op Translator 的 CLI、API 与维护文档后，发现其默认重译粒度仍按**受影响的文件**；它提供可选的 `TranslationStateProvider`，由宿主保存已接受的源文/译文基线，支持保护未变 Markdown 块中的人工修改，但文档明确指出还**没有持久化块级断点恢复状态**，且“接受哪份译文”的权威状态需宿主自行管理。

`VERIFIED`：go-dev 当前的共享翻译流程包含 TranslationUnit、来源/术语当前性、逐单元结构校验、原始输出与身份/provenance、精确 retry/revision、独立 Reviewer 的 A/B/C/D、重新审核和 A-only finalization，Site v2 还需维护独立的发布/内容契约。Co-op Translator 的确定性检查和实验性 LLM 评估，**不能据此直接等同于**这些正式审核授权机制。

`NOT_DECIDED`：没有对两套工具进行同源/同语言/同模型成本与质量对比；“谁的翻译质量更好”“是否节省实际工时”“能否嵌入而不破坏权威流程”均为 `UNKNOWN`。

## 二、能力对照与复用优先级

| 领域 | Co-op Translator 已核实功能 | 与 go-dev 的关系 | 建议 |
| --- | --- | --- | --- |
| Markdown 分块/重试 | 分块、失败重新分块及重试 | 功能范围交叠 | 可参考，暂不替换 |
| 代码/URL/Markdown 结构保护 | 解析保护及链接重写 | 与 Go 专有保护机制部分重叠，但具体契约不同 | 后续可做独立样本验证 |
| 源哈希和翻译新鲜度 | 文件级元数据与跳过未变化内容 | 与现有来源/currentness 检查有交集 | 不迁移现有 authority |
| 人工修改保留 | 选配 Markdown 块级 baseline provider；默认受影响文件整文件重译 | 不直接等价于 TU precise revision、独立 re-QC | 不作为 go-dev 替代 |
| 审核 | `co-op-review` 只读确定性结构/链接/缺漏/疑似英文检查；`evaluate` 可 LLM 评估，文档声明为实验性 | 与独立 Reviewer、A-only lifecycle 非同一强制权威 | 不互相替代 |
| Notebook / 图片文字 | 支持；图片文字需要 Azure AI Vision | 新项目可能用得上，go-dev 场景不一定需要 | **未来专项复用候选** |
| 集成 | CLI、Python API、MCP、GitHub Actions；附 Codex plugin/agent skill | 可用于轻量 Markdown 仓库或只读技术比较 | 不在主项目直接安装 |
| 正式网站生产 | 主要关注 GitHub 仓库翻译与同步 | 不覆盖 go-dev 全套 Site v2 发布职责 | 保留现有主工程 |

注：上述仅比较功能**文档/工程契约**，未进行受控运行测试，不代表 Co-op Translator 质量不足或 go-dev 翻译质量已经占优。

## 三、语言/locale 差异（重点）

截至本次核实，`docs/supported-languages.md` 的表格列有 **56 个 language/locale codes**，包括 `ja`、`de`、`fr`、`zh-CN` 等。go-dev 既定跨项目目标是 **66 个 locale**，如 `ja-JP`、`de-DE`、`fr-FR`、`zh-CN`。

不能直接计算 `66-56=10` 作为真实缺口，因为二者语言代码粒度、地区变体和映射方式不同。未来若考虑采用，须逐 locale 检查映射、地区表达、RTL、字体、文件路径及输出结果；Co-op 声称支持某语言代码也不代表已独立验证相应完整教材译文质量。

## 四、成本、授权、可靠性与使用边界

- `VERIFIED`：Co-op Translator 仓库根 MIT 许可证允许符合条款的商业软件使用、修改与再分发；**不自动授权翻译任意第三方课程，也不覆盖独立媒体的不同许可**。
- `VERIFIED`：文本翻译可配置 Azure OpenAI、OpenAI 或 Anthropic；使用提供方 API 的实际费用/配额依其服务而定。图片翻译另外依赖 Azure AI Vision。
- `VERIFIED`：Co-op Translator 的 agent-assisted **单内容**接口可让宿主模型翻译预处理分块，但文档表明其不会自动创建完整的 repository sync metadata；不应推断 Codex 订阅额度可无成本完成全部批量翻译。
- `VERIFIED`：`co-op-review` 的结构/缺漏检查是启发式的，不证明语义正确；图片文字需人工视觉复核；`evaluate` 仍标注 experimental。
- `UNKNOWN`：对 go-dev 特定 protected representations、code comments、严格 provenance、术语 authority 和 66 locale 的完整兼容性、真实成本优势、端到端审校质量。
- `ESTIMATE`：强制替换主项目可带来适配、回归及权限风险，并可能扰动 current authority；需要小样本证据才值得考虑。

## 五、决策与唯一未来验证问题

**当前：不在 go-dev 引入、替换或重构。** 将 Co-op Translator 作为未来 GitHub Markdown/Notebook 或图片文字项目的候选实现，优先复用成熟模块、数据契约和经验，而不是再写一遍同类工具。

若正式项目出现真实的 Markdown/Notebook 需求，在**独立临时目录和无敏感数据的单篇测试文档**中评估：`dry-run`、受保护代码和链接保持率、修改源文本后人工译文是否保留、对应 locale 映射、复核及 API 成本。先检查合法授权和配置，不使用 go-dev 的正式生命周期文件做试验。

**停止线**：没有明确可复用需求时不安装、不集成、不重写、不搭建新的共享翻译框架。

## 六、来源

- https://github.com/Azure/co-op-translator
- https://github.com/Azure/co-op-translator/blob/main/LICENSE
- https://github.com/Azure/co-op-translator/blob/main/README.md
- https://github.com/Azure/co-op-translator/blob/main/docs/cli.md
- https://github.com/Azure/co-op-translator/blob/main/docs/api.md
- https://github.com/Azure/co-op-translator/blob/main/docs/workflows.md
- https://github.com/Azure/co-op-translator/blob/main/docs/maintainer-guide.md
- https://github.com/Azure/co-op-translator/blob/main/docs/agents.md
- https://github.com/Azure/co-op-translator/blob/main/docs/configuration.md
- https://github.com/Azure/co-op-translator/blob/main/docs/supported-languages.md
- https://github.com/shuijingwan/go-tour-i18n/blob/main/docs/SHARED_TRANSLATION_UNIT_LIFECYCLE.md
- https://github.com/shuijingwan/go-tour-i18n/blob/main/docs/TERMINOLOGY_GUIDE.md
- https://github.com/shuijingwan/go-tour-i18n/blob/main/docs/TRANSLATION_WORKFLOW.md
- https://github.com/shuijingwan/multilingual-project-research/blob/main/research/2026-11-03-engineering-reuse-inventory.md

`CO_OP_TOOL_LICENSE=MIT_VERIFIED`  
`GENERIC_FEATURE_OVERLAP=VERIFIED`  
`GO_DEV_FULL_WORKFLOW_REPLACEMENT=NOT_SUPPORTED_BY_CURRENT_EVIDENCE`  
`GO_DEV_COMPATIBILITY=UNKNOWN`  
`CO_OP_LANGUAGE_CODE_COUNT=56`  
`TARGET_LOCALES=66`  
`ADOPTION=DEFERRED`  
`MIGRATION=NOT_AUTHORIZED`  
`GO_DEV_V2_MUTATION=NONE`  
`RESEARCH_ONLY=YES`
