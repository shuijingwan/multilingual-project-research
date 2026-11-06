# 第二翻译项目商业门槛调整与暂定方向 001

核实/决策记录日期：2026-11-06
阶段：SECOND_TRANSLATION_PROJECT_THRESHOLD_REVISION
状态：RESEARCH_ONLY
主项目：go-dev v2
第二正式项目：NOT_DECIDED
商业目标：LONG_TERM_AD_NET_PROFIT

## 一、决策背景

此前跨领域调查多次因新站可获取自然流量、AdSense RPM 和长期净收益均为 UNKNOWN 而暂停。此做法能够避免无证据的高成本投入，但当它演变为「第二项目必须在开发前证明具有与 go.dev 相近的流量与收入机会」时，容易形成无法跨越的过严门槛。

项目负责人于 2026-11-06 明确调整商业偏好：

- 第二个**翻译项目**不必复制 go.dev 的商业机会。
- 可以从现有已经研究的候选中选择。
- 相对 go.dev 较低的潜在收益与性价比可以接受。
- 这不是放弃长期广告净收益目标，也不意味着愿意接受无限维护成本。

本报告记录偏好变化，**不把研究顾问的推荐误写为项目负责人已批准 Rust 正式立项**。

## 二、正式调整：硬条件与软条件分离

### 不放松的硬条件

1. 拟复用的具体正文、代码、图片、数据商业权利边界清楚；UNCLEAR 的部分不直接复制翻译。
2. 独立网站能提供真实、可持续的用户价值，而不是仅为增加页面或语言数量。
3. AdSense 法规、搜索政策、商标以及必要署名和相同方式共享条款需要逐项符合。
4. 能力和工期允许控制持续维护成本，不影响 go-dev v2 的正常上线与运营。
5. 决定正式实施范围时设置时间/资源停止线，避免依赖尚未证实的收益长期扩大投入。

### 可以放宽的软条件

1. 不要求流量和广告收入与 go.dev 同等级。
2. 不要求在立项前取得精确新站流量、广告 RPM 或净利润预测；缺失继续标记 UNKNOWN。
3. 成熟竞争者存在不自动否决项目，但必须说明合法且有价值的服务方式。
4. 不要求在实施首期一次完成 66 个 locale；项目总目标范围及顺序仍固定为 66。
5. 官方链接收录可作为潜在优势，但不得假设其一定获批或能带来访问量。

降低收益预期并不等于把「仍可能长期亏损」当作已获许可的商业决定；必须限制风险敞口与机会成本。

## 三、现有翻译类候选复评（复用已归档研究，非新收益排名）

| 候选 | 已核实优势 | 主要阻碍 | 建议 |
| --- | --- | --- | --- |
| Rust 完整学习体系 | 六模块主要原始资料有较明确的商业授权基础；官方 Rust Book 社区译文列表有独立托管先例；工程经验可复用 | 多语言社区已有译文，升级维护成本，带广告链接收录态度 UNCLEAR | **暂定优先研究方向** |
| 世界历史三本开放教材 | 两本通史加一本非欧洲视角的合法正文来源；基础内容寿命较长 | 图片/地图权利需单独核查，历史准确性审核，独立流量未知 | **非技术方向主要备选** |
| OWASP Cheat Sheet Series | 正文 CC BY-SA 4.0 授权基础明确 | 安全更新与专业准确性要求高，同源社区译本已有部分覆盖 | 保留，暂不优先 |
| Python 官方文档 | PSF 许可证基础明确，搜索学习意图可识别 | 官方核心译本及成熟第三方教程竞争强 | 暂不优先 |
| Shopify、DeepSeek、Ethereum 全站/全套官方文档 | 专门开发者场景有用户价值 | 不同内容的商业翻译/独立托管授权仍有实质不确定性 | 不因门槛放宽而跳过版权限制 |

本比较是**风险与实施可行性判断**，不是广告收入、搜索量或利润预测。

现有具体参考：
- `research/2026-11-04-rst-full-ecosystem-license-and-coverage-gate-001.md`
- `research/2026-11-05-rst-search-competition-traffic-proxy-pilot-001.md`
- `research/2026-11-04-his-licensed-corpus-scope-gate-001.md`
- `research/2026-11-04-his-source-specific-translation-coverage-pilot-001.md`
- `research/2026-11-05-py-official-translation-coverage-and-search-intent-stop-pilot-001.md`
- `research/2026-11-05-owasp-search-demand-differentiation-stop-gate-001.md`

## 四、暂定下一项目的选择

研究顾问建议：

`PROVISIONAL_FRONT_RUNNER=RUST_FULL_LEARNING_PATH`

`STRONG_ALTERNATIVE=HIS_LICENSED_WORLD_HISTORY_CORPUS`

`PROVISIONAL_RECOMMENDATION_IS_USER_APPROVAL=NO`

选择 Rust 的依据不是已证明更高广告收益，而是具体来源商业授权、完整学习路径、工程复用和现有核查深度的组合。Rust 仍存在真实社区竞争与维护负担，必须诚实记录。

世界历史有低频更新的潜力（定性判断），但长篇历史教材的资料准确性审核、图片/地图许可证与搜索竞争不能忽略。不得预先认定技术领域在商业上胜过非技术领域。

## 五、实施与停止线

- 本报告**不批准现在启动正式 Rust 翻译或部署**。
- go-dev v2 的正常上线优先，任何第二项目不得修改它的仓库、配置和生命周期。
- 如果决定立项 Rust，先制定最小合法来源范围、先期语言范围、人工审核方法、可复用工程以及有限的时间/维护预算，再由负责人明确授权开发。
- 不为了做完整66语言而一次性启动完整六模块翻译。
- 现阶段避免再次进行广泛候选轮换、无限关键词查询和无法改变决策的重复 E3 门槛调查。

## 六、当前状态

`SELECTION_STANDARD=LOWER_RETURN_ACCEPTABLE_WITH_HARD_GUARDRAILS`

`COMMERCIAL_RANKING=NOT_READY`

`ATTAINABLE_ORGANIC_TRAFFIC=UNKNOWN`

`AD_PAGE_RPM=UNKNOWN`

`LONG_TERM_AD_NET_PROFIT=UNKNOWN`

`SECOND_PROJECT=NOT_DECIDED`

`FORMAL_PROJECT_SELECTED=NO`

`RESEARCH_ONLY=YES`

`NEXT=RUST_SECOND_PROJECT_SCOPE_AND_RESOURCE_STOP_DECISION`

下一步只围绕「如果选 Rust，如何限定第一期内容、工作量与退出条件」做简短可行性决策，不再要求先证明与 go.dev 相当的广告收入。研究结果可在后续正式项目选择前与世界历史备选比较。

不得启动翻译、建站、部署或修改 go-dev v2。
