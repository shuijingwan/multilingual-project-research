# 项目范围与生命周期

更新时间：2026-11-06  
状态：`RESEARCH_ONLY`  
定位：**Multilingual Project Research & Pre-Launch Planning（多语言项目研究与启动前规划）**

## 一、目标与成功指标

本仓库用于跨领域发现、研究、选择具有长期用户价值和商业潜力的多语言内容网站及工具网站，并为**已选项目**完成低成本、可中断、可交接的启动前规划。

终极商业目标是**长期自然搜索流量带来的可持续广告净收益**，同时考虑用户价值、授权合规和长期维护成本。翻译数量、语言数量、仓库提交数或页面数量均不是主要成功指标。

go-dev v2 是当前主项目。本仓库的任何研究都不得影响它的开发、质量审核或上线，也不得未经授权修改其代码、配置或生命周期。

## 二、允许的三个阶段

### 阶段 A：候选领域发现与初筛（DISCOVERY）

- 发现技术和非技术领域的候选项目；筛查长期需求、竞争、语言覆盖和用户价值。
- 核实原文、图片、源码、数据及平台条款的商业许可，区分它们的不同授权。
- 记录可信证据、核实日期、`VERIFIED`/`ESTIMATE`/`UNKNOWN`/`UNCLEAR` 结论以及停止线。
- 不以官方已有部分语言自动排除其余目标语言，关注实际内容范围、质量、更新状态和形式。

### 阶段 B：正式选型与决策（SELECTION）

- 对候选进行可核查的商业取舍：需求、竞争、语言缺口、版权、广告适配、工程和维护成本。
- 明确项目决定：`SELECTED`、`RESEARCH_CONTINUE`、`PAUSED` 或 `REJECTED`。
- **选定项目不等于批准实施**；流量和收益证据不足时仍记录`UNKNOWN`，不填造 RPM 或收入。
- 决定后可以停止横向选型研究，也可以根据实际需要另行研究其他方向。

### 阶段 C：已选项目的启动前规划（PRE_LAUNCH_PLANNING）

本阶段仍归属本仓库，而非必须立即新建独立仓库。

允许：
- 确认官方内容源、版本身份、文件哈希、章节完整性、媒体许可证和可商用性；
- 研究具体书籍、数据源或功能的范围，规划国家/地区语言变体与有效官方覆盖；
- 对官方页面、PDF、XML、EPUB 等来源进行**小规模、只读**的质量和格式可行性验证；
- 比较阅读体验、是否链接官方、是否需要独立 HTML、网站架构的最小方案；
- 轻量原型或只读脚本用于证明关键风险，避免建设第二套完整翻译框架；
- 形成可交接的项目决策、证据索引、已知风险、待办和未来工程成本边界。

**完成标准不是无止境补齐每个细节**：若内容源与版权、目标用户价值、核心语言策略、主要实施障碍和商业不确定性已得到充分梳理，就应形成一份`PRE_LAUNCH_HANDOFF`；低价值次要问题可留待真正启动时决定。证据不足则保留`UNKNOWN`，不因有未知项而无限延迟交接。

### 阶段 D：正式实施（OUT_OF_SCOPE）

以下需要负责人另行明确授权，原则上在独立项目仓库进行：
- 正式翻译及大规模质量审核；
- 正式内容网站与生产阅读器、批量页面生成；
- 完整翻译工程、部署系统、DNS或域名批量操作；
- 面向生产的持久化内容管线、上线及商业运营。

启动独立仓库的时点由负责人决定，不会因为正式选型或研究规划完成自动触发。

## 三、当前已选世界历史项目

- `SECOND_PROJECT=WORLD_HISTORY`：第二个项目**已经选定**。
- 项目标识：`world-history`；正式项目独立仓库尚未建立，也不要求现在建立。
- `SELECTION=SELECTED`；`PRE_LAUNCH_PLANNING=IN_PROGRESS`（可随时暂停）。
- `SOURCE_BOOKS=3`：HIS-A / HIS-B / HIS-C，官方原著 PDF 已取得；HIS-C 另取得出版社官方 XML。
- 正式翻译只能依据出版社或官方权威提供的原著；第三方镜像可作为研究对照，**不作为正式原文输入**。
- 目标语言计划保持 66 locale，其中七个英语地区变体均在范围内；三本书目前均有美式英语原文的强证据。原文语言和其他变体的网页策略按书×locale具体评估。
- 已正式批准的网页形式例外：出版社只有 PDF 等非语义 HTML 源、缺少可用的官方 HTML 正文时，可以从官方原著建立有实际增量阅读价值的 HTML 网页；不意味着必须复制所有官方网页。
- 来源、媒体版权、版本对照和用户体验的进一步验证，依然只能在本仓库研究范围内低成本进行，不能直接开始建设站点。
- 搜索需求、自然流量、广告收益、长期净利润尚无足够实证的部分继续标记 `UNKNOWN`。

### 世界历史启动时间限制

**负责人于2026-11-06确认：世界历史项目正式开发至少应等 go-dev v2 完成以后。也可能等到 go-dev v3，启动时点尚未确定。**

- `WORLD_HISTORY_IMPLEMENTATION_BEFORE_GO_DEV_V2_COMPLETE=NOT_AUTHORIZED`
- `GO_DEV_V3_DEPENDENCY=POSSIBLE_NOT_DECIDED`
- `WORLD_HISTORY_IMPLEMENTATION_START_DATE=UNKNOWN`
- **go-dev v2 完成不会自动授权世界历史开工**；届时仍须结合主项目进度、投入成本和商业证据作独立决策。
- 在此之前，世界历史只允许不影响主项目的零散、低成本启动前研究；不要求持续开展，也不预定结束日期。

## 四、记录、权威与交接规范

- 现有历史调查报告留在本仓库，**不迁移、不删除、不重写 Git 历史**。先前已完成的初期规划本身属于本仓库更新后的合法范围。
- 同一事项有前驱研究和新决策时，应在新报告明确其对前驱结论的覆盖关系；不要将旧的推测误当成当前权威。
- 正式研究记录尽量进入 Git；提交使用中文为主的 Conventional Commits（例如 `docs:`、`fix:`）。
- 原始 PDF/EPUB/XML 可以保留在安全的本地证据位置，公开仓库中优先保存 URL、SHA256、体积、核实日期及许可结论，避免提交过大的原文件或未经授权的素材。
- 启动阶段真正获准时，再建立专属项目仓库，并通过`PRE_LAUNCH_HANDOFF`引用这里的决策、证据和风险，避免重复复制所有报告。

## 五、边界摘要

```text
RESEARCH_REPOSITORY_SCOPE=DISCOVERY_SELECTION_PRE_LAUNCH_PLANNING
RESEARCH_ONLY=YES
SECOND_PROJECT=WORLD_HISTORY
SECOND_PROJECT_SELECTION=SELECTED
WORLD_HISTORY_PRE_LAUNCH_PLANNING=IN_PROGRESS
WORLD_HISTORY_IMPLEMENTATION=NOT_AUTHORIZED
WORLD_HISTORY_IMPLEMENTATION_BEFORE_GO_DEV_V2_COMPLETE=NOT_AUTHORIZED
GO_DEV_V3_DEPENDENCY=POSSIBLE_NOT_DECIDED
WORLD_HISTORY_START_DATE=UNKNOWN
INDEPENDENT_HISTORY_REPOSITORY=DEFERRED_UNTIL_IMPLEMENTATION_APPROVAL
GO_DEV_V2_PRIORITY=UNCHANGED
```
