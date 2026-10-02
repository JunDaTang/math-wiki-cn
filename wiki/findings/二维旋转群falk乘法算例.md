---
type: finding
title: "二维旋转群 Falk 乘法算例（式 5.138–5.139，已复算）"
created: 2026-09-30
updated: 2026-09-30
tags: [so2, 旋转矩阵, 加法定理, Falk式, 已复算]
related: [so2-二维旋转群, 连续群, 群表与凯莱表, c-n循环点群, 5-3-6未入库依赖缺口]
sources: ["数学手册(原书第10版)/5.3.6 李群和李代数.md"]
source: "[[10-数学手册原书第10版--10-536-李群和李代数--i2rmm8]]"
confidence: high
replicated: true
---
# 二维旋转群 Falk 乘法算例（式 5.138–5.139，已复算）

## 陈述
ℝ² 中的旋转矩阵群（式 5.138）：

$$
D=\begin{pmatrix}\cos\varphi&-\sin\varphi\\ \sin\varphi&\cos\varphi\end{pmatrix}=a(\varphi),\quad 0\leqslant\varphi\leqslant 2\pi
$$

两个旋转矩阵 a(φ₁)、a(φ₂) 之积为 a₃=a(φ₁)*a(φ₂)=a(φ₃)，其中 φ₃=f(φ₁,φ₂)=φ₁+φ₂。本源以 Falk 式（原书 4.1.4.5，p.366，未入库）逐元素列出乘积表并援引加法定理。

## 复算结果（独立验证）
表中四个乘积元素逐格核对：
- (1,1)：cosφ₁cosφ₂−sinφ₁sinφ₂ = cos(φ₁+φ₂) ✓
- (1,2)：−cosφ₁sinφ₂−sinφ₁cosφ₂ = −sin(φ₁+φ₂) ✓
- (2,1)：sinφ₁cosφ₂+cosφ₁sinφ₂ = sin(φ₁+φ₂) ✓
- (2,2)：−sinφ₁sinφ₂+cosφ₁cosφ₂ = cos(φ₁+φ₂) ✓

加法定理逐格成立，φ₃=φ₁+φ₂ 无误。复算结论：算例正确。

## 意义
这是「连续群以参数函数 f（此处为向量加法）取代有限 [[concepts/群表与凯莱表]]」的最小算例；同一矩阵群即 [[entities/so2-二维旋转群|SO(2)]]，为 5.3.4 中 C₃ 二维旋转表示所在的连续群。
