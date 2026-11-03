# 第一批跨渠道内容源发现

日期：2026-11-03
阶段：SOURCE_DISCOVERY
项目状态：RESEARCH_ONLY

## 一、目的

从已确认的内容发现渠道寻找具体内容源。

本轮只记录发现结果及许可证线索，
不进行商业排名，不确定开发项目。

固定研究范围为 66 门语言。

本轮未完成：
- 66 门语言覆盖调查
- 完整版权与第三方素材审核
- 自然搜索需求调查
- 广告 RPM 与收益评估
- 长期维护成本量化

上述项目均保持 UNKNOWN 或 UNCLEAR。

## 二、已发现内容源

### 1. The Rustonomicon

渠道：GitHub
领域：Rust 进阶编程

来源：
https://github.com/rust-lang/nomicon

许可证线索：MIT OR Apache-2.0

主要内容：
Unsafe Rust、内存安全及进阶知识。

注意：
官方明确提示该文档仍不完整。

现有翻译竞争：UNKNOWN
商业可行性：UNKNOWN

状态：DISCOVERED

### 2. OWASP Cheat Sheet Series

渠道：GitHub
领域：应用安全

来源：
https://github.com/OWASP/CheatSheetSeries

许可证线索：CC BY-SA 4.0

主要内容：
应用安全最佳实践及开发参考资料。

需要核实：
- 现有多语言覆盖
- 资料持续更新频率
- 具体文件和素材许可
- 官方多语言替代风险

状态：DISCOVERED

### 3. History of International Relations

渠道：Open Textbook Library
领域：世界历史、国际关系

出版社：
https://www.openbookpublishers.com/books/10.11647/obp.0074

许可证线索：CC BY 4.0

出版社已明确标示正文许可证。
部分图片授权另有规定。

提供多种电子书格式。

现有多语言竞争：UNKNOWN
商业搜索需求：UNKNOWN

状态：DISCOVERED

### 4. World History: Cultures, States,
### and Societies to 1500

渠道：Open Textbook Library
领域：世界历史

来源：
https://open.umn.edu/opentextbooks/textbooks/world-history-cultures-states-and-societies-to-1500

许可证线索：
CC BY-SA 4.0，存在素材例外。

需要核实：
- 原出版版本与授权
- 地图及图片权限
- 现有多语言版本
- 搜索竞争与维护成本

状态：DISCOVERED

### 5. Ethics and Artificial Intelligence

渠道：Pressbooks Directory
领域：人工智能伦理

目录：
https://directory.pressbooks.pub/

作者：Joel Gladd

目录许可证线索：CC BY

注意：
目前仅完成目录层面的发现。
尚需确认原出版页的许可声明。

现有多语言竞争：UNKNOWN
长期流量机会：UNKNOWN

状态：DISCOVERED

## 三、授权元数据风险

发现渠道标注的许可证，
可能与内容发布者当前版本不同。

例如：

Open Textbook Library 部分 OpenStax
历史教材条目仍显示 CC BY。

OpenStax 当前网站则对部分内容
采用 CC BY-NC-SA 授权。

OpenStax 说明：
既有 CC BY 版本可继续遵循原许可，
但必须确认实际使用的具体版本。

参考：
https://help.openstax.org/s/article/Openstax-textbook-licensing-and-customization

因此，必须记录：
- 来源版本
- 原出版社许可
- 授权核实日期
- 第三方素材例外

## 四、渠道覆盖情况

GitHub：已发现具体内容源
Open Textbook Library：已发现具体内容源
Pressbooks Directory：已发现具体内容源
OER Commons：保留渠道，待继续发现

其余补充渠道与专项数据来源
不在本批次调查范围。

不为达到候选数量而强行补充。

## 五、阶段结论

发现 5 个待进一步核查的内容源。

本轮没有商业立项结论。

下一阶段：
核实具体内容版权、现有多语言覆盖、
上游替代风险以及内容规模。

不得因许可证宽松而直接启动翻译。

保持 RESEARCH_ONLY。
不修改 go-dev v2。

## 六、Rust 学习路径与 OWASP 维护策略修订

核实日期：2026-11-03

### 6.1 Rust 应作为完整学习体系研究

此前发现 Rustonomicon，仅代表找到一个符合
初步授权条件的内容源，不代表优先选择高级教程。

正式研究对象调整为：

Rust Official Learning & Documentation

需要覆盖的学习层次：

1. 入门：The Rust Programming Language
2. 基础实践：Rust By Example、Rustlings
3. 进阶：Cargo Book、Rust Reference
4. 高级：Rustonomicon

主要来源：
https://rust-lang.org/documentation
https://github.com/rust-lang/book
https://github.com/rust-lang/rust-by-example
https://github.com/rust-lang/rustlings
https://github.com/rust-lang/nomicon

现有社区译本不能直接作为淘汰理由。

需要按具体语言、文档模块、翻译范围、
质量和更新状态评估有效覆盖。

不同仓库的许可证及第三方素材需要分别核实。

Rustlings 的交互练习具有额外工程成本，
不得将其视为普通静态文档翻译。

### 6.2 OWASP 官方权威性属于潜在优势

OWASP Cheat Sheet Series 具有官方权威性、
可获取的 Markdown 内容及明确的 CC BY-SA 4.0 许可。

如果目标语言缺少高质量完整译本，
独立多语言站点可能提供实际用户价值。

但不得假定独立站点自动继承官方搜索排名、
外部链接或品牌授权。

官方资料：
https://owasp.org/projects/cheat-sheet-series
https://github.com/OWASP/CheatSheetSeries

### 6.3 OWASP 更新策略

建议的初步维护机制：

- 每月：轻量检查上游变更。
- 每季度或半年：处理普通内容更新。
- 重大安全修正：发现后优先处理。
- 每半年：完成一次系统范围复核。

这是研究建议，不是官方更新承诺。

后续需要实际核实：
- 原始文档的更新频率。
- 每次变更涉及的文章比例。
- 安全修正的紧急程度。
- 66 门语言的翻译与审核成本。
- 上游多语言覆盖情况。
- 用户需求和广告商业可行性。

维护成本、流量与广告收益仍为 UNKNOWN。

### 6.4 阶段结论

Rust 从单一高级教材候选，
提升为完整官方学习体系研究对象。

OWASP 保留为重点技术文档候选，
不能因持续更新需求而直接淘汰。

这不是正式立项或开发授权。

研究状态继续保持 RESEARCH_ONLY。
