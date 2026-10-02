---
type: query
title: "Table 首行 imax 释义与 Mathematica 语义之辨"
created: 2026-10-02
updated: 2026-10-02
tags: [Mathematica, Table, 语义校勘]
related: [Table-Range-Array列表生成命令, Table与Array与Range比较, 10-数学手册原书第10版--7-2024-列表--9o5vl4]
sources: ["数学手册(原书第10版)/20.2.4 列表.md"]
---

# Table 首行 imax 释义与 Mathematica 语义之辨

## 疑点

表 20.5 首行将 `Table[f, {imax}]` 释为「创建 f 具有 imax 值: f(1), f(2),···, f(imax) 的一个列表」。而按 Mathematica 实际语义，`Table[f, {imax}]` 的迭代说明不含迭代变量，产生的是 imax 个 f 本身的拷贝；欲得函数值序列须写 `Table[f[i], {i, imax}]` 或 `Array[f, imax]`。

## 裁定路径

1. 在 Mathematica 中实测 `Table[f, {3}]` 与 `Table[f[i], {i, 3}]` 的输出差异；
2. 核对原书该行命令是否为 `Table[f[i], {i, imax}]`（转写脱迭代变量的下标）抑或原书释义本身如此；
3. 结论回填 [[Table-Range-Array列表生成命令]] 与 [[Table与Array与Range比较]]。

## 佐证与局限

- 本节二项式系数算例均含迭代变量（{i, 0, 7}、{i, 1, 7}），不能佐证或反证首行释义（见 [[Table-Range-Array二项式系数算例复算]]）。
- 源文自身的「Array 使用函数（相对于 Table 使用的函数值）」之说，与首行「无变量的 f(1)…f(imax)」表述存在张力。