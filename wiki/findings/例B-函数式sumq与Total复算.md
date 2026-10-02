---
type: finding
title: 例 B 函数式 sumq 与 Total 复算
tags: [mathematica, apply, plus, table, total, range, sumq, 函数式程序设计, 转录复算]
related: [concepts/Mathematica函数式程序设计, concepts/Table-Range-Array列表生成命令, sources/10-数学手册原书第10版--9-2029-程序设计--l13hq7, findings/式20-27-sumq过程式算例复算, comparisons/过程式与函数式sumq实现比较, queries/Total版十位结果逐位相同之辨]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
source: "[[sources/10-数学手册原书第10版--9-2029-程序设计--l13hq7]]"
confidence: high
replicated: true
---
# 例 B 函数式 sumq 与 Total 复算

**结论**：例 B 之 `N[Apply[Plus, Table[Sqrt[i], {i, 1, n}]], 10]` 在 n = 30 时给出 112.0828452，经独立复算验证**正确**（10 位有效数字）；同页所称 `Total[Sqrt[N[Range[n], 10]]]`「给出相同的结果」为**推断性陈述**，其逐位一致性未经实测验证。

## 原文转录（例 B）

```
sumq[n_] := N[Apply[Plus, Table[Sqrt[i], {i, 1, n}]], 10]
```

`sumq[30]` 的结果为 112.0828452；`Total[Sqrt[N[Range[n], 10]]]` 据称给出相同的结果。

## 复算

- 精确和 Σ_{i=1}^{30} √i = 112.0828452157…；
- 取 10 位有效数字得 **112.0828452**，与原文一致（此为 `N[精确表达式, 10]` 语义：先在精确数域求和，再一次性数值化）。

## 直接证据与推断之别

- **直接证据（已复算）**：`N[Apply[Plus, Table[...]], 10]` 之结果 112.0828452；
- **推断（未实测）**：`Total[Sqrt[N[Range[n], 10]]]` 与上者逐位相同。该式先将各整数数值化为 10 位精度、逐项开方（每项各自舍入）、再求和，30 项的逐项舍入累积可能波及末位；原文断言偏强，见 [[queries/Total版十位结果逐位相同之辨]]。

## 措辞含混

原文「要求有十位精确数字」与 `N[..., 10]` 的实际语义（10 位**有效数字**）措辞略含混，属翻译措辞问题而非计算错误。