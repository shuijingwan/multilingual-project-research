# AI 用户任务需求与现有供给停止门槛 001

核实日期：2026-11-08  
阶段：`AI_USER_TASK_DEMAND_AND_SUPPLY_STOP_GATE`  
项目：`RESEARCH_ONLY`，第二项目 `WORLD_HISTORY / SELECTED_NOT_LAUNCHED`，无新 AI 正式项目。  
前驱：`research/2026-11-08-berkeley-cs188-source-equivalent-locale-and-search-pilot-001.md`

## 一、问题和方法

此前针对 Ragas、NeMo Guardrails、Berkeley CS188 等的研究表明“某源文有商业翻译许可”与“独立多语言广告网站存在可达自然搜索机会”之间缺乏证据链。

这轮不继续枚举教材许可证，改从公开第一人称问题出发，核查：
1. 用户提出的具体困难（`USER_REPORTED_PROBLEM`）；
2. 现有可用工具的覆盖（`CURRENT_SUPPLY`）；
3. 现有产品仍未满足的**独立网站**价值（`UNMET_NEED_AFTER_SUPPLY`）；
4. 搜索量/自然点击/AdSense RPM（不知道就标 `UNKNOWN`）。

有限样本为两个任务，而不是全领域商业排名：A. 本地 LLM 显存 / KV Cache 估算；B. 多语言 LLM Token 成本比较。

## 二、任务 A：本地 LLM 显存估算

### 真实问题

Reddit 本地 LLM 社区的公开一手讨论：
- 2026-03-06：用户询问 Qwen 模型 128K context 消耗的显存计算方法；社区指出量化、上下文、不同执行框架会导致大幅偏差。
  https://www.reddit.com/r/LocalLLaMA/comments/1rmkzzu/how_to_find_for_a_model_how_much_vram_we_need_for/
- 2026-06-06：用户反馈一些 VRAM calculator 夸大了 activations 所需显存，导致实际可运行模型被显示为不适配；这是**用户反馈**，不是本研究复现并确认的具体计算器 BUG。
  https://www.reddit.com/r/LocalLLaMA/comments/1tym480/better_vram_estimator/
- 2026-06-24：用户问不同推理后端（llama.cpp、vLLM、SGLang）的上下文、KV Cache 和量化显存如何可靠估算；提及已有 HF accelerate 和专用计算器。
  https://www.reddit.com/r/LocalLLaMA/comments/1ueb2yn/whats_everyone_using_to_estimate_vramram_weights/
- 2026-09-04：用户询问模型文件/上下文显存能否分布到双 16GB GPU，和 132K context 的计算方式。
  https://www.reddit.com/r/LocalLLaMA/comments/1w7i7mz/help_me_understand_gguf_sizectx_size/

### 竞争供给

- https://canirunllm.dev/ ：用户可选模型、GPU、量化、context、KV 精度、CPU offload，公开各项显存分解；示例注明 GGUF 文件实际大小与模型配置来源。
- https://llmvramcalc.com/ ：按模型量化/context/GPU 比较显存分配，并处理 GQA、混合/滑动窗口架构等，提供推理/训练选择。
- https://kenodo.com/tools/llm-vram-gpu-calculator ：独立模型与 KV Cache 估算工具。
- https://github.com/AlexsJones/llmfit ：真实 README 明确提供硬件自动检测、Web/TUI、估算、基准测试/共享结果及多运行时支持。README 存在中文与日文版本链接，说明多语言页面并非当然空白。它的 README 自述和功能不是本研究端到端精度测试。

### 停止判断

`USER_REPORTED_PAIN=VERIFIED`；`EXISTING_TOOL_SUPPLY=VERIFIED`；`BUG_INDEPENDENT_REPRODUCTION=NOT_DONE`；`UNMET_NEED_AFTER_SUPPLY=NOT_VERIFIED`。

市场或许存在**不同硬件/不同推理后端实际测量准确度**的残余需求，但若要声称优于工具，需要付出跨模型、驱动、设备、运行时实测与持续更新成本；目前缺乏证据支持单人独立广告网站拥有可持续差异化。维持 `PAUSED`，不开展显存计算器开发。

## 三、任务 B：多语言 Token 成本比较

### 真实问题与技术意义

- 2026-06-11 的 Reddit 讨论明确询问非英语提示是否因 token 用量差异增加成本；属于用户提出的疑问，帖子本身没有账单级交叉验证。
  https://www.reddit.com/r/ChatGPT/comments/1u37es3/does_anyone_actually_think_about_token_costs_when/
- `tokentax` 的开放评估使用 FLORES+ devtest 的同义跨语言句子对不同 Tokenizer 进行定量比较。其项目自述 222 种语言，提供逐 Token 高亮与个人文本估算。其数值是项目提供的数据，不应当作本项目独立复核的绝对 API 账单。
  https://github.com/Anri-Lombard/tokentax
- API Token 计费不能仅用“英文字符/非英文字符多少”统一折算；模型 tokenizer、语言/书写系统、输入输出内容、供应商定价和版本均不同。

### 竞争供给

- https://anri-lombard.github.io/tokentax ：`tokentax` 已实现 222 语言、多 Tokenizer、单段文本浏览器计算、近似成本估算和 CLI，根仓库代码 MIT，`README.md` 于本次从 GitHub 直接读取。
- https://geratools.com/cross-lingual-token-cost-comparison ：公开 20 种语言的词数倍率与成本比较，浏览器端实现。
- https://aiganak.com/language-token-tax/ ：提供 23 种语言的多模型计费实测示例及检查器（公布结果依赖其自有测量方法，未经本研究复核）。

### 停止判断

`TECHNICAL_PROBLEM=VERIFIED`；`MULTILINGUAL_SUPPLY=VERIFIED`；`USER_REPORTED_PAIN=LIMITED_SAMPLE`；`UNMET_NEED_AFTER_SUPPLY=NOT_VERIFIED`。

即使选用用户项目的 66 locales，现成竞争者已宣称覆盖 222 种语言；支持语言数量本身不是差异化或商用验证依据。不构建重复的 Token 计算器；除非有可重复的特定语言评估误差、具体商业用户需求以及可查询的独立搜索点击证据。

## 四、商业判定、停止线和后续方向

两任务分别真实，但“真实问题”未转化为“有足够独立价值且可获取搜索点击的广告网站”。本轮没有获取可信的可获得搜索点击、Google Search Console 查询对照、竞争者自然流量或页面 RPM。也没有独立进行广泛的语言市场比较。

对这两个任务都判 `PAUSE`，不是断言它们没有搜索量或没有收入。**不应马上再枚举大量新 AI 工具/教程以强行找出一个候选**。如果以后获得搜索点击、用户反复报道同一未解决工作流，或发现真正可复现的竞争功能错误，再围绕那个任务重新开启。

可以在未来使用已经拥有合法访问权的 GSC 数据，做用户实际到站查询与 AI 使用意图基线（要区分 go-dev 现有内容用户与新网站流量，不得把目前不存在的 AI 流量写成事实）；本轮没有访问 GSC，也没有发明数据。

许可证：此次比较是**独立产品/需求研究**，不是复制竞争者代码；若未来要复用某工具软件，必须另查具体许可证与素材条款，不可将项目开放代码许可直接推及网站内容。

```text
RESULT=PASS
STAGE=AI_USER_TASK_DEMAND_AND_SUPPLY_STOP_GATE
USER_TASKS=2
A_LOCAL_LLM_VRAM=PAUSED
B_MULTILINGUAL_TOKEN_COST=PAUSED
USER_PAIN_EVIDENCE=VERIFIED_IN_SAMPLE
EXISTING_SOLUTIONS=VERIFIED
UNMET_NEED_AFTER_SUPPLY=NOT_VERIFIED
SEARCH_VOLUME=UNKNOWN
ATTAINABLE_ORGANIC_CLICKS=UNKNOWN
AD_PAGE_RPM=UNKNOWN
LONG_TERM_AD_NET_PROFIT=UNKNOWN
FORMAL_AI_PROJECT_SELECTED=NO
SECOND_PROJECT=WORLD_HISTORY
RESEARCH_ONLY=YES
```
