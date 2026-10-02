---
type: concept
title: 共轭指数与 (L^p)* = L^q
tags: [泛函分析, Lp空间, 对偶空间, 赫尔德不等式]
related: [Lp函数空间, lp空间, 对偶空间, 自反空间, 赫尔德条件]
created: 2026-10-01
updated: 2026-10-01
sources: ["数学手册(原书第10版)/12.5 连续线性算子和泛函.md"]
---
# 共轭指数与 (L^p)* = L^q

**共轭指数**：设 $p\ge1$，数 $q$ 称作 $p$ 的共轭指数，是指 $\frac1p+\frac1q=1$（$p=1$ 时约定 $q=\infty$）。

基于赫尔德积分不等式（源回指 1.4.2.12，未入库），可在 $L^p([a,b])$（$1\le p\le\infty$）上考虑积分型泛函 (12.163)（$\varphi\in L^q$），其范数是

$$\|f\|=\|\varphi\|=\begin{cases}\left(\int_a^b|\varphi|^q\,\mathrm{d}t\right)^{1/q}, & 1<p\le\infty,\\[4pt]\operatorname*{ess\,sup}_{t\in[a,b]}|\varphi|, & p=1,\end{cases}\tag{12.166}$$

反之，对于 $L^p([a,b])$ 中的连续线性泛函 $f$，存在唯一（按等价类确定的）元 $y\in L^q([a,b])$ 使得

$$f(x)=(x,y)=\int_a^b x(t)\overline{y(t)}\,\mathrm{d}t,\qquad\|f\|=\|y\|_q. \tag{12.167}$$

即 $(L^p)^*=L^q$（$1\le p<\infty$；至于 $p=\infty$ 情形，源移交文献 [12.18]）。

## 转写与术语注记

- 源注“（关于 $\exp|\varphi|$ 的定义参见 (12.221)）”中 "exp" 应为 **ess sup**，其定义在未入库的 12.9.4（见 [[queries/12-5未入库回指缺口]]）。
- **同名异义警示**：本节所引“赫尔德积分不等式”与库内 [[concepts/赫尔德条件]]（赫尔德**连续性**，11.5 用于奇异积分方程）是不同概念，勿混。
- 复算判定：(12.166)–(12.167) 限 $1\le p<\infty$ 无误，见 [[findings/式12-161至12-167连续泛函与Lp对偶转录复算]]。

## 关系

[[concepts/Lp函数空间]]、[[entities/lp空间]]（序列版对偶可类比）、[[entities/对偶空间]]、[[concepts/自反空间]]（$L^p$ 自反性判定的依据，并引发源内矛盾，见 [[queries/Lp空间自反性陈述内部矛盾]]）。