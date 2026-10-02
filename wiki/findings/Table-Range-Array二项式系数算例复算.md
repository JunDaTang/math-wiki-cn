---
type: finding
title: "Table-Range-Array 二项式系数算例复算"
created: 2026-10-02
updated: 2026-10-02
tags: [Mathematica, Table, Range, Array, 算例复算]
related: [Table-Range-Array列表生成命令, Table与Array与Range比较]
sources: ["数学手册(原书第10版)/20.2.4 列表.md"]
source: "[[10-数学手册原书第10版--7-2024-列表--9o5vl4]]"
confidence: high
replicated: true
---

# Table、Range 与 Array 二项式系数算例复算

对 20.2.4.4 的 Table 二项式系数算例及 Range、Array 语义复算，全部通过，属直接证据。

| 转录算例 | 复算判定 |
|---|---|
| Table[Binomial[7, i], {i, 0, 7}] → {1, 7, 21, 35, 35, 21, 7, 1} | 通过：n = 7 的二项式系数行（k = 0..7） |
| Table[Binomial[i, j], {i, 1, 7}, {j, 0, i}] → 七个嵌套子列表 | 通过：恰为帕斯卡三角第 1–7 行，内层迭代上界 {j, 0, i} 依赖外层变量 |
| Array[Exp, 5] → {e, e², e³, e⁴, e⁵} | 通过：与「Array 使用函数本身」之说一致 |
| Range[n] → {1, 2, ..., n}；Range[n1, n2, dn] 步长 1 或 dn | 通过：算术序列语义 |

## 附注

- In[1] 转录衍一右括号（`{i, 0, 7}]]`）；正文「得到直至 次的二项式系数」脱「7」，见 [[20-2-4全节系统性转写讹误清单]]。
- 本组算例均含迭代变量（{i, 0, 7} 或 {i, 1, 7}），不能验证表 20.5 首行 `Table[f, {imax}]`（无迭代变量）的释义；该释义之辨见 [[Table首行imax释义与Mathematica语义之辨]]。