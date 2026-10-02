---
type: finding
title: "素域分类与 ℂ = ℝ(i)"
created: 2026-09-30
updated: 2026-09-30
tags: [代数, 环和域, 素域, 域扩张]
related: [素域, 域扩张, 极小多项式, 数集记号]
sources: ["数学手册(原书第10版)/5.3.7 环和域.md"]
source: "[[10-数学手册原书第10版--7-537-环和域--3j0nhk]]"
confidence: high
replicated: null
---
# 素域分类与 ℂ = ℝ(i)

数学手册 5.3.7.1.3 给出域扩张的关键例子与素域的分类。

## ℂ = ℝ(i) 与扩张次数

$\mathbb{C} = \mathbb{R}(\mathrm{i})$，并且 $\mathrm{i} \in \mathbb{C}$ 是多项式 $x^2 + 1 \in \mathbb{R}[x]$ 的根，即 $\mathbb{C}$ 是 $\mathbb{R}$ 的单代数扩张，并且 $[\mathbb{C} : \mathbb{R}] = 2$：$\mathbb{C}$ 在 $\mathbb{R}$ 上是 2 维的，$\{1, \mathrm{i}\}$ 是基。对照：$\mathbb{R}$ 是 $\mathbb{Q}$ 上的无限维空间。

一般框架（概念页见 [[concepts/域扩张]]）：对于集合 $M \subseteq L$，$K(M)$ 表示含域 $K$ 及集合 $M$ 的最小域；特别重要的是单代数扩张 $K(\alpha)$（$\alpha \in L$ 是 $K[x]$ 中某多项式的根）。若 $\alpha \in L$ 的极小多项式（以 $\alpha$ 为根的最低次且首项系数为 1 的多项式）次数是 n，则 $K(\alpha)$ 是 n 次扩张，即**极小多项式的次数等于 $K(\alpha)$ 作为 $K$ 上向量空间的维数**（见 [[concepts/极小多项式]]）。

## 素域分类

- 没有任何真子域的域称作**素域**；每个域 $K$ 都含有一个最小的子域，即 $K$ 的素域；
- 除同构外，$\mathbb{Q}$（对于特征 0 的域）以及 $\mathbb{Z}_p$（$p$ 是素数，对于特征 p 的域）是仅有的素域（源文作「是单素域」，「单」疑为衍字，见 [[queries/5-3-7全节系统性转写讹误清单]]）。

## 复核说明

均为标准结果，源未给证明；$[\mathbb{C} : \mathbb{R}] = 2$ 与 $\{1, \mathrm{i}\}$ 为基是可直接验证的初等事实。素域并置比较见 [[comparisons/素域q与zp比较]]；数集记号见 [[entities/数集记号]]。