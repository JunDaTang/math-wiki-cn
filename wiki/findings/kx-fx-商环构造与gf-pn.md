---
type: finding
title: "K[x]/f(x) 商环构造与 GF(pⁿ)（式 5.179）"
created: 2026-09-30
updated: 2026-09-30
tags: [代数, 环和域, 有限域, 商环, 不可约多项式]
related: [伽罗瓦域gf-pn, 不可约多项式, 多项式环, 商环, 剩余类环zn]
sources: ["数学手册(原书第10版)/5.3.7 环和域.md"]
source: "[[10-数学手册原书第10版--7-537-环和域--3j0nhk]]"
confidence: high
replicated: true
---
# K[x]/f(x) 商环构造与 GF(pⁿ)（式 5.179）

数学手册 5.3.7.4.1 给出有限域的存在唯一性，并用多项式商环构造 GF(pⁿ)。

## 存在唯一性

对于每个素数幂 $p^n$ 存在唯一的含 $p^n$ 个元素的域（不计同构），并且每个有限域含素数幂 $p^n$ 个元素。$p^n$ 个元素的域记作 $\mathrm{GF}(p^n)$（伽罗瓦域）。源文特别提醒：**对于 $n > 1$，$\mathrm{GF}(p^n)$ 与 $\mathbb{Z}_{p^n}$ 是不同的**（对照 [[comparisons/gf-pn与zp-n比较]]）。

## 商环构造（式 5.179）

不可约多项式：$f(x) \in K[x]$ 不能表示为较低次数的多项式之积，即（类似于 $\mathbb{Z}$ 中的素数）$f(x)$ 是 $K[x]$ 中的素元素；对于二次或三次多项式，不可约性意味着它们在 $K$ 中没有根。可以证明 $K[x]$ 中存在任意次数的不可约多项式。如果 $f(x) \in K[x]$ 是不可约多项式，那么

$$K[x]/f(x) := \{p(x) \in K[x] \mid \deg p(x) < \deg f(x)\} \tag{5.179}$$

是一个域，这里加法和乘法由模 $f(x)$ 实施，即 $g(x) * h(x) = g(x) \cdot h(x) \pmod{f(x)}$。

如果 $K = \mathbb{Z}_p$ 并且 $\deg f(x) = n$，那么 $K[x]/f(x)$ 有 $p^n$ 个元素，即 $\mathrm{GF}(p^n) = \mathbb{Z}_p[x]/f(x)$，其中 $f(x)$ 是 n 次不可约多项式（源文两处将记号写作 $\mathbb{Z}_p/f(x)$、$\mathbb{Z}_p(x)$，高置信脱落「[x]」，见 [[queries/zp-fx记号是否缺x]]）。

## 分裂域视角

在 $\mathrm{GF}(p^n) = \mathbb{Z}_p[x]/f(x)$ 中存在一个元素 $\alpha = x$ 是不可约多项式 $f(x)$ 的一个根，并且 $\mathrm{GF}(p^n) = \mathbb{Z}_p[x]/f(x) = \mathbb{Z}_p(\alpha)$。可以证明 $\mathbb{Z}_p(\alpha)$ 是 $f(x)$ 的分裂域——$\mathbb{Z}_p$ 的含 $f(x)$ 所有根的最小扩张。

## 复核说明

✓ 构造在 $p = 2$、$n = 3$ 的实例 $\mathrm{GF}(2^3)$ 中完整验证（对数表全表复算通过，见 [[findings/gf23对数表与分式算例]]）；存在唯一性与分裂域陈述为标准结果，源未给证明。相关：[[concepts/不可约多项式]]、[[concepts/域扩张]]、[[entities/伽罗瓦域gf-pn]]。