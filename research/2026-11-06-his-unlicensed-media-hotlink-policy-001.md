# 世界历史商业翻译站：未授权图片热链接与普通外链处理规则 001

核实日期：2026-11-06
阶段：HIS_UNLICENSED_MEDIA_HOTLINK_POLICY
项目：WORLD_HISTORY（第二项目已正式选定）
执行状态：RESEARCH_ONLY
项目域名：world-history，locale沿用go-dev生产命名前缀

## 一、研究问题

项目负责人询问：如果原教材图片、地图、第三方素材没有获得明确商业使用许可，是否可不将文件存放在本站服务器，而在HTML中直接引用原开源教材/出版方的图片URL，作为页面内图片显示？

本报告明确区分三种行为：

1. **本地复制与托管**：从原站下载图像后发布到本站。
2. **热链接/行内嵌入（hotlink）**：使用`<img src="https://出版社域名/图片.jpg">`或同类技术，让访问者浏览器从原站读取、但在本站页面中展示。
3. **普通链接（normal hyperlink）**：`<a href="https://出版社原始页面">查看原图及来源</a>`，用户主动打开原出处；本站不行内展示受限制图像。

### 正式研究结论

**图片不保存在自己服务器上，不会自动使该图片获得商业嵌入或公开展示的权利。**

不过，也**不能一概断言所有跨域图片嵌入必然构成版权侵权**。各司法辖区对第三方内容嵌入的特定行为、许可及其他权利分析并不相同，需要结合具体场景。

美国第九巡回上诉法院判例`Hunley v. Instagram, LLC`（2023-07-17）适用基于`Perfect 10`的Server Test，在相关事实下认定被告的第三方图片嵌入不构成直接侵犯展示权；该结论不能直接扩展为全球任何未授权素材都可以在商业站中热链接：
https://law.justia.com/cases/federal/appellate-courts/ca9/22-15293/22-15293-2023-07-17.html

欧盟法院`VG Bild-Kunst, C-392/19`（2021-03-09）说明绕过权利人设置或要求的有效防嵌入技术措施所进行的framing，可能构成需经许可的向公众传播：
https://infocuria.curia.europa.eu/tabs/redirect/juris/liste.jsf?num=C-392%2F19

本报告不是对具体国家、案件的法律意见；全球66-locale、商业广告运营必须采取可执行的低风险政策。

## 二、实际网站运营风险

即使在某些法域某种嵌入可能不构成特定版权侵权，也不等于原站明确允许：

- 原站服务条款可能限制第三方嵌入、热点引用或带宽滥用。
- 原站可能启用防盗链，导致图片失效，变更资源路径，或替换内容。
- 网站无法稳定控制远端文件的长期可访问性、版本与内容完整性。
- 加载远程图片会向第三方暴露访问请求相关信息；实际是否有其他合规风险须结合网站情况评估。
- 外站提供官方嵌入代码并不必然涵盖源图所有版权，仍须按具体许可和使用条件判断。

Cloudflare公开的Hotlink Protection文档确认，原站可按HTTP Referer来源拒绝来自其他网站的图片请求：
https://developers.cloudflare.com/waf/tools/scrape-shield/hotlink-protection/

## 三、针对世界历史三书的推荐决策

**商业图片/地图使用的默认顺序**：

1. `VERIFIED_REUSABLE`：具体素材已确认公有领域、CC0、适用的CC BY/CC BY-SA或其他允许本站相应商业用途的许可；记录原文件与许可、作者、链接及必要修改说明。优先合法自托管，保证稳定性、缓存与多语言复用。若许可证只允许原样使用、不允许改编，则不得翻译原图内部文字。
2. `REPLACE`：原图无法获知或未获允许再利用，寻找有明确授权的等效图片/地图，记录替代出处，独立核实权利。
3. `LINK_ORIGINAL_PAGE_ONLY`：未确认复制或嵌入权利、没有适当替代，正文可给出清晰的普通超链接，指向出版社承载图片及署名的**原始页面**，不以`<img>`、iframe、CSS背景图或后台代理的方式在本站内显示。
4. `OMIT`：无法保证链接稳定或素材对正文非必要，保留合适文字说明并省略图片。

**特殊情况**：如果原站明确提供允许第三方在商业站点嵌入的许可证或具体嵌入授权，可按其条款另行评估`AUTHORIZED_EMBED`；需要可留存证据、遵守来源署名及限制，不等同于任何原站图片都能热链接。

项目默认规则：
`UNCLEAR_MEDIA_DEFAULT=LINK_ORIGINAL_PAGE_ONLY_OR_OMIT`
`UNCLEAR_MEDIA_INLINE_EMBED=NO`
`HOTLINK_IS_LICENSE_SUBSTITUTE=NO`
`AUTHORIZED_EMBED_PER_ITEM_REVIEW=YES`
`LICENSED_MEDIA_SELF_HOSTING_PREFERRED=YES`
`SOURCE_PAGE_LINK_ALLOWED_AS_DEFAULT_NAVIGATION=YES`

### 对具体源的指导

- **HIS-A**：约350幅图片和地图的出版社描述不能当作全部已授权。作者许可明确的地图可做许可列表，其他素材分项判断。
- **HIS-B**：某图标注出版社购买iStock标准许可，不等于本站获得许可。此图不应被“热链接”绕过，优先普通链接到原书页面或替换为合法作品。
- **HIS-C**：结合List of Illustrations逐项核对，不能因为正文CC BY直接嵌入全部图像。

## 四、同“LICENSED_TRANSLATION_PLUS_OFFICIAL_LINKS”政策的关系

此处`OFFICIAL_LINKS`特指让用户点击访问官方原始页面的**普通跳转链接**。

它**不自动包含**使用原出版社的图像地址在本站直接显示，也不等于许可复制、iframe镜像、Cloudflare Workers反向代理图片、CDN中转、图片缓存或缩略图重新发布。

即使“技术上不在自己服务器保存图片”，也不允许将其归为`LICENSED`内容并进入未来出版白名单。

## 五、实际状态、后续工作与停止线

当前不建立独立图像托管或导入系统，不批量抓图，不创建链接抓取工具，不修改Go项目或DNS，不开始66-locale正式翻译。

将本策略作为前驱：
`research/2026-11-06-his-source-and-media-licensed-scope-freeze-research-001.md`

真正下一步仍然为：
`NEXT=HIS_EDITION_HASH_AND_MEDIA_MINIMAL_SAMPLE_PILOT`

该阶段只抽样核实具体源版本和重要图片权利，分别计算可用、自有权利、须替换/链接与不明数量，不用热链接人为提高“可使用图片比例”。

## 六、结论

`RESULT=PASS`
`STAGE=HIS_UNLICENSED_MEDIA_HOTLINK_POLICY`
`SECOND_PROJECT=WORLD_HISTORY`
`FORMAL_PROJECT_SELECTED=YES`
`UNCLEAR_MEDIA_INLINE_EMBED=NO`
`UNLICENSED_MEDIA_ACTION=LINK_ORIGINAL_PAGE_ONLY_OR_OMIT`
`HOTLINK_NOT_SUBSTITUTE_FOR_LICENSE=YES`
`RESEARCH_ONLY=YES`
`PROJECT_LAUNCH_AUTHORIZED=NO`
`GO_DEV_MUTATION=NONE`
`NEXT=HIS_EDITION_HASH_AND_MEDIA_MINIMAL_SAMPLE_PILOT`
