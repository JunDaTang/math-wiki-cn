---
type: concept
title: Euler 反射公式型积分
created: 2026-10-02
updated: 2026-10-02
tags: [反常积分, Beta函数, 定积分]
related: [Beta函数（第一型欧拉积分）, Cauchy主值, 条件46与47条件疑脱下界0之辨]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
---
# Euler 反射公式型积分

指值由 Euler 反射公式 Γ(a)Γ(1−a)=π/sin πa（经 B(1−a,a)）决定的幂-有理反常积分族。

## 手册 21.8.4（21.46–21.48）

- **21.46**：$\int_0^\infty\frac{dx}{(1+x)x^a}=\frac{\pi}{\sin a\pi}$（原文条件 a<1 不完整，应 0<a<1：x→0 需 a<1、x→∞ 需 a>0；a=0 时退化为 ∫dx/(1+x) 发散）
- **21.47**：$\int_0^\infty\frac{dx}{(1-x)x^a}=-\pi\cot a\pi$（同需 0<a<1；x=1 处一阶极点，值经 [[Cauchy主值]] $\mathrm{PV}\int_0^\infty\frac{x^{s-1}}{1-x}dx=\pi\cot\pi s$（s=1−a）证实）
- **21.48**：$\int_0^\infty\frac{x^{a-1}}{1+x^b}dx=\frac{\pi}{b\sin\frac{a\pi}{b}}$（0<a<b，一般化）

机制：$\int_0^\infty\frac{x^{-a}}{1+x}dx=B(1-a,a)=\Gamma(1-a)\Gamma(a)=\frac{\pi}{\sin\pi a}$，与 [[Beta函数（第一型欧拉积分）]] 直接相连。

条件与主值问题见 [[条目46与47条件疑脱下界0之辨]]。