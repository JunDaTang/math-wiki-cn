---
type: entity
title: "SO(2)（二维旋转群）"
created: 2026-09-30
updated: 2026-09-30
tags: [矩阵李群, 李群, 旋转群, 连续群]
related: [矩阵李群, 连续群, 李代数, 指数映射, se-n特殊欧几里得群, c-n循环点群, 典型矩阵群gln-sln-on-son-un-sun, 二维旋转群falk乘法算例, so2切元素算例]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
---
# SO(2)（二维旋转群）

SO(2) 是 ℝ² 中绕原点的全部旋转在矩阵乘法下构成的群，是一个 1 维矩阵李群。其元素由旋转角 φ 唯一参数化（本源式 5.138、5.142）：

$$
\operatorname{SO}(2)=\left\{\begin{pmatrix}\cos\varphi&-\sin\varphi\\ \sin\varphi&\cos\varphi\end{pmatrix},\ \varphi\in\mathbb{R}\right\}
$$

## 群结构与维数
- 乘法由加法定理给出：a(φ₁)a(φ₂)=a(φ₃)，φ₃=f(φ₁,φ₂)=φ₁+φ₂；本源用 Falk 式逐元素列出乘法表算例（式 5.139），已独立复算通过（见 [[findings/二维旋转群falk乘法算例]]）。
- 群元素仅依赖一个实参数 φ，故维数为 1（本源 5.3.6.2.3(3) 例 B；转写中维数「1」脱落）。

## 李代数 so(2)
由切元素算出（式 5.153，已复算，见 [[findings/so2切元素算例]]）：

$$
\operatorname{so}(2)=\left\{s\begin{pmatrix}0&-1\\1&0\end{pmatrix},\ s\in\mathbb{R}\right\},\qquad
\mathrm{e}^{sX}=\cos s\begin{pmatrix}1&0\\0&1\end{pmatrix}+\sin s\begin{pmatrix}0&-1\\1&0\end{pmatrix}
$$

指数映射 so(2)→SO(2) 满射，即李代数元素经指数函数参数化整个群。计算流程见 [[methodology/由切元素求李代数流程]]。

## 与有限群论的桥接
5.3.4 中 C₃ 的二维旋转表示矩阵（见 [[findings/c3二维旋转表示算例]]）即取 φ 为 2π/3 整数倍处的 SO(2) 元素；一般地，循环点群 [[entities/c-n循环点群|C_n]] 可视为 SO(2) 的有限子群。SO(2) 由此成为离散表示论（[[concepts/群表示]]）与连续群之间的桥梁。

## 出处
[[sources/10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]] 5.3.6.2.3(3) 例 B、5.3.6.2.4 F、5.3.6.4.4 例 A。
