---
type: comparison
title: 过程式与函数式 sumq 实现比较
tags: [mathematica, module, do, apply, table, total, range, sumq, 函数式程序设计, 比较]
related: [concepts/Module与局部变元, concepts/Mathematica函数式程序设计, concepts/Table-Range-Array列表生成命令, sources/10-数学手册原书第10版--9-2029-程序设计--l13hq7, findings/式20-27-sumq过程式算例复算, findings/例B-函数式sumq与Total复算, queries/Total版十位结果逐位相同之辨]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
---
# 过程式与函数式 sumq 实现比较

《数学手册（原书第10版）》20.2.9 以同一任务（Σ_{i=1}^n √i）给出例 A（过程式）与例 B（函数式）两种实现，并称函数式版本「不使用下标，不连续递增其值，也无须变元 sum 及其初始值」。三种写法对照如下（证据均出自本来源）：

| 维度 | 例 A（Module + Do） | 例 B（Apply + Table） | 例 B 之 Total 变体 |
|---|---|---|---|
| 构造 | 过程式：局部变元 + 循环累加 | 函数式：生成列表后求和 | 函数式：列表整体运算 |
| 代码 | `Module[{sum = 1.}, Do[sum = sum + N[Sqrt[i]], {i, 2, n}]; sum]` | `N[Apply[Plus, Table[Sqrt[i], {i, 1, n}]], 10]` | `Total[Sqrt[N[Range[n], 10]]]` |
| 局部变元 | 须变元 sum 及初值 1. | 无 | 无（原文明言「无须变元 sum 及其初始值」） |
| 下标与递增 | 循环变量 i 自 2 递增至 n | `Table` 仍以下标 i 生成列表 | 原文称「不使用下标，不连续递增其值」 |
| 精度路径 | 逐项 `N[Sqrt[i]]` 机器精度 | 精确求和后 `N[..., 10]` | 逐项 10 位精度数值化 |
| sumq[30] 结果 | 112.083（机器精度显示） | 112.0828452（复算通过） | 原文称与左同，逐位待实测 |

要点：

- **精度差异**：例 A 显示 112.083 缘于逐项机器精度与约 6 位显示；例 B 先精确求和再取 10 位有效数字，得 112.0828452（[[findings/式20-27-sumq过程式算例复算]]、[[findings/例B-函数式sumq与Total复算]]）；
- **原文观点（修辞性）**：函数式方法是 Mathematica 程序设计「真正力量」所在；例 A/B 对比为其佐证，但无量化证据；
- **保留**：`Total` 变体与 `N[Apply[...], 10]` 之逐位一致性未经实测（[[queries/Total版十位结果逐位相同之辨]]）；原文「不使用下标」之评语按句法系针对 `Total` 变体，`Apply/Table` 版仍隐式使用下标。