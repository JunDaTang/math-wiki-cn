---
type: concept
title: "Mathematica标准函数"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 标准函数, 初等函数, 复自变量]
related: [entities/mathematica, concepts/Mathematica特殊函数, concepts/Mathematica数的四种基本类型, concepts/Mathematica中数的表示与转换, concepts/Head函数与类型查询, findings/表20-7与20-8函数名清单转录校勘, queries/20-2-6未入库回指缺口, sources/10-数学手册原书第10版--7-2026-函数--v9sqy0]
sources: ["数学手册(原书第10版)/20.2.6 函数.md"]
---
# Mathematica标准函数

Mathematica标准函数指 Mathematica 内建的基本初等数学函数，共六类：指数、对数、三角、反三角、双曲、反双曲。据手册 20.2.6.1（表 20.7），所有这些函数也都可以使用复自变量。其记号一律为 `函数名[自变量]` 的方括号前缀形式，与 Mathematica 表达式的一般结构（[[concepts/表达式（Mathematica）]]）一致。

## 表 20.7 若干标准函数

| 函数类 | Mathematica 记号 |
|---|---|
| 指数函数 | `Exp[x]` |
| 对数函数 | `Log[x]`, `Log[b,x]` |
| 三角函数 | `Sin[x]`, `Cos[x]`, `Tan[x]`, `Cot[x]`, `Sec[x]`, `Csc[x]` |
| 反三角函数 | `ArcSin[x]`, `ArcCos[x]`, `ArcTan[x]`, `ArcCot[x]`, `ArcSec[x]`, `ArcCsc[x]` |
| 双曲函数 | `Sinh[x]`, `Cosh[x]`, `Tanh[x]`, `Coth[x]`, `Sech[x]`, `Csch[x]` |
| 反双曲函数 | `ArcSinh[x]`, `ArcCosh[x]`, `ArcTanh[x]`, `ArcCoth[x]`, `ArcSech[x]`, `ArcCsch[x]` |

计 27 种调用形式、26 个不同函数名（`Log` 兼有 `Log[x]` 与 `Log[b,x]` 两种调用，后者为以 b 为底的对数）。逐一核验均为合法内建记号，表内未发现转写讹误（[[findings/表20-7与20-8函数名清单转录校勘]]）。

## 单值性：支与主值

手册指出：在每种情形下必须考虑该函数的单值性——对于实函数（如果需要的话）必须选择函数的一支；对于以复数为自变量的函数应该选择主值。原文回指手册第 989 页 14.5；该回指目标未入库（[[queries/20-2-6未入库回指缺口]]），本页仅能转述此一句带过的表述。

## 关联

- 数侧的类型与精度见 [[concepts/Mathematica数的四种基本类型]]、[[concepts/Mathematica中数的表示与转换]]。
- 与 [[concepts/Mathematica特殊函数]] 相对：前者为初等函数，后者为非初等的命名函数。
- 求值后表达式的头可由 [[concepts/Head函数与类型查询]] 查询。