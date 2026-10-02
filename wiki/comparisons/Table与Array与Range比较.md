---
type: comparison
title: "Table、Array 与 Range 比较"
created: 2026-10-02
updated: 2026-10-02
tags: [Mathematica, 列表生成, 命令比较]
related: [Table-Range-Array列表生成命令, 列表（Mathematica）, 嵌套列表]
sources: ["数学手册(原书第10版)/20.2.4 列表.md"]
---

# Table、Array 与 Range 比较

本页并列比较 Mathematica 三个列表生成命令 Table、Array、Range 的语义分工。直接依据是《数学手册(原书第10版)》20.2.4.4 的原文表述——「命令 Array 使用函数（相对于 Table 使用的函数值）创建列表」——以及该节给出的 Table 表格算例与 Range、Array 说明。

## 比较表

| 维度 | Table | Array | Range |
|---|---|---|---|
| 生成机制 | 按迭代变量的取值对表达式求值（用「函数值」） | 将「函数本身」作用于指标 | 直接生成连续数或等间距数（算术序列） |
| 本节给出的形式 | Table[f, {imax}]；Table[f, {i, imin, imax}]；Table[f, {i, imin, imax, di}]；Table[f, {i, i1, i2}, {j, j1, j2}, ...] | Array[Exp, 5] | Range[n]；Range[n1, n2]；Range[n1, n2, dn] |
| 增量控制 | 迭代增量 di | 本节未述及 | 步长 dn（缺省 1） |
| 多维嵌套 | 支持：多重迭代器产生高维、多重嵌套表 | 本节未述及 | 不涉及 |
| 本节算例 | 二项式系数行、帕斯卡三角 | {e, e², e³, e⁴, e⁵} | {1, 2, ..., n} 等 |

## 要点

1. **Table 与 Array 的关键差别在「函数值 vs 函数本身」**：Table 对含迭代变量的表达式逐点求值（如 `Table[Binomial[7, i], {i, 0, 7}]`）；Array 直接以函数对象配指标长度（如 `Array[Exp, 5]`），不需写出调用式。
2. **Range 不涉及函数**，只按端点与步长生成算术序列，是最轻量的列表生成方式。
3. **只有 Table 在本节中被明确给出多维嵌套形式**，与嵌套列表（见 [[嵌套列表]]）直接衔接。

## 待核验

表 20.5 首行 `Table[f, {imax}]` 的释义（f(1), …, f(imax)）与 Mathematica 实际语义疑似冲突；若按实际语义（产生 imax 个 f 的拷贝），则「以最简形式产生函数值序列」的恰是 Array 而非 Table。见 [[Table首行imax释义与Mathematica语义之辨]] 与 [[Table-Range-Array二项式系数算例复算]]。