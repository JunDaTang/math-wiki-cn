---
type: finding
title: "GA(2) 与 P(2) 生成元组（式 5.147）"
created: 2026-09-30
updated: 2026-09-30
tags: [ga2, 仿射变换, 射影变换, 生成元, 机器视觉, 疑误]
related: [ga2-二维仿射变换群, 齐次坐标, se-n特殊欧几里得群, sim-n标度欧几里得群, 式5-147b-m6是否应为双曲旋转]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
source: "[[10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]]"
confidence: medium
replicated: true
---
# GA(2) 与 P(2) 生成元组（式 5.147）

## 陈述
GA(2)（二维仿射变换群，六维）的变换以齐次坐标 (x, y, 1)ᵀ 的 (3,3) 矩阵刻画（式 5.147a–b）：

$$
M_1=\begin{pmatrix}1&0&a\\0&1&0\\0&0&1\end{pmatrix},\quad
M_2=\begin{pmatrix}1&0&0\\0&1&b\\0&0&1\end{pmatrix},\quad
M_3=\begin{pmatrix}\cos\alpha&-\sin\alpha&0\\\sin\alpha&\cos\alpha&0\\0&0&1\end{pmatrix}
$$

$$
M_4=\begin{pmatrix}\mathrm{e}^{\tau}&0&0\\0&\mathrm{e}^{\tau}&0\\0&0&1\end{pmatrix},\quad
M_5=\begin{pmatrix}\mathrm{e}^{\mu}&0&0\\0&\mathrm{e}^{-\mu}&0\\0&0&1\end{pmatrix},\quad
M_6=\begin{pmatrix}\cosh\nu&-\sinh\nu&0\\\sinh\nu&\cosh\nu&0\\0&0&1\end{pmatrix}\ \text{（疑误）}
$$

射影群 P(2) 由 M₁–M₆ 及另两个矩阵生成（式 5.147c）：

$$
M_7=\begin{pmatrix}1&0&0\\0&1&0\\\beta&0&1\end{pmatrix},\qquad
M_8=\begin{pmatrix}1&0&0\\0&1&0\\0&\gamma&1\end{pmatrix}
$$

M₇、M₈ 对应于水平线的变化或平面图形边缘的消失。本质子群链：M₁、M₂（平移群）⊂ M₁–M₃（欧几里得群 SE(2)）⊂ M₁–M₄（相似群，即 SIM(2)）⊂ GA(2)。

## 验证状态
- M₁–M₅ 复核通过：均为单参数子群（M₁、M₂ 平移；M₃ 旋转；M₄ 一致伸缩；M₅ 双曲伸缩 diag(e^μ, e^{−μ})，det=1）。
- M₆ 按所印符号不构成单参数子群：[[cosh ν, −sinh ν],[sinh ν, cosh ν]] 满足 M₆(ν)M₆(μ)≠M₆(ν+μ)，且 det=cosh²ν+sinh²ν=cosh 2ν≠1；(1,2) 元疑应为 +sinh ν（标准双曲旋转，det=1），见 [[queries/式5-147b-m6是否应为双曲旋转]]。
- M₇、M₈ 的底行 (β, 0)、(0, γ) 突破仿射形式（仿射变换底行应为 (0,0,1)），属射影变换，与 P(2) 的定位一致。

因 M₆ 存疑，整体 confidence 取 medium。应用背景：GA(2) 刻画平面刚体被移动照相机记录时的微小角度形变；大透视角时改用 P(2)。
