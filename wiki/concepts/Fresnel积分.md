---
type: concept
title: Fresnel 积分
created: 2026-10-02
updated: 2026-10-02
tags: [反常积分, 特殊函数, 定积分]
related: [Gamma函数（第二型欧拉积分）, Gauss积分族, 定积分表]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
---
# Fresnel 积分

Fresnel 积分指 sin(x²)、cos(x²) 的条件收敛反常积分，经典值 $\int_{-\infty}^{+\infty}\sin(x^2)dx=\int_{-\infty}^{+\infty}\cos(x^2)dx=\sqrt{\pi/2}$。

## 手册 21.8.1（21.13、21.17）

- **21.13**：$\int_0^\infty\frac{\sin x}{\sqrt x}dx=\int_0^\infty\frac{\cos x}{\sqrt x}dx=\sqrt{\frac{\pi}{2}}$
- **21.17**：$\int_{-\infty}^{+\infty}\sin(x^2)dx=\int_{-\infty}^{+\infty}\cos(x^2)dx=\sqrt{\frac{\pi}{2}}$

两式经 x=t² 换元相通（21.13 = 2×半轴 Fresnel 积分，21.17 = 2×半轴，二者相容）。复算：经 Γ(½)=√π 与旋转 π/4（sin(π/4) 因子）的解析延拓、分部积分与已知值交叉，成立。

## 关联

与 [[Gamma函数（第二型欧拉积分）]]（Γ(½)）和 [[Gauss积分族]]（经复平面旋转 e^{−x²}→e^{−ix²}）相连。