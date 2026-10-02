---
type: finding
title: 式 12.56 柯西序列与 ℓ¹ 上 sup 距离不完备反例复算
created: 2026-10-01
updated: 2026-10-01
tags: [泛函分析, 柯西序列, 完备性, 转录复算]
related: [柯西序列与完备距离空间, lp序列空间, lp空间两种距离完备性比较, 距离空间的完备化]
sources: ["数学手册(原书第10版)/12.2 距离空间.md"]
source: "[[10-数学手册原书第10版--8-122-距离空间--4k304g]]"
confidence: high
replicated: true
---

# 式 12.56 柯西序列与 ℓ¹ 上 sup 距离不完备反例复算

## 转录内容

柯西序列定义 (12.56)：$\forall\varepsilon>0\ \exists n_0(\varepsilon)\ \forall n,m>n_0:\rho(x_n,x_m)<\varepsilon$。性质：每个柯西序列都是有界集；每个收敛序列都是柯西序列；逆命题一般不成立。反例（转录）：考虑空间 $\ell^1$ 赋以空间 $m$ 的距离 (12.46)，则 $x^{(n)}=(1,\tfrac12,\dots,\tfrac1n,0,0,\dots)$ 是柯西列；若收敛则必按坐标收敛于 $x^{(0)}=(1,\tfrac12,\tfrac13,\dots)$，但 $x^{(0)}\notin\ell^1$，因为 $\sum_{n=1}^\infty\tfrac1n=+\infty$（参见 7.2.1.1，2. 调和级数）。

## 复算

1. **$x^{(n)}\in\ell^1$**：$\sum_{k=1}^n\tfrac1k$ 为有限和 ✓
2. **柯西性**：对 $m>n$，
$$
\rho(x^{(n)},x^{(m)})=\sup_k\lvert x^{(n)}_k-x^{(m)}_k\rvert=\sup_{n<k\le m}\tfrac1k=\tfrac1{n+1}\longrightarrow 0\quad(n\to\infty)\ ✓
$$
3. **不收敛**：若存在 $x\in\ell^1$ 使 $\rho(x^{(n)},x)\to0$，则逐坐标 $x_k=\lim_n x^{(n)}_k=\tfrac1k$，故 $x=(1,\tfrac12,\tfrac13,\dots)$；但 $\sum_k\tfrac1k=+\infty$，$x\notin\ell^1$，矛盾 ✓
4. **归因**：不完备属于二元组 $(\ell^1,\ (12.46)\ \sup\text{距离})$；$(\ell^1,\ \ell^1\text{-距离}\ (12.47))$ 仍完备（本节完备空间清单）——完备性依赖距离而非仅依赖集合，见 [[comparisons/lp空间两种距离完备性比较]]。

## 备注

该反例同时演示了「收敛⇒柯西、逆不成立」与完备化的动机（坐标极限 $x^{(0)}$ 生活在更大空间中，见 [[concepts/距离空间的完备化]]）。复算全部通过，可信度高。