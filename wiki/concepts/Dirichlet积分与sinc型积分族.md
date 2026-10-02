---
type: concept
title: "Dirichlet 积分与 sinc 型积分族"
created: 2026-10-02
updated: 2026-10-02
tags: [反常积分, 傅里叶分析, 定积分]
related: [Cauchy主值, 傅里叶级数, 三角函数系正交性, 条目9上限α疑为∞之辨]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
---
# Dirichlet 积分与 sinc 型积分族

Dirichlet 积分 $\int_0^\infty\frac{\sin ax}{x}dx=\frac{\pi}{2}\operatorname{sgn}(a)$ 是 sinc 型核反常积分的原型；同族还包括 tan(ax)/x 的主值积分与 Frullani 型余弦差积分。

## 手册 21.8.1（21.8–21.12）

- **21.8**：$\int_0^\infty\frac{\sin ax}{x}dx=\pm\frac{\pi}{2}$（符号同 a）
- **21.9**：$\int_0^{\alpha}\frac{\cos ax\,dx}{x}=\infty$（α 取任意(正)数）——发散源于下限 0；上限之辨见 [[条目9上限α疑为∞之辨]]
- **21.10**：$\int_0^\infty\frac{\tan ax\,dx}{x}=\pm\frac{\pi}{2}$——被积函数在正半轴有无穷多极点，等式仅 [[Cauchy主值]] 意义下成立（上半平面围道复算 PV∫_{−∞}^{∞}tan x/x dx = π，半轴 ±π/2）
- **21.11**：$\int_0^\infty\frac{\cos ax-\cos bx}{x}dx=\ln\frac{b}{a}$（Frullani 余弦差；收敛需 a,b>0）
- **21.12**：$\int_0^\infty\frac{\sin x\cos ax}{x}dx=\begin{cases}\pi/2,&|a|<1\\ \pi/4,&|a|=1\\ 0,&|a|>1\end{cases}$

## 归属限定

主值解释仅属 21.10；21.8、21.11、21.12 为通常收敛的反常积分，不可移用主值说明。复算方法：Dirichlet 引理、Frullani 定理、留数/围道。

## 关联

可视为 [[三角函数系正交性]] 的周期核向非周期振荡核的延伸；Dirichlet 引理亦为 [[傅里叶级数]] 收敛理论的基本工具。