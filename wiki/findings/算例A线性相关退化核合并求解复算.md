---
type: finding
title: 算例 A 线性相关退化核合并求解复算
tags: [算例复算, 积分方程, 退化核, 线性相关, 线性方程组]
related: [concepts/退化核, methodology/退化核求解流程, entities/第二类弗雷德霍姆积分方程, findings/式11-7a至11-7d系数方程组建立转录复算, queries/11-2-1全节系统性转写讹误清单]
created: 2026-09-30
updated: 2026-09-30
source: "[[sources/10-数学手册原书第10版--15-1121-具有退化核的积分方程--1pg6dhz]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/11.2.1 具有退化核的积分方程.md"]
---
# 算例 A 线性相关退化核合并求解复算

**结论**：算例 A（$\lambda=1$，核 $x^2y+xy^2-xy$，区间 $[-1,1]$）的全部系数、方程组与解经逐项独立复算吻合；对 (11.5) 最小性条件的活用（合并线性相关项）是本算例的方法要点。

## 题目与合并

$$\varphi(x) = x + \int_{-1}^{+1}\bigl(x^2y + xy^2 - xy\bigr)\varphi(y)\,\mathrm{d}y$$

原始分解：$\alpha_1=x^2,\ \alpha_2=x,\ \alpha_3=-x$；$\beta_1=y,\ \beta_2=y^2,\ \beta_3=y$。其中 $\alpha_2=x$ 与 $\alpha_3=-x$ **线性相关**，违反 (11.5) 最小性条件，故合并为两项核：

$$\varphi(x) = x + \int_{-1}^{+1}\bigl[x^2y + x(y^2-y)\bigr]\varphi(y)\,\mathrm{d}y,\qquad \alpha_1=x^2,\ \alpha_2=x,\ \beta_1=y,\ \beta_2=y^2-y$$

解形式：$\varphi(x) = x + A_1x^2 + A_2x$。

## 系数复算（全部吻合）

| 量 | 复算值 | 核对 |
|---|---|---|
| $c_{11}=\int_{-1}^{1}x^3\,\mathrm{d}x$ | $0$ | ✓ |
| $c_{12}=\int_{-1}^{1}x^2\,\mathrm{d}x$ | $2/3$ | ✓ |
| $c_{21}=\int_{-1}^{1}(x^4-x^3)\,\mathrm{d}x$ | $2/5$ | ✓ |
| $c_{22}=\int_{-1}^{1}(x^3-x^2)\,\mathrm{d}x$ | $-2/3$ | ✓ |
| $b_{1}=\int_{-1}^{1}x^2\,\mathrm{d}x$ | $2/3$ | ✓ |
| $b_{2}=\int_{-1}^{1}(x^3-x^2)\,\mathrm{d}x$ | $-2/3$ | ✓ |

## 方程组与解

$$A_1 - \tfrac{2}{3}A_2 = \tfrac{2}{3},\qquad -\tfrac{2}{5}A_1 + \bigl(1+\tfrac{2}{3}\bigr)A_2 = -\tfrac{2}{3}$$

解得 $A_1=\dfrac{10}{21},\ A_2=-\dfrac{2}{7}$，故

$$\varphi(x) = x + \tfrac{10}{21}x^2 - \tfrac{2}{7}x = \tfrac{10}{21}x^2 + \tfrac{5}{7}x \quad ✓$$

## 附加验证（原文未算，复算时补充）

$$D(1)=\det\begin{pmatrix}1 & -2/3\\ -2/5 & 5/3\end{pmatrix} = 1+\tfrac{2}{3}-\tfrac{4}{15} = \tfrac{7}{5}\neq 0$$

与 $D(\lambda)\neq 0$ 情形的唯一可解性相符。

## 转写问题

"个函数 $\alpha_k(x)$ 是线性相关的"漏"这 3"（或"诸"）；"利用这些值来确 $A_1$ 和 $A_2$"疑漏"定"；方程组中 "(1+ 2/3 ∫A₂" 的 "∫" 疑为 ")" 之讹。见 [[queries/11-2-1全节系统性转写讹误清单]]，均不影响数学内容。