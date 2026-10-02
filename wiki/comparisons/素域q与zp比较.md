---
type: comparison
title: "素域 ℚ 与 ℤ_p 比较"
created: 2026-09-30
updated: 2026-09-30
tags: [代数, 环和域, 素域, 有限域]
related: [素域, 剩余类环zn, 伽罗瓦域gf-pn, 域扩张, 环的特征]
sources: ["数学手册(原书第10版)/5.3.7 环和域.md"]
---
# 素域 ℚ 与 ℤ_p 比较

数学手册 5.3.7.1.3 的素域分类：除同构外，$\mathbb{Q}$ 与 $\mathbb{Z}_p$（p 素数）是仅有的素域，分别嵌入特征 0 与特征 p 的域。

| | ℚ | ℤ_p |
|---|---|---|
| 特征 | 0 | p（素数） |
| 元素数 | 无限 | p |
| 构造 | 有理数域本身 | 剩余类环 $\mathbb{Z}/(p)$；p 素时为域（式 5.174 判据） |
| 作为素域出现于 | 每个特征 0 的域（如 ℝ；ℝ 是 ℚ 上无限维空间） | 每个特征 p 的域（如 GF(pⁿ)，见 [[findings/kx-fx-商环构造与gf-pn]]） |
| 在本节的下游角色 | ℂ = ℝ(i) 扩张链的底（ℝ/ℚ 无限维） | GF(pⁿ) 构造的基域 $\mathbb{Z}_p$ |

## 共同点

- 都没有任何真子域（素域定义）；每个域 $K$ 都含有一个最小的子域，即 $K$ 的素域；
- 鉴别方法：给定域 $K$，其素域由 $\operatorname{char} K$ 决定——$\operatorname{char} K = 0$ ⟹ ℚ；$\operatorname{char} K = p$ ⟹ $\mathbb{Z}_p$（与 [[concepts/环的特征]] 衔接）。

## 相关页面

[[findings/素域分类与c等于ri]]（分类陈述与 ℂ = ℝ(i)）、[[comparisons/gf-pn与zp-n比较]]（ℤ_p 与 GF(pⁿ) 的区分）、[[entities/数集记号]]、[[entities/剩余类环zn]]、[[entities/伽罗瓦域gf-pn]]。