---
type: entity
title: "GF(pⁿ)（伽罗瓦域／有限域）"
created: 2026-09-30
updated: 2026-09-30
tags: [域论, 有限域, 伽罗瓦域, 抽象代数, 编码理论, 数学手册, 5-3-7]
related: [concepts/不可约多项式, concepts/本原多项式, concepts/多项式环, concepts/素域, concepts/代数闭与代数闭包, concepts/环的特征, concepts/域扩张, entities/剩余类环zn, entities/线性反馈移位寄存器, concepts/分圆域, comparisons/gfpn与zpn比较, findings/gf23构造与对数表算例, findings/有限域存在唯一性与构造定理组, findings/有限域乘法群循环性与本原多项式, methodology/gf对数表构造与运算流程]
sources: ["数学手册(原书第10版)/5.3.7 环和域.md"]
---
# GF(pⁿ)（伽罗瓦域／有限域）

GF(pⁿ)（伽罗瓦域，又称有限域）是恰含 pⁿ 个元素（p 为素数、n 为正整数）的域，以 Galois 命名。源书断言：对每个素数幂 pⁿ 存在唯一的（不计同构）pⁿ 元域，且每个有限域的元素个数都是素数幂。它是本节最重的实质数学对象，也是编码理论与线性反馈移位寄存器的公共基础。

## 存在唯一性

- 对每个素数幂 pⁿ，存在唯一的含 pⁿ 个元素的域（不计同构）；
- 每个有限域含 pⁿ 个元素（阶必为素数幂）；
- **注意**：对 n > 1，GF(pⁿ) 与 ℤ_{pⁿ} 是不同的（见 [[comparisons/gfpn与zpn比较]]）。

## 构造：ℤ_p[x]/f(x)

构造需要 ℤ_p 上的多项式环（系数按模 p 计算，见 [[concepts/多项式环]]）与 n 次不可约多项式 f（见 [[concepts/不可约多项式]]）：

$$
K[x]/f(x) := \{p(x) \in K[x] \mid \deg p(x) < \deg f(x)\}\tag{5.179}
$$

在模 f(x) 的加法与乘法下是一个域；当 K = ℤ_p 且 deg f = n 时恰有 pⁿ 个元素，即 GF(pⁿ) = ℤ_p[x]/f(x)（源文作 ℤ_p/f(x)，脱 [x]）。

## Frobenius 运算法则

GF(pⁿ) 中成立

$$
(a + b)^{p^{r}} = a^{p^{r}} + b^{p^{r}}, \quad r \in \mathbb{N}.\tag{5.180}
$$

GF(pⁿ) 的特征为 p（见 [[concepts/环的特征]]）。

## 分裂域身份

在 GF(pⁿ) = ℤ_p[x]/f(x) 中存在元素 α = x，它是不可约多项式 f(x) ∈ ℤ_p[x] 的一个根，且 GF(pⁿ) = ℤ_p(α)；可以证明 ℤ_p(α) 是 f(x) 的分裂域（ℤ_p 的含 f(x) 所有根的最小扩张，见 [[concepts/域扩张]]）。GF(p) = ℤ_p 本身是素域（见 [[concepts/素域]]）；有限域的代数闭包并不有限（见 [[concepts/代数闭与代数闭包]]）。

## 乘法群循环性与对数表

有限域的乘法群 K* = K \ {0} 是循环群；不可约 f 为本原多项式 ⇔ x 生成 L* = (K[x]/f(x))*（见 [[concepts/本原多项式]]、[[findings/有限域乘法群循环性与本原多项式]]）。借助本原 f 可构造 GF(pⁿ) 的对数表，把乘除法化为对数（模 pⁿ − 1）加法（流程见 [[methodology/gf对数表构造与运算流程]]）；GF(2³) 的完整算例见 [[findings/gf23构造与对数表算例]]。

## 应用

- 编码理论：线性码是 (GF(q))ⁿ 的子空间，码字是 GF(q) 元素的 n 元组（引 5.4.6.2.3，未入库）；
- 分圆域：Xⁿ − 1 的分裂域与 n 次单位根（见 [[concepts/分圆域]]）；
- 多项式模 f(x) 运算可由 [[entities/线性反馈移位寄存器]] 实施。