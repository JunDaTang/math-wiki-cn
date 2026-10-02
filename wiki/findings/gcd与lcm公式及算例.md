---
type: finding
title: gcd 与 lcm 的指数公式及关系式
tags: [数论, gcd, lcm, 指数公式]
related: [最大公因子与最小公倍数, gcd与lcm比较, 标准素因子分解]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.4.1 整除性.md"]
source: "[[10-数学手册原书第10版--7-541-整除性--1bgclvy]]"
confidence: high
replicated: true
---

# gcd 与 lcm 的指数公式及关系式

## 内容（式 5.231、5.235、5.236）

- **gcd**：对不全为零的整数，公因子集合中的最大数；$\gcd=1$ 时称互素。由标准素因子分解 $a_i=\prod_p p^{\nu_p(a_i)}$（5.231a）：

$$\gcd(a_1,\dots,a_n)=\prod_p p^{\min_i(\nu_p(a_i))}\tag{5.231b}$$

- **lcm**：对全不为零的整数，正公倍数集合中最小的数：

$$\operatorname{lcm}(a_1,\dots,a_n)=\prod_p p^{\max_i(\nu_p(a_i))}\tag{5.235}$$

- **关系式**：对任意整数 $a,b$，

$$|ab|=\gcd(a,b)\cdot\operatorname{lcm}(a,b)\tag{5.236}$$

本源指出：因此 $\operatorname{lcm}(a,b)$ 可借助欧几里得算法而不应用素因子分解确定。

## 算例（本次独立复算，全部通过）

$a_1=15400=2^3\cdot5^2\cdot7\cdot11$ ✓，$a_2=7875=3^2\cdot5^3\cdot7$ ✓，$a_3=3850=2\cdot5^2\cdot7\cdot11$ ✓：

- $\gcd(a_1,a_2,a_3)=5^2\cdot7=175$ ✓（各素数指数取最小）
- $\operatorname{lcm}(a_1,a_2,a_3)=2^3\cdot3^2\cdot5^3\cdot7\cdot11=693000$ ✓（取最大）

## 边界

min/max 对偶与两概念的完整对照见 [[comparisons/gcd与lcm比较]]；计算算法见 [[methodology/整数欧几里得算法求gcd流程]]。
