---
type: finding
title: "螺旋导数与 se(3) 一般元素（式 5.170–5.172，已复核）"
created: 2026-09-30
updated: 2026-09-30
tags: [se3, 螺旋运动, 反对称矩阵, 向量积, 角速度, 已复核]
related: [se-n特殊欧几里得群, 李代数, 沙勒定理与螺旋运动, so3与se3标准基与log-exp插值, 李群与李代数对应比较, 5-3-6全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
source: "[[10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]]"
confidence: high
replicated: true
---
# 螺旋导数与 se(3) 一般元素（式 5.170–5.172，已复核）

## 陈述
螺旋运动 A(θ)（式 5.170，同 5.166）由角 θ 参数化刚体运动；θ=0 给出恒等变换。在 θ=0 处求导得 se(3) 的一般元素（式 5.171a）：

$$
\boldsymbol{S}=\frac{\mathrm{d}A}{\mathrm{d}\theta}\bigg|_{\theta=0}
=\begin{pmatrix}\boldsymbol{\Omega}&\frac{p}{2\pi}\vec{x}-\boldsymbol{\Omega}\vec{u}\\0&0\end{pmatrix}
$$

（所印 (5.171a) 末项保留 θ，疑未消去——求导后应为 (p/2π)x⃗，见 [[queries/5-3-6全节系统性转写讹误清单]]。）其中 Ω=dR/dθ(0) 是斜对称矩阵：因 R 正交，RRᵀ=I，求导得 (dR/dθ)Rᵀ+R(dR/dθ)ᵀ=0（式 5.171b）；θ=0 时 R=I，故 dR/dθ(0)+dR/dθ(0)ᵀ=0（式 5.171c）。

每个斜对称矩阵（式 5.171d）：

$$
\boldsymbol{\Omega}=\begin{pmatrix}0&-\omega_z&\omega_y\\ \omega_z&0&-\omega_x\\ -\omega_y&\omega_x&0\end{pmatrix}
$$

可以等同于向量 ω⃗ᵀ=(ω_x, ω_y, ω_z)；用 Ω 乘任何三维向量 p⃗ 对应于与向量 ω⃗ 的向量积（式 5.171e）：Ωp⃗=ω⃗×p⃗。从而 ω⃗ 是刚体运动的角速度。因此 se(3) 的一般元素有形式（式 5.171f）：

$$
\boldsymbol{S}=\begin{pmatrix}\boldsymbol{\Omega}&\vec{v}\\0&0\end{pmatrix}
$$

这些矩阵形成一个六维向量空间，它们通常等同于形如 s⃗=(ω⃗, v⃗)ᵀ 的六维向量（式 5.172）。

## 复核结果
- (5.171b)–(5.171c)：对 RRᵀ=I 求导并在 θ=0 赋值，复核成立 ✓。
- (5.171e)：用 p⃗=e₁ 验证 Ωe₁=(0, ω_z, −ω_y)ᵀ = ω⃗×e₁ ✓（一般 p⃗ 由线性性成立）。
- (5.171a) 末项：d/dθ[(θp/2π)x⃗]=(p/2π)x⃗，所印保留 θ 疑误；d/dθ[(I−R)ū]=−Ωū 部分无误。

## 意义
此推导把 se(3) 的矩阵元素与物理量（角速度 ω⃗、速度 v⃗）联系起来，是螺旋/机器人学中六维速度向量 s⃗ 的来源；对应表见 [[comparisons/李群与李代数对应比较]]。
