---
type: finding
title: "SE(3) 六变换矩阵与齐次坐标作用（式 5.145–5.146，已复核）"
created: 2026-09-30
updated: 2026-09-30
tags: [se3, 刚体运动, 齐次坐标, 变换矩阵, 已复核]
related: [se-n特殊欧几里得群, 齐次坐标, 齐次坐标变换矩阵构造流程, so3与se3标准基与log-exp插值, 5-3-6全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
source: "[[10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]]"
confidence: high
replicated: true
---
# SE(3) 六变换矩阵与齐次坐标作用（式 5.145–5.146，已复核）

## 陈述
SE(3) 是 ℝ³ 中的刚体运动群。通常定义六个独立的变换：a)–c) 为三个方向的平移，d)–f) 为绕三个轴的旋转（转写中 x-/y-/z- 轴名脱落）。这些变换以三维齐次坐标 (x, y, z, 1)ᵀ 的 (4,4) 矩阵表示（式 5.145）：

$$
M_1=\begin{pmatrix}1&0&0&a\\0&1&0&0\\0&0&1&0\\0&0&0&1\end{pmatrix},\quad
M_2=\begin{pmatrix}1&0&0&0\\0&1&0&b\\0&0&1&0\\0&0&0&1\end{pmatrix},\quad
M_3=\begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&1&c\\0&0&0&1\end{pmatrix}
$$

$$
M_4=\begin{pmatrix}1&0&0&0\\0&\cos\alpha&-\sin\alpha&0\\0&\sin\alpha&\cos\alpha&0\\0&0&0&1\end{pmatrix},\quad
M_5=\begin{pmatrix}\cos\beta&0&\sin\beta&0\\0&1&0&0\\-\sin\beta&0&\cos\beta&0\\0&0&0&1\end{pmatrix},\quad
M_6=\begin{pmatrix}\cos\gamma&-\sin\gamma&0&0\\\sin\gamma&\cos\gamma&0&0\\0&0&1&0\\0&0&0&1\end{pmatrix}
$$

群作用（式 5.146）：

$$
\binom{\vec{x}'}{1}=\begin{pmatrix}\boldsymbol{R}&\vec{v}\\0&1\end{pmatrix}\binom{\vec{x}}{1}=\binom{\boldsymbol{R}\vec{x}+\vec{v}}{1}
$$

其中 R∈SO(3) 是旋转，v⃗=(a,b,c)ᵀ 是平移向量。矩阵 M₄、M₅、M₆ 刻画 ℝ³ 的旋转，因此 SO(3) 是 SE(3) 的子群。

## 复核结果
- 已验证：se(3) 生成元 E₄–E₆（式 5.156）恰为 M₄–M₆ 在单位元处（参数=0）的导数，与 5.3.6.4 的李代数构造交叉印证一致。
- 平移矩阵 M₁–M₃ 的结构（单位阵 + 末列平移向量）与作用式 (5.146) 一致。

## 转写注记
六变换 a)–f) 的轴向说明（x-/y-/z-）在转写中系统性脱落；齐次坐标的原始出处 3.5.4.2（p.310）未入库，见 [[queries/5-3-6未入库依赖缺口]]。
