---
type: finding
title: "商群、群同态定理与 GL(n)/SL(n) ≅ ℝ∖{0} 实例（式 5.92）"
created: 2026-09-30
updated: 2026-09-30
tags: [群论, 商群, 同态定理, 矩阵群]
related: [商群, 群同态与同构, 正规子群, 典型矩阵群gln-sln-on-son-un-sun, 群同态与行列式例子]
sources: ["数学手册(原书第10版)/5.3.2 半群.md"]
source: "[[10-数学手册原书第10版--6-532-半群--pf5w9f]]"
confidence: high
replicated: null
---
# 商群、群同态定理与 GL(n)/SL(n) ≅ ℝ∖{0} 实例（式 5.92）

《数学手册(原书第10版)》5.3.3.3, 3. 定义商群（式 5.92）并给出群同态定理及其在矩阵群上的实例链。本发现为定理性陈述（标准成熟理论），未做独立复算；各环节均与已复核/已入库事实衔接（行列式乘法律见 [[findings/群同态与行列式例子]]）。

## 内容（式 5.92，逐字保留）

$$aN \circ bN = abN \tag{5.92}$$

- 群 $G$ 的正规子群 $N$ 的陪集的集合关于群运算也是一个群，称为 $G$ 关于 $N$ 的**商群** $G/N$。
- **群同态定理**：群同态 $h : G_1 \to G_2$ 定义 $G_1$ 的一个正规子群 $\ker h = \{a \in G_1 \mid h(a) = e\}$；商群 $G_1/\ker h$ 同构于同态象 $h(G_1) = \{h(a) \mid a \in G_1\}$。反之，$G_1$ 的每个正规子群通过 $\operatorname{nat}_N(a) = aN$ 定义一个同态映射 $\operatorname{nat}_N : G_1 \to G_1/N$，称为**自然同态**。

## 实例链（依本节）

> 因为行列式构造 $\det : GL(n) \to \mathbb{R}\backslash\{0\}$ 是一个核为 $SL(n)$ 的群同态，所以 $SL(n)$ 是 $GL(n)$ 的正规子群，并且（依据同态定理）$GL(n)/SL(n)$ 同构于实数的乘法群 $\mathbb{R}\backslash\{0\}$。

该链条把三件事连接起来：det 同态（式 5.91）→ 核 $SL(n)$ 正规 → 商群同构，是同态定理的标准演示，见 [[entities/典型矩阵群gln-sln-on-son-un-sun]]、[[comparisons/经典矩阵群比较]]。

## 转写注记

原文「实数的乘法群趴{O}」应为 $\mathbb{R}\backslash\{0\}$；「映射 na压」应为 $\operatorname{nat}_N$；「它称为 关千 的商群」脱 G、N，见 [[queries/5-3全节系统性转写讹误清单]]。