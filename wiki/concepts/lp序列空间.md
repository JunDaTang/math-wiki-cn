---
type: concept
title: "ℓ^p 空间（序列空间）"
created: 2026-10-01
updated: 2026-10-01
tags: [泛函分析, 序列空间, 距离空间, 完备性, 可分性]
related: [距离空间, 柯西序列与完备距离空间, 稠密集与可分距离空间, Lp函数空间]
sources: ["数学手册(原书第10版)/12.2 距离空间.md"]
---

# ℓ^p 空间（序列空间）

$\ell^p$（$1\le p<\infty$）是由 $p$-绝对可求和数列构成的距离空间：其元素是使级数 $\sum_{k=1}^\infty\lvert\xi_k\rvert^p$ 收敛的序列 $x=(\xi_1,\xi_2,\dots)$，距离定义为

$$
\rho(x,y)=\sqrt[p]{\sum_{k=1}^{\infty}\lvert\xi_k-\eta_k\rvert^{p}},\quad x,y\in\ell^p.\tag{12.47}
$$

（源文称 $\sum\lvert\xi_k\rvert^p$「绝对收敛」；因项非负，「收敛」即足，术语小瑕。）

## 本节论断

- **完备性**：$\ell^p$（$1\le p<\infty$）列入本节完备空间清单，是完备距离空间；
- **可分性**：$\ell^1$ 可分——所有含有理分量、形如 $x=(r_1,r_2,\dots,r_N,0,0,\dots)$（$N=N(x)$ 任意自然数）的点集是可数稠密集（源文「空间 $\ell=\ell^1$ 也是可分的」中「$\ell=\ell^1$」记法疑衍文，见 [[queries/12-2全节系统性转写讹误清单]]）；
- **关键反例的舞台**：在同一集合 $\ell^1$ 上改赋 $m$ 的距离 (12.46)（$\sup_k\lvert\xi_k-\eta_k\rvert$）后，空间**不再完备**：$x^{(n)}=(1,\tfrac12,\dots,\tfrac1n,0,\dots)$ 是不收敛的柯西列。完备性是（集合，距离）二元组的属性，见 [[comparisons/lp空间两种距离完备性比较]] 与 [[findings/式12-56柯西序列与lp上sup距离不完备反例复算]]。

## 联系

$\ell^p$ 是 $L^p(\Omega)$（[[concepts/Lp函数空间]]）在计数测度下的序列类比；序列空间族 $m$、$c$、$c_0$（距离 (12.46)）的定义在 12.1，尚未入库（见 [[queries/12-2未入库回指缺口]]）。