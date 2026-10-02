---
type: finding
title: "矩阵作为 R^n 到 R^m 的映射并以线性方程组表示（式 2.3 例 B）"
tags: [数学手册, 映射, 矩阵, 线性代数]
related: [映射, 函数, 10-数学手册原书第10版--9-211-函数的定义--191yjep]
sources: ["数学手册(原书第10版)/2.1.1 函数的定义.md"]
source: "[[10-数学手册原书第10版--9-211-函数的定义--191yjep]]"
confidence: high
replicated: null
created: 2026-09-29
updated: 2026-09-29
---

# 矩阵作为 R^n 到 R^m 的映射并以线性方程组表示（式 2.3 例 B）

手册 2.1.1.7 例 B：若 $f$ 是一个 $(m,n)$ 型的矩阵 $A=(a_{ij})$（$i=1,2,\cdots,m$；$j=1,2,\cdots,n$），且 $X=\mathbb{R}^n$、$Y=\mathbb{R}^m$，则式 (2.3) 定义了一个从 $\mathbb{R}^n$ 到 $\mathbb{R}^m$ 的映射。对应法则 (2.3) 可以用下面的 $m$ 个线性方程构成的方程组表示（原文逐字保留）：

```latex
\begin{array}{rl}
& y_1 = a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n, \\
\underline{\boldsymbol{y}} = A\underline{\boldsymbol{x}} \text{ 或} & y_2 = a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n, \\
& \dots\dots \\
& y_m = a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n
\end{array}
```

即 $A\underline{\boldsymbol{x}}$ 表示矩阵 $A$ 与向量 $\underline{\boldsymbol{x}}$ 的乘积。

## 证据与置信

直接证据：本节例 B 原文（含方程组），见 [[sources/10-数学手册原书第10版--9-211-函数的定义--191yjep]]。该例是手册给出的映射概念典范实例：矩阵按式 (2.3) 定义 $\mathbb{R}^n \to \mathbb{R}^m$ 的映射，对应法则由 $m$ 个线性方程给出。概念页见 [[concepts/映射]]。