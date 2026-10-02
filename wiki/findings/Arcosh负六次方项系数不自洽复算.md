---
type: finding
title: "Arcosh 负六次方项系数不自洽复算"
created: 2026-10-02
updated: 2026-10-02
tags: [复算, 反双曲函数, Arcosh, 渐近展开, 转写讹误, 数学手册]
related: [面积函数与Ar-记法, Arcosh第三项分母疑脱6之辨, 21-5全表级数系数与通项复算]
sources: ["数学手册(原书第10版)/21.5 重要级数展开.md"]
source: "[[10-数学手册原书第10版--10-215-重要级数展开--1gmcxgd]]"
confidence: high
replicated: true
---

# Arcosh 负六次方项系数不自洽复算

[[sources/10-数学手册原书第10版--10-215-重要级数展开--1gmcxgd]] 面积函数块 $\Arcosh x$ 行的 $x^{-6}$ 项系数与复算真值不自洽。原文（照录）：

```latex
\text{Arcosh}\,x = \pm\left[\ln(2x) - \frac{1}{2\cdot 2x^{2}} - \frac{1\cdot 3}{2\cdot 4\cdot 4x^{4}} - \frac{1\cdot 3\cdot 5}{2\cdot 4\cdot 6x^{6}} - \cdots\right],\quad x > 1
```

## 复算

真值为 $\Arcosh x=\ln(2x)-\sum_{n\ge1}\frac{(2n-1)!!}{(2n)!!\cdot 2n}\,x^{-2n}$，分母呈「$(2n)!!\times 2n$」模式：

- $n=1$：$\frac{1}{2\cdot2x^2}=\frac{1}{4x^2}$ ✓（表中作 $2\cdot2$，即 $2!!\times2$）；
- $n=2$：$\frac{1\cdot3}{2\cdot4\cdot4x^4}=\frac{3}{32x^4}$ ✓（$4!!\times4$）；
- $n=3$：真值应为 $\frac{1\cdot3\cdot5}{2\cdot4\cdot6\cdot6x^6}=\frac{5}{96x^6}$；表中作 $\frac{1\cdot3\cdot5}{2\cdot4\cdot6x^6}=\frac{5}{16x^6}$，恰差一个因子 6；
- $n=4$ 佐证：真值 $\frac{1\cdot3\cdot5\cdot7}{2\cdot4\cdot6\cdot8\cdot8x^8}=\frac{35}{1024x^8}$，与「$(2n)!!\times 2n$」模式一致，进一步锁定 $n=3$ 项脱漏。

## 结论与范围

表中 $x^{-6}$ 项分母疑脱「·6」。该不自洽属转写脱字还是刊本排印原误未定，见 [[queries/Arcosh第三项分母疑脱6之辨]]。本 finding 仅涉及该行，不影响同表其他行（[[findings/21-5全表级数系数与通项复算]]）。

复算状态：经通式模式与 $x^{-8}$ 项两条独立路径互证，replicated: true。