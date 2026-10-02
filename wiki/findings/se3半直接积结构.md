---
type: finding
title: "SE(3) 半直接积结构（式 5.160–5.161，已复核）"
created: 2026-09-30
updated: 2026-09-30
tags: [se3, 半直接积, 刚体运动, 机器人学, 已复核]
related: [半直接积, se-n特殊欧几里得群, 群的直积, 直接积与半直接积比较, 5-3-6全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
source: "[[10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]]"
confidence: high
replicated: true
---
# SE(3) 半直接积结构（式 5.160–5.161，已复核）

## 陈述
刻画 ℝ³ 中机器人运动的特殊欧几里得群 SE(3) 是群 SO(3)（绕原点的旋转）和 ℝ³（平移）的半直接积（式 5.160）：

$$
\operatorname{SE}(3)=\operatorname{SO}(3)\ltimes\mathbb{R}^3
$$

转写注记：原书 (5.160) 印作「×」，与正文「半直接积」的行文不符，疑为 ⋉ 之转写失真（见 [[queries/5-3-6全节系统性转写讹误清单]]）。在直接积中因子没有交互作用，但这里是半直接积，因为旋转在平移上的作用显然从矩阵乘法得到（式 5.161）：

$$
\begin{pmatrix}\boldsymbol{R}_2&\vec{t}_2\\0&1\end{pmatrix}
\begin{pmatrix}\boldsymbol{R}_1&\vec{t}_1\\0&1\end{pmatrix}
=\begin{pmatrix}\boldsymbol{R}_2\boldsymbol{R}_1&\boldsymbol{R}_2\vec{t}_1+\vec{t}_2\\0&1\end{pmatrix}
$$

即加第二个平移向量前第一个平移向量已被旋转。

## 复核结果
分块乘法逐块复核：左上块 R₂R₁、右上块 R₂t⃗₁+t⃗₂（末行 (0,0,0,1) 左乘贡献 t⃗₂）✓，与「旋转作用于平移」的半直接结构解释一致。

## 意义
这是 [[concepts/半直接积]] 相对 [[concepts/群的直积]]（5.3.3.9）的推广实例，对照见 [[comparisons/直接积与半直接积比较]]；机器人运动（5.3.6.5.1）以此为结构基础。
