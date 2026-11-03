# 具体目标语言与内容机会清单 001

核实日期：2026-11-03
状态：RESEARCH_ONLY
正式立项：NOT_DECIDED
清单性质：进一步调查对象，不是商业排名

## 一、固定商业边界

最终目标：长期合法广告净收益。

前期主要代理指标：
独立站可获取的长期自然搜索流量。

目标范围：66个locale。
Google广告支持：62个locale。
既定语言顺序不变。

RPM与净收益缺少证据时保持UNKNOWN。

不因语言没有进入官方目录，
就认定其不存在第三方内容。

## 二、候选A：国家与首都知识工具

目标：id-ID、vi-VN

可能产品：
国家与首都资料查询、记忆练习、
地图知识及必要的数据比较。

授权证据：

Natural Earth公共领域地图数据：
https://www.naturalearthdata.com/about/terms-of-use/

Wikidata结构化数据CC0：
https://www.wikidata.org/wiki/Wikidata:Licensing

状态：VERIFIED（限定上述数据范围）。

已有竞争：
https://www.dodothinks.online/id/
https://flagquizzes.com/vi/capitals/world/

德国相关知识搜索兴趣已得到观察，
但不能直接转用为印尼或越南市场需求。

目标市场需求：UNKNOWN。
实质功能缺口：UNKNOWN。
工程成本：UNKNOWN。

下一步：
验证当地具体搜索意图和现有工具功能。
若没有显著未满足的需求，暂缓。

## 三、候选B：非欧洲视角历史教材

目标：vi-VN、hi-IN

具体来源：
History of International Relations:
A Non-European Perspective

出版社：
https://www.openbookpublishers.com/books/10.11647/obp.0074

正文授权：
CC BY 4.0，允许符合条件的商业改编。

部分插图或第三方素材可能另有许可。

越南高校资料库：
https://oerrepository.ntt.edu.vn/handle/298300331/703

该馆藏记录语言为英语。
不能把馆藏记录当作越南语译本。

历史知识需求存在跨领域研究线索，
但本书的目标语言搜索需求：UNKNOWN。

目标语言有效译本覆盖：UNKNOWN。
单本教材可获取流量：UNKNOWN。

下一步：
核查越南语、印地语现有译本，
以及对应章节主题的长期搜索需求。

没有足够需求则暂缓完整翻译。

## 四、候选C：Shopify Liquid参考

目标：id-ID

限定内容源：
https://github.com/Shopify/theme-liquid-docs

该仓库采用MIT许可证。

商业使用许可仅适用于
实际获得许可的仓库内容。

不得推导整个shopify.dev
均可商业转载或翻译。

已有源文件清点：
research/2026-11-03-shopify-liquid-inventory.md

目标语言搜索需求：UNKNOWN。
有效本地化参考覆盖：UNKNOWN。
官方文档竞争：需要深入调查。
持续维护成本：UNKNOWN。

下一步：
验证印尼开发者的Liquid参考查询需求。
若需求不明显，暂缓。

## 五、候选D：Rust完整学习路径

目标：id-ID

Rust Book官方目录：
https://doc.rust-lang.org/book/appendix-06-translation.html

官方目录未列出印尼语，
但已经找到实际社区项目：

https://github.com/rustid/book-id
https://github.com/renomureza/rust-book-id
https://github.com/evilfactorylabs/belajar-rust

因此不得把印尼语Rust列为翻译空白。

需要核查：
- Book实际完成度和更新版本
- Rust By Example等其他学习模块
- Cargo及Reference等文档覆盖
- 搜索需求及竞争难度
- 不同仓库的许可证与长期维护成本

有效内容缺口：UNKNOWN。
可获取自然流量：UNKNOWN。

当前不优先重复翻译Rust Book。

## 六、其他保留候选

OWASP：
CC BY-SA 4.0源资料具有研究价值，
但安全修正及长期审校成本较高。
等需求和维护证据更明确后再深入。

Python：
官方部分语言覆盖率较低，
但翻译体系已经成熟。
需评估官方后续补齐风险。

Ethereum：
已有官方本地化内容入口。
没有证明差异化价值前，
不建议重复翻译官方基础文档。

其他历史、AI和开放数据方向：
继续保留探索资格，不机械淘汰。

## 七、跨领域结论

本轮没有确定任何一个
商业价值已得到验证的供给缺口。

以上候选都需要进一步证明：
1. 目标语言存在实际搜索需求。
2. 现有内容不能充分满足需求。
3. 新网站能够提供实质性额外价值。
4. 商业授权明确。
5. 更新及运营成本合理。
6. 有机会形成长期可变现流量。

不得根据候选排列顺序
推断预计广告收入或建设优先级。

## 八、研究停止线与下一阶段

下一阶段：
GEO_VI_EFFECTIVE_GAP_VERIFICATION

仅选择一个明确组合：
vi-VN × 国家与首都查询及练习。

调查具体越南语搜索表达、
现有产品功能和潜在差异化。

这只是下一项研究任务，
不是正式项目选择。

若无明显需求或功能缺口，
及时停止，不启动开发。

维持RESEARCH_ONLY。
不翻译、不建站、不部署。
不修改go-dev v2。
