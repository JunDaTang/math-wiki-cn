---
type: concept
title: Do 与 While 循环（Mathematica）
tags: [mathematica, 循环结构, do, while, 程序设计, 迭代]
related: [concepts/Module与局部变元, concepts/Mathematica函数式程序设计, concepts/Mathematica输入输出行记法, entities/mathematica, findings/式20-24与20-26循环与模块语法转录复算, findings/式20-25-e2级数近似算例复算, findings/式20-27-sumq过程式算例复算, comparisons/Do循环与While循环比较]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
---
# Do 与 While 循环（Mathematica）

`Do` 与 `While` 是 Mathematica 中两个基本的循环结构命令：前者按事先给定的次数对表达式重复求值，后者在条件保持为 True 期间持续求值。《数学手册（原书第10版）》20.2.9（式 20.24a/b）将其定位为 Mathematica「可以处理其他程序设计语言中所熟知的循环结构」的两个基本命令。

## 语法

```
Do[expr, {i, i1, i2, di}]    (20.24a)
While[test, expr]            (20.24b)
```

**Do 的迭代子句与默认值**（据原文文字说明，该句存在脱字）：

- 循环变量 i 以步长 di 从 i1 取值到 i2；
- 略去 di，则步长为 1；
- 再略去 i1，则从 1 开始。

**While**：只要 test 具有值 True，即对 expr 求值；条件失效则终止。原文概括：「Do 循环按照事先给定的次数对其自变量赋值，而 While 循环赋值直到事先给定的条件失效」——其中「赋值」疑为「求值」的翻译残留，见 [[queries/赋值措辞疑为求值语义之辨]]。

## 本节算例

e² 级数近似（式 20.25，以 `Do` 累加 Σ 2^i/i!）：

```
In[1] := sum = 1.0;
        Do[sum = sum + (2^i/i!), {i, 1, 10}];
        sum
Out[1] = 7.38899
```

例 A 的 `sumq` 定义（式 20.27）以 `Do[sum = sum + N[Sqrt[i]], {i, 2, n}]` 实现 Σ_{i=1}^n √i 的累加，并与 [[concepts/Module与局部变元]] 配合使用。

## 相关比较与校勘

- 定次数与条件驱动的对照见 [[comparisons/Do循环与While循环比较]]；
- 语法转录与 Mathematica 实际语义的一致性核对见 [[findings/式20-24与20-26循环与模块语法转录复算]]；
- 原文迭代子句描述的脱字问题见 [[queries/Do迭代描述脱循环变量与起值之辨]]；
- 本节全部算例均使用 `Do`，`While` 仅有语法定义而无算例，故 `While` 的行为细节不据本来源展开。