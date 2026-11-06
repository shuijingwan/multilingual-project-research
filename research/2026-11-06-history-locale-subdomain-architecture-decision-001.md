# 世界历史候选项目：延续 go-dev 的每语言子域名架构

> **后续正式决策覆盖旧示例（2026-11-06）**：负责人已将历史项目域名标识从 `history` 确定为 `world-history`。本文件前文的 `*-history` 例子均为历史记录，**不可用于新建DNS或生成域名**。当前有效规则参见本文件第七节及 `research/2026-11-06-second-project-world-history-owner-selection-001.md`。

日期：2026-11-06
阶段：HIS_LOCALE_SUBDOMAIN_ARCHITECTURE_DECISION
项目状态：RESEARCH_ONLY
第二项目：NOT_DECIDED
正式建设授权：NO

## 一、负责人明确选择

延续 go-dev 的部署与 URL 思路：**每个目标 locale 使用独立的子域名**。

如果未来选择世界历史项目，同一 locale 下的三本历史教材**共用该 locale 子域名**，通过站内路径划分教材，而不是每本教材再单独使用一个域名。

命名仅作示例（不是已批准、已注册或已部署的主机名）：

- `zh-cn-history.shuijingwanwq.com/world-history-to-1500/`
- `zh-cn-history.shuijingwanwq.com/world-history-since-1500/`
- `zh-cn-history.shuijingwanwq.com/international-relations/`
- `de-de-history.shuijingwanwq.com/world-history-to-1500/`

具体主机名、locale 映射、路径风格须在正式立项后独立决定；**沿用项目既有冻结66-locale范围及顺序**。不得由本记录推定全部66个站点必须一次性上线。

## 二、Cloudflare 免费区配额规划

2026-11-06，项目负责人提供的 Cloudflare 截图显示：

`CURRENT_DNS_RECORDS=87`
`FREE_DNS_RECORD_LIMIT=200`
`CURRENT_REMAINING_RECORD_SLOTS=113`

如果将来在**同一个 Cloudflare DNS zone** 中按66个locale新增66条独立记录，且期间其他记录总数不变，则：

`PROJECTED_RECORDS=153`
`PROJECTED_REMAINING=47`

这是条件算术规划，不是已经新增66条 DNS，也不能保证之后其他项目始终有配额。

当现有免费DNS记录容量不足时，**再解决升级付费方式或其他适用方案**；目前不因为预期未来上限而改变已选择的每语言子域名结构。

不应把“后续考虑付费”解释为已经决定购买任何 Cloudflare 付费产品，也不应未经核对就假设升级付费一定可以解决所有 DNS/证书问题。

## 三、独立于域名数量的内容组织

- 每个语言站点提供统一历史学习导航，包含三本教材的合法可译资料及未授权内容的官方外链。
- 每本教材独立保存原书来源、版本、许可证、署名、修改说明和媒体资产授权记录。
- 可共享部署代码、静态资源生成能力、术语与审校流程，但不同 locale 保持独立 URL。
- 未来上线应按跨域名实际 URL 配置导航、站点地图、规范地址、hreflang、缓存和监控。
- 图片素材授权不因跨语言共享而自动变化；具体改编和图片中文字本地化仍须遵守对应许可。

## 四、不在本轮执行的操作

- 不新增、删除或修改 DNS 记录。
- 不部署任何历史网站或购买域名。
- 不改 go-dev 源码、配置、域名和运行环境。
- 不启动翻译、不建设正式生产内容站。
- 不修改此前的第二项目正式选择状态。

## 五、状态与下一步

`ARCHITECTURE_PREFERENCE=PER_LOCALE_SUBDOMAIN`
`THREE_HISTORY_BOOKS_SHARE_LOCALE_HOST=YES`
`SUBDIRECTORY_FOR_ALL_LOCALES=REJECTED_AS_CURRENT_PREFERENCE`
`CLOUDFLARE_PLAN=FREE_FOR_NOW`
`UPGRADE_PAYMENT_SOLUTION=DEFER_UNTIL_NEEDED`
`DNS_MUTATION=NONE`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`SECOND_PROJECT=NOT_DECIDED`
`RESEARCH_ONLY=YES`
`NEXT=SECOND_PROJECT_OWNER_SELECTION_DECISION`

本记录只是可复用架构约束，不将历史候选误写为正式立项。

## 六、后续负责人正式选择与域名 locale 纠正（2026-11-06）

**本节为后续正式负责人决策；与上文示例或状态冲突时，以本节为准。**

权威决策：`research/2026-11-06-second-project-world-history-owner-selection-001.md`。

- `SECOND_PROJECT=WORLD_HISTORY`，`FORMAL_PROJECT_SELECTED=YES`：世界历史已由项目负责人正式选定，不再是尚未决定的备选。
- 域名locale前缀必须与Go正式生产映射**完全一致**；不是把完整locale码转成小写后直接拼到`-history`。
- 来源为`shuijingwan/go-tour-i18n/production/identity.json`中65个已发布`production_hostname`；只在域名中把`go-dev`标签替换成`history`。
- 因此：`zh-CN`由`go-dev.shuijingwanwq.com`对应`history.shuijingwanwq.com`，**不是**前文仅作假设的`zh-cn-history.shuijingwanwq.com`。
- `de-DE`由`de-go-dev.shuijingwanwq.com`对应`de-history.shuijingwanwq.com`，**不是**`de-de-history.shuijingwanwq.com`。
- `de-AT`对应`de-at-history.shuijingwanwq.com`；`es-419`对应`es-419-history.shuijingwanwq.com`。
- `en-US`是跨项目第66个目标而不是Go现有生产locale，不能臆造其Go正式hostname；历史教材原文是英语，具体英文地区是否需另建站点留在实施前的内容覆盖决策。
- 三本教材继续**共用同一locale历史域名**，通过路径区分。
- 本次仅研究和决策：`RESEARCH_ONLY=YES`，`PROJECT_LAUNCH_AUTHORIZED=NO`，`DNS_MUTATION=NONE`，不修改go-dev。

`NEXT=HIS_SOURCE_AND_MEDIA_LICENSED_SCOPE_FREEZE_RESEARCH`

## 七、当前生效的项目域名标识：world-history（负责人后续决策）

负责人明确选定第二项目`WORLD_HISTORY`，并进一步决定：

- 项目标识 `PROJECT_DOMAIN_SLUG=world-history`，**不再使用**原来的 `history`。
- 从 Go 的65个正式生产主机名逐项派生，只将主机名中的 `go-dev` 替换为 `world-history`，保留其余locale前缀及区域变体原样。例如：
  - `go-dev.shuijingwanwq.com` → `world-history.shuijingwanwq.com`（zh-CN）；
  - `ja-go-dev.shuijingwanwq.com` → `ja-world-history.shuijingwanwq.com`（ja-JP）；
  - `de-go-dev.shuijingwanwq.com` → `de-world-history.shuijingwanwq.com`（de-DE）；
  - `de-at-go-dev.shuijingwanwq.com` → `de-at-world-history.shuijingwanwq.com`（de-AT）；
  - `es-419-go-dev.shuijingwanwq.com` → `es-419-world-history.shuijingwanwq.com`（es-419）。
- 三本历史教材在同一语言对应子域名下共存，以路径区分；以后新增世界历史同源内容可按独立决策纳入该项目，其他历史专项不自动混入。
- `en-US` 是跨项目66目标之一，Go无对应生产hostname；历史英语原版是否构成官方有效支持，另行研究，**不得伪造Go的en-US域名身份**。
- 本文件此前 `zh-cn-history`、`de-de-history` 和 `*-history` 示例均属**被取代的历史建议**；最终域名清单以第七节规则和正式选题决策为准。
- 当前仍是 `RESEARCH_ONLY`；未创建DNS记录，不修改go-dev，也未授权建站/翻译。

`SECOND_PROJECT=WORLD_HISTORY`
`FORMAL_PROJECT_SELECTED=YES`
`PROJECT_DOMAIN_SLUG=world-history`
`DOMAIN_LOCALE_NAMING=EXACT_GO_DEV_PRODUCTION_HOST_PREFIX`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`DNS_MUTATION=NONE`
`NEXT=HIS_SOURCE_AND_MEDIA_LICENSED_SCOPE_FREEZE_RESEARCH`
