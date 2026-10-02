---
type: finding
title: "GF(pⁿ) 中的 Frobenius 恒等式（式 5.180）"
created: 2026-09-30
updated: 2026-09-30
tags: [代数, 环和域, 有限域, 环的特征]
related: [伽罗瓦域gf-pn, 环的特征, 域扩张]
sources: ["数学手册(原书第10版)/5.3.7 环和域.md"]
source: "[[10-数学手册原书第10版--7-537-环和域--3j0nhk]]"
confidence: high
replicated: true
---
# GF(pⁿ) 中的 Frobenius 恒等式（式 5.180）

数学手册 5.3.7.4.1（4）给出 GF(pⁿ) 中的有用计算法则：

$$(a + b)^{p^r} = a^{p^r} + b^{p^r}, \quad r \in \mathbb{N}. \tag{5.180}$$

源文未给该式命名；通行文献中此式称为 Frobenius 恒等式（独立可查的背景命名），它是特征 p 域的标志性性质，即「p 次幂映射保持加法」的体现。

## 复核说明

✓ 由二项式定理：$(a+b)^p$ 展开中系数 $\binom{p}{k}$（$0 < k < p$）均被素数 $p$ 整除，在特征 p 的域中相应项为零，得 $r = 1$ 情形；对 $p^r$ 次幂迭代即得一般 $r$。与 GF(2³)（特征 2）实例一致：$(a+b)^2 = a^2 + b^2$。

## 意义与联系

- 与 [[concepts/环的特征]]（整区特征为 0 或素数）相衔接：恒等式成立正因 GF(pⁿ) 的特征是 p；
- 在本节中它紧邻 $\mathrm{GF}(p^n) = \mathbb{Z}_p(\alpha)$ 的分裂域讨论（见 [[findings/kx-fx-商环构造与gf-pn]]）。载体实体页：[[entities/伽罗瓦域gf-pn]]。