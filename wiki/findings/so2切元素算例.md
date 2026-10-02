---
type: finding
title: "so(2) 切元素算例（式 5.153，已复算）"
created: 2026-09-30
updated: 2026-09-30
tags: [so2, 李代数, 切元素, 指数映射, 已复算]
related: [so2-二维旋转群, 李代数, 指数映射, 由切元素求李代数流程, 李群与李代数对应比较]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
source: "[[10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]]"
confidence: high
replicated: true
---
# so(2) 切元素算例（式 5.153，已复算）

## 陈述与复算
与李群 SO(2) 相伴的李代数 so(2) 从 SO(2) 的表示 g(θ) 借助于切元素算出（式 5.153a）：

$$
\frac{\mathrm{d}g}{\mathrm{d}\theta}g^{-1}\bigg|_{\theta=0}
=\begin{pmatrix}-\sin\theta&-\cos\theta\\ \cos\theta&-\sin\theta\end{pmatrix}
\begin{pmatrix}\cos\theta&\sin\theta\\ -\sin\theta&\cos\theta\end{pmatrix}
=\begin{pmatrix}0&-1\\1&0\end{pmatrix}
$$

独立复算：该矩阵乘积对**所有** θ 恒等于 [[0,−1],[1,0]]（逐项：(1,1)=−sinθcosθ+cosθsinθ=0；(1,2)=−sin²θ−cos²θ=−1；(2,1)=cos²θ+sin²θ=1；(2,2)=cosθsinθ−sinθcosθ=0），不只在 θ=0 处成立。故（式 5.153b）：

$$
\operatorname{so}(2)=\left\{s\begin{pmatrix}0&-1\\1&0\end{pmatrix},\ s\in\mathbb{R}\right\}
$$

反向验证（式 5.153c）：从 X=[[0,−1],[1,0]] 得

$$
\mathrm{e}^{sX}=\cos s\begin{pmatrix}1&0\\0&1\end{pmatrix}+\sin s\begin{pmatrix}0&-1\\1&0\end{pmatrix}
=\begin{pmatrix}\cos s&-\sin s\\ \sin s&\cos s\end{pmatrix}
$$

即指数映射由李代数恢复整个旋转群（满射），复算通过。

## 意义
本算例是 [[methodology/由切元素求李代数流程]] 的范式，也是 [[concepts/指数映射]] 群–代数对应的最小实例；详见 [[comparisons/李群与李代数对应比较]]。
