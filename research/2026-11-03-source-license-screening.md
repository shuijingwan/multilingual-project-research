# 第一批具体内容源：商业授权与上游替代风险调查

核实日期：2026-11-03
状态：RESEARCH_ONLY
语言范围：既定 66 门语言

## 一、结论

本次只调查具体内容来源。

具有开放许可证不代表适合建立商业翻译站。

如果官方已经建立成熟多语言体系，
应降低项目优先级，并调查未来替代风险。

本次未完成 66 门语言的逐项覆盖核查。
所有流量、RPM 和广告净收益均为 UNKNOWN。

## 二、具体来源

### 1. Rust Book

来源：
https://github.com/rust-lang/book

授权：VERIFIED
MIT / Apache-2.0。

已存在社区翻译：VERIFIED。

66 门语言完整覆盖：UNKNOWN。

结论：继续调查，不启动翻译。

### 2. Dive into Deep Learning

来源：
https://github.com/d2l-ai/d2l-en

授权：VERIFIED
教材 CC BY-SA 4.0。
示例代码采用单独的许可证。

已有中文及其他语言翻译：VERIFIED。

完整语言覆盖：UNKNOWN。

结论：上游替代风险较高，降低优先级。

### 3. Google Machine Learning Crash Course

来源：
https://developers.google.com/machine-learning/crash-course

授权：
Google Developers 通用政策支持
符合 CC BY 4.0 条件的页面商业改编。

完整课程及独立媒体授权：UNCLEAR。

官方已有阿拉伯语、法语、
印尼语等实际翻译页面：VERIFIED。

66 门语言及各章节完整覆盖：UNKNOWN。

结论：官方多语言能力较成熟，暂缓。

### 4. Google Machine Learning Glossary

来源：
https://developers.google.com/machine-learning/glossary

页面文字授权：VERIFIED
CC BY 4.0。

页面代码授权：VERIFIED
Apache-2.0。

已有官方多语言入口：VERIFIED。
各语言内容完整性：UNKNOWN。

结论：暂缓重复翻译。

### 5. DeepSeek-R1

来源：
https://github.com/deepseek-ai/DeepSeek-R1

仓库授权：VERIFIED
MIT。

模型权重需区分具体模型及底座许可证。

整个 API 官方网站授权：UNCLEAR。

海外 API 文档本地化搜索需求：UNKNOWN。

结论：
保留仓库内许可覆盖的技术文档候选。
继续核实 API 文档授权及市场需求。

### 6. Shopify Theme Liquid Docs

来源：
https://github.com/Shopify/theme-liquid-docs

仓库授权：VERIFIED
MIT。

整个 shopify.dev/docs 的授权：
UNCLEAR，不得由仓库许可证推导。

上游多语言覆盖：UNKNOWN。

结论：
保留 Liquid 参考资料候选。
暂缓 Shopify 官方文档整站翻译。

### 7. OpenStax World History

来源：
https://openstax.org/books/world-history-volume-1/pages/preface

教材授权：VERIFIED
CC BY-NC-SA 4.0。

存在 NonCommercial 限制。

结论：
未经单独商业许可，不适合作为
广告变现翻译项目的内容来源。

## 三、许可证原始证据

Rust：
https://github.com/rust-lang/book/blob/main/COPYRIGHT

Dive into Deep Learning：
https://github.com/d2l-ai/d2l-en/blob/master/LICENSE

Google Developers：
https://developers.google.com/terms/site-policies

DeepSeek-R1：
https://github.com/deepseek-ai/DeepSeek-R1/blob/main/LICENSE

Shopify Theme Liquid Docs：
https://github.com/Shopify/theme-liquid-docs

OpenStax：
https://openstax.org/books/world-history-volume-1/pages/preface

## 四、下一轮问题

1. 确认 DeepSeek 具体 API 文档的版权边界。
2. 调查 Shopify Liquid 文档的内容规模和覆盖。
3. 核实 Rust 官方及社区译本覆盖情况。
4. 继续寻找长期有效、商业授权明确、
   且没有成熟多语言体系的 AI 基础教材。
5. 对非技术领域寻找同样符合条件的内容源。

上述研究均不意味着启动正式项目。

不得将许可证许可直接等同于
搜索流量、AdSense 批准或广告收入。

不启动翻译，不部署网站，
不修改 go-dev 项目。
