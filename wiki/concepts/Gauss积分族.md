---
type: concept
title: Gauss 积分族
created: 2026-10-02
updated: 2026-10-02
tags: [反常积分, 定积分, 概率核]
related: [Gamma函数（第二型欧拉积分）, Fresnel积分, 定积分表]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
---
# Gauss 积分族

Gauss 积分族指 e^{−a²x²} 及其 cos bx 调制、x^n 加权的定积分族，基准值 $\int_{-\infty}^{\infty}e^{-x^2}dx=\sqrt{\pi}$（可独立验证的背景知识）。

## 手册 21.8.2（21.23–21.27）

- **21.23a**：$\int_0^\infty x^ne^{-ax}dx=\frac{\Gamma(n+1)}{a^{n+1}}$（a>0, n>−1；n 非负整数时 = n!/a^{n+1}）——本小节的 Γ 换元基础
- **21.24a–c**：$\int_0^\infty x^ne^{-ax^2}dx=\frac{\Gamma(\frac{n+1}{2})}{2a^{(n+1)/2}}$；n=2k 支 $=\frac{1\cdot3\cdots(2k-1)\sqrt{\pi}}{2^{k+1}a^{k+1/2}}$，n=2k+1 支 $=\frac{k!}{2a^{k+1}}$
- **21.25**：$\int_0^\infty e^{-a^2x^2}dx=\frac{\sqrt{\pi}}{2a}$
- **21.26**：$\int_0^\infty x^2e^{-a^2x^2}dx=\frac{\sqrt{\pi}}{4a^3}$
- **21.27**：$\int_0^\infty e^{-a^2x^2}\cos bx\,dx=\frac{\sqrt{\pi}}{2a}\,e^{-b^2/4a^2}$（a>0）

复算：Γ 换元（t=ax²）、对参数求导递推（21.26 由 21.25 对 a 求导）、配方（21.27），全部成立；21.24a 取 n=0 与 21.25（参数记法 a↔a²）一致。

## 关联

[[Gamma函数（第二型欧拉积分）]] 提供 21.24a 的统一闭式；经复旋转与 [[Fresnel积分]] 相连。