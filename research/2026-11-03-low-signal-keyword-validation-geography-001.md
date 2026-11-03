# 地理领域低信号关键词验证 001

核实日期：2026-11-03
状态：RESEARCH_ONLY
阶段：LOW_SIGNAL_KEYWORD_VALIDATION

## 一、数据来源

来源：https://trends.google.com/explore
地区：德国（DE）
时间：2021-11-01 至 2026-10-31
搜索类型：Google 网页搜索
数据点：60个月，5个搜索词

这是同一批次中的相对搜索兴趣指数，
可用于本批次内部比较，
不能直接与上一批 AI / Python / 历史等词的指数做严格数值比较。

## 二、实测结果

| 搜索词 | 60月平均 | 前12月平均 | 后12月平均 | 0值月份 |
| --- | ---: | ---: | ---: | ---: |
| Geografie lernen | 0.02 | 0.00 | 0.08 | 59/60 |
| Geographie lernen | 5.35 | 5.50 | 6.08 | 12/60 |
| Erdkunde lernen | 1.85 | 2.25 | 1.50 | 40/60 |
| Hauptstädte lernen | 8.08 | 7.25 | 8.75 | 6/60 |
| Länder und Hauptstädte | 64.03 | 74.08 | 54.08 | 0/60 |

## 三、研究结论

1. `Geografie lernen` 几乎全程为0，不适合作为代表地理学习需求的主关键词。
2. `Geographie lernen` 存在稳定但不高的真实需求。
3. `Hauptstädte lernen` 具有更明显的学习需求信号。
4. `Länder und Hauptstädte` 是本批次中最强的地理相关表达。
5. 地理方向更值得进一步研究的可能不是泛化的“地理教程”，
   而是国家、首都、地图、查询、记忆与练习类内容或工具。

## 四、商业解释边界

- 本轮只能说明上次地理信号偏低主要与关键词选择有关。
- 不能仅据本轮数据选定正式项目。
- 不能把 Trends 指数当作绝对搜索次数。
- 不能把本批次指数与其他批次直接拼接比较。

## 五、原始证据

文件：`research/evidence/2026-11-03-google-trends-DE-geography-001.csv`
SHA-256：`5a329605227fc54c87c568e89694a9370f42196d385a109763bd870260b1deb5`

## 六、下一步

建议进入：RUST_LOW_SIGNAL_KEYWORD_VALIDATION

优先验证 Rust 是否也因关键词选择不当而被低估。
在此之前，不淘汰地理领域。

不启动翻译、建站或部署。
不修改 go-dev v2。
