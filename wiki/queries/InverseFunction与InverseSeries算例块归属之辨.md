---
type: query
title: InverseFunction 与 InverseSeries 算例块归属之辨
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, InverseFunction, InverseSeries, 文献校勘]
related: [InverseFunction与InverseSeries算例复算, 20-2-7未入库回指缺口, 20-2-7全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/20.2.7 模式.md"]
---
# InverseFunction 与 InverseSeries 算例块归属之辨

## 问题

20.2.7 节（“模式”）末尾附有三个框排算例（■ A：`InverseFunction[f][x]`；■ B：`InverseFunction[Exp]`；■ C：`InverseSeries[Series[g[x], {x, 0, 2}]]`），与本节主题“模式”无任何文字衔接。此算例块究属 20.2.7，还是相邻小节（如未入库的 20.2.5/20.2.6），抑或 20.2 末算例框窜入？

## 证据

- 块内三例各自从 `In[1]` 起，为相互独立的会话算例，具备章末/节末框排算例的典型形态。
- 本 wiki 索引中无 20.2.5、20.2.6 的任何页面，两节是否存在、内容为何均不明；逆函数与级数反演恰是此类小节的常见主题。
- 式号无法判别：20.2.4 末式号约至 20.15，本节自 20.16 起连号，故 20.2.5/20.2.6（若存在）应无编号公式，或该算例块本无式号，无从由编号定位归属。
- 代码围栏语言标签 `autohotkey` 系导出伪影，不影响归属判断。

## 待办

核对纸本目录及 20.2.5/20.2.6 的实际内容。归属辨明前，不为 InverseFunction、InverseSeries 另立概念页（复算已录于 [[findings/InverseFunction与InverseSeries算例复算]]），相关缺口汇总于 [[queries/20-2-7未入库回指缺口]]。
