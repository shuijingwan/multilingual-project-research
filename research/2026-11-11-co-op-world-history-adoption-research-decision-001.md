# Co-op Translator 世界历史项目技术选型研究决策 001

日期：2026-11-11
阶段：CO_OP_WORLD_HISTORY_ADOPTION_RESEARCH_DECISION

## 一、正式研究结论

DECISION=CONDITIONAL_PREFERRED
PREFERRED_ENGINE=CO_OP_TRANSLATOR
PREFERRED_INTEGRATION=EXTERNAL_THIN_ADAPTER
IMPLEMENTATION_AUTHORIZED=NO
RESEARCH_ONLY=YES

决定将 Co-op Translator 作为 WORLD_HISTORY
未来翻译工程的有条件首选基础框架。

这属于研究阶段的技术方向决策，
不代表批准生产采用、建设网站或大规模翻译。

## 二、已经验证的能力

- Markdown Agent-assisted 分块与还原：PASS。
- 模拟中文译文结构还原：PASS。
- 缺失翻译分块拒绝：PASS。
- 未变化块的人工修订保留：PASS。
- 单个变化块增量翻译：PASS。
- 外层候选隔离与哈希检查：PASS。
- Co-op 既有输出文件接入候选目录：PASS。

上述实验均未调用模型 API。

## 三、已发现的关键风险

### 1. 已批准译文覆盖风险

Co-op 默认翻译管理器会写入目标文件，
不能把它的普通输出目录直接当作
经过独立审核的正式 Accepted 目录。

未来必须分离：

Source / Candidate / Accepted

新候选不得直接覆盖已批准译文。
实际发布必须经过独立审核、明确批准
以及来源、候选和已批准版本的哈希检查。

### 2. Agent-assisted 与增量状态组合

Agent-assisted 内容级 API 可以由外部 Agent
生成翻译，而不要求 Co-op 自身配置付费 API。

TranslationStateProvider 支持已批准译文
基线和增量处理，但主要用于仓库级翻译流程。

两者是否能够通过公开 API 组成
一个完整、可靠、无需付费模型 API 的
增量翻译工作流，仍然是 UNKNOWN。

不得把已分别验证的功能
误写为已通过端到端集成验证。

### 3. 66 locale 支持

此前静态检查：

- 直接代码匹配：7
- 基础语言别名需审核：51
- 特殊映射需审核：3
- 官方表无对应基础代码：5

完整翻译兼容性尚未验证。
具体语言代码与正式地域变体不得直接等同。

### 4. 历史教材输入

三本历史教材的结构化全文获取、
版本一致性、章节完整性及第三方媒体授权
仍由 WORLD_HISTORY 项目单独核实。

Co-op 不替代原始资料来源与版权审核。

## 四、架构取舍

优先保留：

1. Co-op Translator 官方公开接口。
2. 轻量内容格式适配。
3. Source / Candidate / Accepted 隔离。
4. 最少的来源与译文身份哈希。
5. 独立语言和历史事实审核。
6. 显式批准后发布。

暂不移植：

- go-dev 完整 TranslationUnit 生命周期。
- 多层 authorization epoch。
- 大量 snapshot / successor 恢复机制。
- 跨项目通用翻译平台。
- 为每个项目单独维护一份 Co-op Fork。

若公开 API 在正式小样本中无法满足核心需求，
再评估单一公共 Fork 或其他实现。

## 五、停止线

不再为已经验证的普通 Markdown
分块、模拟翻译和文件隔离重复建立小型实验。

世界历史正式开发仍需单独授权，
且不得影响 go-dev v2 当前进度。

当前不存在可靠证据证明：
采用 Co-op 将直接增加自然搜索流量、
提高 AdSense 收益或降低总维护成本。
这些商业效果保持 UNKNOWN。

## 六、后续最有价值的研究问题

NEXT=HIS_THREE_BOOK_TRANSLATION_SOURCE_READINESS_REVIEW

优先回到三本历史教材的可靠正文来源、
章节完整性与授权边界。

待正式开发获准时，再使用真实章节进行
Co-op + 外层适配器的端到端受控验证。

## 七、研究证据

- research/2026-11-09-co-op-translator-world-history-adapter-feasibility-gate-001.md
- research/2026-11-10-co-op-translator-66-locale-compatibility-gate-001.md
- research/2026-11-10-co-op-agent-roundtrip-smoke-001.md
- research/2026-11-11-co-op-agent-zh-mock-gate-001.md
- research/2026-11-11-co-op-approved-edits-incremental-gate-001.md
- research/2026-11-11-co-op-candidate-isolation-risk-gate-001.md
- research/2026-11-11-co-op-candidate-promotion-isolation-pilot-001.md
- research/2026-11-11-co-op-external-output-adapter-gate-001.md

官方来源：

- https://github.com/Azure/co-op-translator
- https://github.com/Azure/co-op-translator/blob/main/docs/api.md
- https://github.com/Azure/co-op-translator/blob/main/docs/workflows.md
- https://github.com/Azure/co-op-translator/blob/main/LICENSE

## 八、最终状态

RESULT=PASS
STAGE=CO_OP_WORLD_HISTORY_ADOPTION_RESEARCH_DECISION
DECISION=CONDITIONAL_PREFERRED
FORK=DEFERRED
SHARED_REPOSITORY=DEFERRED
GO_DEV_V2_MUTATION=NONE
WORLD_HISTORY_IMPLEMENTATION=NOT_AUTHORIZED
RESEARCH_ONLY=YES
