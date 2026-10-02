---
type: finding
title: quad 与 quadl 求值次数复算
created: 2026-10-02
updated: 2026-10-02
tags: [复算, 数值积分, Matlab, 自适应求积]
related: [10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm, matlab, quad与quadl自适应求积]
source: "10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/19.8.4 交互程序系统和计算机代数系统的应用.md"]
---
# quad 与 quadl 求值次数复算

## 摘要

两组对照算例给出 quad（自适应辛普森）与 quadl（高阶洛巴托）的函数求值次数与积分值；积分值经已知常数（Si(1)、√π）复算证实，求值次数为软件输出转录。

## 算例 1：I = ∫₀¹ (sin x)/x dx（正弦积分，回指 8.2.5,1）

```txt
>> format long; [I, fwerte] = quad(@(x)(sin(x)./x), 0, 1)
I = 0.94608307007653    fwerte = 14
>> format long; [I, fwerte] = quadl(@(x)(sin(x)./x), 0, 1)
I = 0.94608307036718    fwerte = 19
>> format long; [I, fwerte] = quad(@(x)(sin(x)./x), 0, 1, 1e-14)
I = 0.94608307036718    fwerte = 258
>> format long; [I, fwerte] = quadl(@(x)(sin(x)./x), 0, 1, 1e-14)
I = 0.94608307036718    fwerte = 19
```

（quad 与 quadl 首次调用均伴随 "Warning: Divide by zero"，两程序都认知被积函数在区间左端的不连续性，但得到积分近似值并无困难。）

复算：Si(1) = 0.946083070367183（已知值），与两程序在容差 10⁻¹⁴ 下的输出 0.94608307036718 一致；quad 默认容差（10⁻⁶）下的输出 0.94608307007653 末数位偏差与其低阶公式相容。**积分值证实**；求值次数（14/19；258/19）为软件输出转录，未独立复算。

## 算例 2：I = ∫₋₁₀₀₀¹⁰⁰⁰ e^(−x²) dx

```txt
>> format long; [I, fwerte] = quad(@(x)(exp(-x.^2)), -1000, 1000, 1e-10)
I = 1.77245385094233    fwerte = 585
>> format long; [I, fwerte] = quadl(@(x)(exp(-x.^2)), -1000, 1000, 1e-10)
I = 1.77245385090571    fwerte = 768
```

复算：√π = 1.772453850905516；quadl 值偏差约 2×10⁻¹³，quad 值偏差约 3.7×10⁻¹¹，均在容差 10⁻¹⁰ 内。**积分值证实**。

## 结论（据本源）

- 光滑被积函数 + 高精度要求（例 1，容差 10⁻¹⁴）：quad 需 258 次、quadl 仅 19 次——quadl 的优越性显然；
- 平坦区间 + 陡峭峰值（例 2，x=0 处峰值）：quad 585 次、quadl 768 次——quad 较好。

## 开放问题

求值次数能否在现代版本复现待查（quadl 在现代 Matlab 中已被替代程序取代）。见 [[concepts/quad与quadl自适应求积]]、[[comparisons/quad与quadl比较]]。

## 置信

confidence: high；replicated: true（积分值经 Si(1) 与 √π 两个独立已知常数证实）。