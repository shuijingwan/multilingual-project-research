# Berkeley CS188 教材：同源译文与五语言搜索竞争试点 001

核实日期：2026-11-08  
阶段：`BERKELEY_CS188_SOURCE_EQUIVALENT_LOCALE_AND_SEARCH_PILOT`  
仓库状态：`RESEARCH_ONLY`  
主项目：go-dev v2  
第二项目：`WORLD_HISTORY / SELECTED_NOT_LAUNCHED`  
AI 新项目：`NOT_SELECTED`  
研究目标：具体来源的合法商业翻译、五门语言的**同源正文**与**同任务内容**竞争、独立网站新增价值。不得把搜索结果出现当搜索量、点击量或收入。

## 一、研究范围与冻结源版本

官方可公开访问的 BerkeleyAI 源仓库：https://github.com/BerkeleyAI/textbook

本轮锁定的 Git 提交：`b0aa2b1f8315ed5c027cfc9741e8b7269420c86a`  
提交链接：https://github.com/BerkeleyAI/textbook/commit/b0aa2b1f8315ed5c027cfc9741e8b7269420c86a

已通过 GitHub 按上述 commit 读取正文并确认与当时 main 的对应文件 blob SHA 一致。冻结四个不同单元的基础章节，实际是四篇而非全书：

| 章节 | 具体使用任务 | 文件路径 | Blob SHA |
| --- | --- | --- | --- |
| 1.3 Uninformed Search | BFS / DFS / UCS 的 frontier、完备性与最优性 | `search/uninformed.md` | `4cc3a445e73cc83d45761bf30a48748ffa1d441d` |
| 1.4 Informed Search | 启发函数、A*、可采纳/一致性条件 | `search/informed.md` | `7e3076c4264242b68465e0ded1b4b6e8fb291575` |
| 4.1 Markov Decision Processes | 状态、动作、转移概率、折扣、奖励 | `mdp/markov-decision-processes.md` | `f9deb78a85bbbedd01090cbd74354d749944c1a9` |
| 5.1 Reinforcement Learning | 离线规划、在线交互与学习概念 | `rl/rl.md` | `83c41ec681adc9b90226948571a1f68d61bddf7c` |

授权：原仓库 `index.md` 明确声明教材正文 CC BY-SA 4.0；对其许可覆盖的原书内容，商业翻译、修改及再分发具有授权基础，但须署名、注明改动并遵守相同方式共享要求。教材不是课程作业和《Artificial Intelligence: A Modern Approach》原书的统一版权许可。

图片与嵌入：抽样 Markdown 直接引用 `assets/images/` 下如 `dfs.png`、`bfs.png`、`ucs.png`、`manhattan.png`、`race-car.png`、`feedback-loop.png` 等图片。图片在仓库内并不自动证明全部由作者原创或可用于本项目；本轮**未完成**逐图作者、来源、独立许可排查。发布时必须有图片级白名单，无法验证则去掉/自行绘制/只引用来源。官网 PDF 与课程其他教材、练习、Pacman 项目不可直接以 `index.md` 授权覆盖。

来源：
- https://github.com/BerkeleyAI/textbook/blob/main/index.md
- https://github.com/BerkeleyAI/textbook/blob/b0aa2b1f8315ed5c027cfc9741e8b7269420c86a/search/uninformed.md
- https://github.com/BerkeleyAI/textbook/blob/b0aa2b1f8315ed5c027cfc9741e8b7269420c86a/search/informed.md
- https://github.com/BerkeleyAI/textbook/blob/b0aa2b1f8315ed5c027cfc9741e8b7269420c86a/mdp/markov-decision-processes.md
- https://github.com/BerkeleyAI/textbook/blob/b0aa2b1f8315ed5c027cfc9741e8b7269420c86a/rl/rl.md
- https://inst.eecs.berkeley.edu/~cs188/textbook/

**官方身份边界**：Berkeley CS188 春季 2026 课程政策说明，其课程正式教材是 AIMA 第四版，而 `BerkeleyAI/textbook` 是往届助教撰写的**非官方辅助教材**。原教材自述为 CS188 textbook 不改变教学政策的归类。独立再分发不得声称伯克利大学正式授权、认可或推荐本站。
- https://inst.cs.berkeley.edu/~cs188/sp26/policies/

## 二、五语言：同源翻译与同任务内容分开

### zh-CN：发现了强烈的同源正文竞争证据

2026 年 8 月的中文网站自述「十章正文依据 cs188.pdf 按页翻译整理」，给出搜索、CSP、博弈、MDP、RL、贝叶斯网络、决策网络、HMM、ML、逻辑等十章导航，并明确引用 `BerkeleyAI/textbook` 作者、链接及 CC BY-SA。其第一章搜索的搜索引擎索引片段中，1.3 无信息搜索对 `frontier` 展开原理、1.4 对一致代价搜索与启发式函数的讲解，与冻结的同名英文 Markdown 章节在结构和内容上明显对应。

站点导航及自述：https://minsecrus.github.io/learning-notes/notes/2026/08/01/cs188-introduction-to-ai
第一章搜索结果：https://minsecrus.github.io/learning-notes/notes/2026/08/01/cs188-introduction-to-ai/01-search

**限定结论**：
- `VERIFIED`：具体中文竞争站、十章内容目录、授权/来源声明、第一章 1.3 和 1.4 的同结构文字样本被公开索引。
- `STRONG_SOURCE_EQUIVALENT_INDICATION`：至少搜索章节与当前 Berkeley 教材来源高度重叠；不能再称简体中文“暂无同源译文”。
- `UNCLEAR`：本轮尝试打开 1.3/1.4 所在章节页面以及 MDP、RL 深链接时收到 404；所以**不能确认**现时可读取的全部十章正文、实际完整程度或与冻结 commit 全文逐段等价。目录可访问不意味着全部正文有效，搜索索引片段也可能是旧缓存。
- `UNCLEAR`：该站在正文自述改编内容 CC BY-SA，页面统一页脚出现 CC BY-NC-SA；这是不同范围告示的可见差异，本轮不作其合法性结论。
- 另有 https://github.com/Anxi7/CS188-Note-Translate 以及 https://github.com/darstib/cs188 ，属于课程讲义/学习笔记和项目等竞争，**不能混同为冻结的教材源全文译本**。

### ja-JP

本轮没有核实四个固定 Markdown 的完整日文逐篇译本；不能推出不存在。**同任务竞争已核实**：日本语 MDP/值迭代文章及日本学术/出版社出版的 MDP 教材。
- https://ja.getdocs.org/cs-mdp-value-iteration
- https://www.morikita.co.jp/books/mid/085521
- https://www.kodansha.co.jp/book/products/0000411364

判定：`EXACT_SOURCE=UNKNOWN`；`SAME_TASK=VERIFIED`。

### de-DE

本轮未核实固定 Markdown 的完整德语同源译文。**同任务竞争**：德国 FH Bielefeld(Hochschule Bielefeld) A* 算法教程，介绍可采纳/一致启发式及其限制。
- https://www.hsbi.de/elearning/data/FH-Bielefeld/lm_data/lm_1358898/searching/search5-astar.html

判定：`EXACT_SOURCE=UNKNOWN`；`SAME_TASK=VERIFIED`。

### es-ES

本轮没有确认 Berkeley 教材逐篇完整西班牙语译本；**同任务竞争**：西语大学/机构的搜索与决策过程教材材料（包括 Bío-Bío University 和西语 MDP 教学研究资源）。
- https://dsi.face.ubiobio.cl/somos/libro_ia/capitulos/Capitulo_8.pdf
- https://www.scielo.org.mx/scielo.php?script=sci_arttext&pid=S1405-77432025000200003

判定：`EXACT_SOURCE=UNKNOWN`；`SAME_TASK=VERIFIED`。

### id-ID

没有核实固定 Markdown 的完整印尼语同源译本；**同任务竞争**：印尼高等教育课程平台已有无信息搜索、启发搜索、A* 的印尼语教材页：
- https://lmsspada.kemdiktisaintek.go.id/mod/page/view.php?id=158350

判定：`EXACT_SOURCE=UNKNOWN`；`SAME_TASK=VERIFIED`。

此处所有 `EXACT_SOURCE=UNKNOWN` 表示有限公开搜索未充分判定：不等于 `VERIFIED_ABSENT`。四语言有同任务页面也不自动等于拥有完整、免费且源等价的学习路径。

## 三、最值得考虑的搜索任务与商业边界

抽查的**三个任务意图**：
1. BFS/DFS/UCS 何时使用、是否完备或最优；
2. A* 搜索启发函数如何设计，admissibility/consistency 的证明条件；
3. MDP 到强化学习如何衔接、值迭代/策略迭代为何有效。

现有多个语言的大学、教育平台、博客、书籍已经覆盖具体任务。**存在可见内容供给**，但没有可重复的关键词点击量、SERP 点击率、广告价值或索引份额；即使某 locale 未找到同源译文，也不能把其广泛搜索市场视为容易取得。

以中文为例，同一本书的 2026 年中文十章竞争网站已经在用户能检索的范围出现，降低翻译一模一样的基础章节带来的独立知识增量。若想提供更强价值，需要真实的本地化例题互动、图示可访问性、习题讲解等，但那属于**额外内容与开发投入**，本研究尚未证明用户未满足，也未授权实施。

商业关键数据：
- `KEYWORD_SEARCH_VOLUME=UNKNOWN`
- `ATTAINABLE_ORGANIC_CLICKS=UNKNOWN`
- `SERP_CTR=UNKNOWN`
- `AD_PAGE_RPM=UNKNOWN`
- `LONG_TERM_AD_NET_PROFIT=UNKNOWN`
- `66_LOCALE_EFFECTIVE_COVERAGE=UNKNOWN`

网站目的必须是长期用户价值与合法广告净收益，不能以翻译四章或 66 语言作为主要 KPI。

## 四、停止判断

本轮明确**暂缓 Berkeley CS188 作为正式 AI 多语言教材网站项目**：

- 源正文许可为正面证据，但图像素材范围未完整确认；
- zh-CN 已有强同源竞争线索，不可宣称空白；
- 其余四语言虽未确认完整同源译本，但主要任务均存在当地学习资料；
- 尚未证明具有可获取自然点击和能超过运营维护费用的广告净收益；
- 原教材历史更新较慢不能替代长期来源监控与专业审校。

维持：`BERKELEY_CS188=RETAINED / DEEP_DIVE_PAUSED`。如出现**具体 locale 的真实搜索点击证据**、被现有资料遗漏的明确用户任务及可验证互动价值，可再启动单点项目比较，否则不再对相似“AI 教科书”的泛泛列举无限扩张研究。

**建议下一项研究**：结束此轮 AI 系统教材筛选，不因连续候选被暂停就强行选出 AI 项目。已有世界历史第二项目正式方向。若将来重新分配调研时间，应先围绕**细分用户需求**及可获取搜索点击证据，而不是再找到一本可以 CC BY-SA 翻译的书就立项。

不开展任何翻译、建站、Codex 重工程、外部模型调用采购，也不修改 go-dev。

```text
RESULT=PASS
STAGE=BERKELEY_CS188_SOURCE_EQUIVALENT_LOCALE_AND_SEARCH_PILOT
FROZEN_COMMIT=b0aa2b1f8315ed5c027cfc9741e8b7269420c86a
SAMPLED_SOURCE_CHAPTERS=4
SAMPLED_LOCALES=5
SOURCE_LICENSE=CC_BY_SA_4_0_VERIFIED
THIRD_PARTY_MEDIA_LICENSE=UNCLEAR
ZH_SOURCE_EQUIVALENT_INDICATION=STRONG_WITH_ACCESS_LIMITATIONS
JA_DE_ES_ID_EXACT_SOURCE=UNKNOWN
SAME_TASK_COMPETITION=VERIFIED_IN_ALL_5_LOCALES
SEARCH_VOLUME=UNKNOWN
ORGANIC_CLICKS=UNKNOWN
AD_PAGE_RPM=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN
BERKELEY_CS188_DEEP_DIVE=PAUSED
FORMAL_AI_PROJECT_SELECTED=NO
SECOND_PROJECT=WORLD_HISTORY
RESEARCH_ONLY=YES
```
