# 第二多语言项目正式选择：世界历史（负责人决策）

记录日期：2026-11-06
阶段：SECOND_PROJECT_OWNER_SELECTION_DECISION
决策者：项目负责人
来源：2026-11-06 负责人明确指示
工作状态：RESEARCH_ONLY
主项目：go-dev v2（优先级不变）

**域名后续修订（2026-11-06）**：负责人明确选择项目域名标识 `world-history` 而不是 `history`；本报告所有规划主机名现已更新为该规则。项目选题与研究状态未变化。

## 一、明确的正式决定

**SECOND_PROJECT=WORLD_HISTORY（HIS）**

**FORMAL_PROJECT_SELECTED=YES**

已结束“世界历史只是有条件首选 / 第二项目尚未决定”的选择阶段。此前备选候选仍保留为未来项目研究池，而不是世界历史同期开工或当前第二项目竞争者。

这是项目**方向正式选择**，不是授权立即开始翻译、生产站开发、部署、购买域名或创建DNS。

- `PROJECT_DIRECTION_SELECTED=YES`
- `TRANSLATION_LAUNCH_AUTHORIZED=NO`
- `WEBSITE_BUILD_AUTHORIZED=NO`
- `DEPLOYMENT_AUTHORIZED=NO`
- `DNS_MUTATION_AUTHORIZED=NO`
- `RESEARCH_ONLY=YES`
- `GO_DEV_V2_PRIORITY=UNCHANGED`

此前历史性研究报告中的 `SECOND_PROJECT=NOT_DECIDED`，是对应报告生成时的状态；**本负责人决策是2026-11-06之后的当前权威状态**。不得回改不可变的历史证据结论。

## 二、项目内容与授权范围

初始源资料为此前已经研究的三本开放教材：

1. `World History: Cultures, States, and Societies to 1500`，University of North Georgia Press，正文CC BY-SA 4.0；原书12章。来源：https://oer.galileo.usg.edu/history-textbooks/2/
2. `World History Since 1500: An Open and Free Textbook`，ETSU，原出版页面正文CC BY 4.0；原书15章。来源：https://dc.etsu.edu/etsu-oer/13/
3. `History of International Relations: A Non-European Perspective`，Open Book Publishers，正文CC BY 4.0。来源：https://www.openbookpublishers.com/books/10.11647/obp.0074

三书构成世界历史项目拟采用的第一轮学习内容源，不表示无需后续源版本冻结、第三方素材审核或课程路径整理。

内容策略继续采用 `LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS`：
- 商业翻译权利明确的**具体正文与素材**，遵守许可证条件后允许纳入未来内容白名单。
- 图片、地图、引文、图表若有独立第三方授权或禁止商业修改/再分发要求，需逐项核对；不允许的素材不复制，保持来源链接或未来另寻合法替代。
- 不需要一律丢弃原图；也不能因为教材正文采用CC BY/CC BY-SA就自动重用全部图片。
- 不要求取得整站全素材授权，不要求原创补齐未获授权内容。

当前项目是否适合AdSense、实际自然搜索流量、RPM和长期广告净收益仍为 `UNKNOWN`，本决策并未把收益预测当作已证明事实。

## 三、locale 及域名：与 go-dev 现有生产命名完全一致（项目名 world-history）

负责人再次决定：

**世界历史沿用 go-dev 的每 locale 独立子域名方式，并且域名里的 locale 标识/前缀与 go-dev 完全一致。**

权威来源（只读，绝不修改 Go 仓库）：
- `shuijingwan/go-tour-i18n`
- `production/identity.json`，main，2026-11-06 读取
- 源 JSON Git blob SHA：`585ae11543b47cbc1b03908896acb4372a1ae958`
- 该文件包含 **65 个正式 live locale 的production_hostname**，与独立研究仓库目标66 locale的额外`en-US`不同。
- 跨项目目标66及顺序仍引用 `docs/LOCALE_ROADMAP.md`（源commit `a929f2bef34be37c6e1860021bd581f8ec54d094`，blob `0787dca237a443f2ef5c8aefd2c2a1d609c6cbb9`），及 `research/2026-11-03-target-locales-source-snapshot.md`，不得建立第二套独立locale authority。

**域名构造正式决定（2026-11-06 后续修订）**：在对应 Go production hostname 中只将主机标签部分的 `go-dev` 替换为 `world-history`，保留原来全部 locale 前缀、拼写、大小写规范化与地域差异；这是一项**计划命名规则**，不是已经创建或解析的DNS记录。

举例：
| Canonical locale | 已存在 Go production hostname | 历史项目规划hostname |
|---|---|---|
| zh-CN | `go-dev.shuijingwanwq.com` | `world-history.shuijingwanwq.com` |
| ja-JP | `ja-go-dev.shuijingwanwq.com` | `ja-world-history.shuijingwanwq.com` |
| de-DE | `de-go-dev.shuijingwanwq.com` | `de-world-history.shuijingwanwq.com` |
| fr-FR | `fr-go-dev.shuijingwanwq.com` | `fr-world-history.shuijingwanwq.com` |
| de-AT | `de-at-go-dev.shuijingwanwq.com` | `de-at-world-history.shuijingwanwq.com` |
| zh-TW | `zh-tw-go-dev.shuijingwanwq.com` | `zh-tw-world-history.shuijingwanwq.com` |
| es-419 | `es-419-go-dev.shuijingwanwq.com` | `es-419-world-history.shuijingwanwq.com` |
| en-GB | `en-gb-go-dev.shuijingwanwq.com` | `en-gb-world-history.shuijingwanwq.com`（是否需区域英文新译另审） |
| ar | `ar-go-dev.shuijingwanwq.com` | `ar-world-history.shuijingwanwq.com` |

**重要**：Canonical locale `ja-JP`、`de-DE` 等不应误生成 `ja-jp-world-history`、`de-de-world-history`。以 Go 的生产主机名为准，不是简单拼接完整 BCP47 locale。`history` 不再是本项目域名标识。

- Go 项目`zh-CN`实际不带`zh-cn-`前缀，世界历史项目对应无前缀的`world-history`。不擅自另加`zh-cn-`。
- `en-US` 是66目标范围中特有的额外locale，**Go无对应生产hostname**。三本原始书主要为英文来源；`en-US`与其他英语区域是否视为已经被原始英文有效覆盖，需后续按项目原始语言内容范围确定。不能伪称Go已有en-US域名，不因该例外而改写65个生产locale映射。
- 若未来 Go 生产 hostname authority 更新，正式建站前只读重新读取来源并检查差异；不得把本报告当成新的Go hostname registry。

三本教材在**同一语言**共享同一个历史域名，通过URL路径区分教材，不建立每本书单独子域名。

## 四、DNS与费用边界

2026-11-06 Cloudflare截图显示87/200条DNS记录。如果未来在同一DNS zone新增66个locale的独立A/CNAME记录且其他记录不变，预计153/200；这只是条件容量假设，不是实际新增记录。实际需翻译及部署语言数量尚须依据来源英文有效覆盖核定。

负责人已明确决定**继续使用Cloudflare免费版直到记录不足时再考虑解决支付/升级方式**。

不使用未经批准的通配符替换现有站点DNS，不修改go-dev现有记录，不提前购买新DNS配额。

## 五、已正式确定与尚未授权事项的边界

**确定**：
- 第二项目方向＝世界历史（HIS）。
- 拟从三本已研究开放教材开始制定合法源与学习路径。
- 与go-dev每语言子域名相同的locale前缀。
- 同语言三教材共用主机名。
- 主项目go-dev v2优先。
- 研究成果进入公开GitHub仓库。

**尚未批准**：
- 任何正式翻译。
- 任何站点代码开发、生产环境初始化、广告接入或部署。
- 任何DNS创建、更改、费用支出。
- 三本书正文/图片全部直接商业发布。
- 66目标所有locale同时生成/上线。

## 六、唯一下一步

`NEXT=HIS_SOURCE_AND_MEDIA_LICENSED_SCOPE_FREEZE_RESEARCH`

仅在 `RESEARCH_ONLY` 范围内，对三书的**具体出版版本、正文及图片/地图授权资产清单**制定最小可实施范围和审校/维护停止线。无需开展已完成的全候选重新排名，也无需现在开始翻译/网站建设。等go-dev v2不受影响且负责人明确批准后，再考虑正式实施。

## 七、决策结论

`RESULT=PASS`
`STAGE=SECOND_PROJECT_OWNER_SELECTION_DECISION`
`SECOND_PROJECT=WORLD_HISTORY`
`HIS_PROJECT_SELECTED=YES`
`FORMAL_PROJECT_SELECTED=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`ARCHITECTURE=PER_LOCALE_SUBDOMAIN`
`DOMAIN_LOCALE_NAMING=EXACT_GO_DEV_PRODUCTION_HOST_PREFIX`
`PROJECT_DOMAIN_SLUG=world-history`
`DOMAIN_SUFFIX_REPLACEMENT=go-dev_TO_world-history`
`GO_DEV_PRODUCTION_LOCALE_MAPPINGS=65`
`EN_US_GO_DEV_PRODUCTION_IDENTITY=NONE`
`THREE_HISTORY_BOOKS_SHARE_LOCALE_HOST=YES`
`CLOUDFLARE_PLAN=FREE_FOR_NOW`
`GO_DEV_MUTATION=NONE`
`RESEARCH_ONLY=YES`
`NEXT=HIS_SOURCE_AND_MEDIA_LICENSED_SCOPE_FREEZE_RESEARCH`
