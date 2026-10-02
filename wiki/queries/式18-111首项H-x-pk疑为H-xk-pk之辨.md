---
type: query
title: "式 18.111 首项 H(x, p_k) 疑为 H(x^k, p_k) 之辨"
tags: [转写讹误, 罚函数法, 公式之辨, 18-2-8]
related: [罚函数法, 10-数学手册原书第10版--15-1828-罚函数法和障碍函数法--fyuzln]
created: 2026-10-01
updated: 2026-10-01
sources: ["数学手册(原书第10版)/18.2.8 罚函数法和障碍函数法.md"]
---
# 式 18.111 首项 H(x, p_k) 疑为 H(x^k, p_k) 之辨

## 疑点

原文（设 $\underline{\boldsymbol{x}}^k$ 为第 $k$ 个罚问题的解）：

$$
H(\underline{\boldsymbol{x}},p_k)\geqslant H(\underline{\boldsymbol{x}}^{k-1},p_{k-1}),\quad f(\underline{\boldsymbol{x}}^k)\geqslant f(\underline{\boldsymbol{x}}^{k-1}),
$$

首项自变量 $\underline{\boldsymbol{x}}$ 无上标，而其余三项均带解点上标。

## 两种读法

1. **字面**（对任意 $\underline{\boldsymbol{x}}\in\mathbb{R}^n$）：即最优值单调——$\min_{\underline{\boldsymbol{z}}}H(\underline{\boldsymbol{z}},p_k)\geqslant H(\underline{\boldsymbol{x}}^{k-1},p_{k-1})$。此读法为真：因 $S\geqslant 0$ 且 $p_k>p_{k-1}$，对一切 $\underline{\boldsymbol{x}}$ 有 $H(\underline{\boldsymbol{x}},p_k)\geqslant H(\underline{\boldsymbol{x}},p_{k-1})\geqslant\min_{\underline{\boldsymbol{z}}}H(\underline{\boldsymbol{z}},p_{k-1})$。
2. **补上标**（通行表述）：$H(\underline{\boldsymbol{x}}^k,p_k)\geqslant H(\underline{\boldsymbol{x}}^{k-1},p_{k-1})$，即第 $k$ 个罚问题的最优值（在解点处取得）不低于第 $k-1$ 个。因 $\underline{\boldsymbol{x}}^k$ 达到最小值，两种读法可互相推出，数学上等价。

## 分析

两种读法皆真且等价，差别只在表述；疑为 OCR 脱上标 $k$（本节多处同类脱上标，见 [[queries/18-2-8全节系统性转写讹误清单]]）。通行文献多取带解点上标的形式，与后项 $H(\underline{\boldsymbol{x}}^{k-1},p_{k-1})$ 对仗。

## 状态

开放：待对原书影印件核字以定表述（两种读法数学上皆成立，不影响实质）。