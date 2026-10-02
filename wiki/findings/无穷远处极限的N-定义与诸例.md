---
type: finding
title: "x 趋于 ±∞ 时极限的 N-定义与诸例（式 2.20a–2.20c）"
tags: [数学手册, 函数极限, 无穷远极限]
related: [函数的极限, 无穷小量与无穷大量, 10-数学手册原书第10版--9-214-函数的极限--u0yeeo]
created: 2026-09-29
updated: 2026-09-29
sources: ["数学手册(原书第10版)/2.1.4 函数的极限.md"]
source: "[[10-数学手册原书第10版--9-214-函数的极限--u0yeeo]]"
confidence: high
replicated: null
---

# x 趋于 ±∞ 时极限的 N-定义与诸例（式 2.20a–2.20c）

**发现**：手册 2.1.4.6 给出自变量趋于无穷时的两类定义。

**情形 a)（有限极限）**：若对任意正数 $\varepsilon$，都存在 $N>0$，当 $x>N$ 时 $A-\varepsilon<f(x)<A+\varepsilon$，则称 $A$ 为 $f(x)$ 当 $x\to+\infty$ 时的极限（式 2.20a）；$x\to-\infty$ 时（当 $x<-N$）类似（式 2.20b）。手册例（经核验）：$\lim_{x\to+\infty}\frac{x+1}{x}=1$、$\lim_{x\to-\infty}\frac{x+1}{x}=1$、$\lim_{x\to-\infty}e^x=0$。

**情形 b)（无穷）**：若对任意正数 $K$，都存在正数 $N$，使得当 $x>N$ 或 $x<-N$ 时 $\lvert f(x)\rvert>K$，则记 $\lim_{x\to+\infty}\lvert f(x)\rvert=\infty$ 或 $\lim_{x\to-\infty}\lvert f(x)\rvert=\infty$（式 2.20c）。手册例（经核验）：

- $\lim_{x\to+\infty}\frac{x^3-1}{x^2}=+\infty$，$\lim_{x\to-\infty}\frac{x^3-1}{x^2}=-\infty$；
- $\lim_{x\to+\infty}\frac{1-x^3}{x^2}=-\infty$，$\lim_{x\to-\infty}\frac{1-x^3}{x^2}=+\infty$。

全部四例的 $\pm\infty$ 判断经独立重算无误。概念页见 [[concepts/函数的极限]] 与 [[concepts/无穷小量与无穷大量]]。