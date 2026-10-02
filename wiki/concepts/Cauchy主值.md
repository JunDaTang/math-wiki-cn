---
type: concept
title: Cauchy 主值
created: 2026-10-02
updated: 2026-10-02
tags: [反常积分, 奇点, 定积分]
related: [Dirichlet积分与sinc型积分族, Euler反射公式型积分, 条目46与47条件疑脱下界0之辨]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
---
# Cauchy 主值

Cauchy 主值（PV）是对带内部奇点或无穷端点的积分取对称极限所得的广义值：$\mathrm{PV}\int_{-\infty}^{\infty}f=\lim_{R\to\infty}\int_{-R}^{R}f$；内部奇点 x₀ 处 $\mathrm{PV}\int=\lim_{\varepsilon\to0}\left[\int^{x_0-\varepsilon}+\int_{x_0+\varepsilon}\right]$。

## 在 21.8 中的隐含使用

手册 21.8 节未出现「主值」术语，但两条等式仅在此意义下成立：

- **21.10**：$\int_0^\infty\frac{\tan ax}{x}dx=\pm\frac{\pi}{2}$——tan ax 在正半轴有无穷多极点，通常反常积分不存在；上半平面围道复算 $\mathrm{PV}\int_{-\infty}^{\infty}\frac{\tan x}{x}dx=\pi$，半轴为 ±π/2，与表值一致。
- **21.47**：$\int_0^\infty\frac{dx}{(1-x)x^a}=-\pi\cot a\pi$——x=1 处一阶极点，值经 $\mathrm{PV}\int_0^\infty\frac{x^{s-1}}{1-x}dx=\pi\cot\pi s$（s=1−a）证实。

## 归属限定

主值解释仅属 21.10 与 21.47；21.8、21.11、21.12 等为通常收敛的反常积分，不得外推。开放问题：刊本是否对此二式标注主值（[[21-8全节系统性转写讹误清单]]）。