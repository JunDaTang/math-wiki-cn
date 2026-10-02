---
type: concept
title: Mathematica 矩阵与向量运算
tags: [mathematica, 矩阵运算, 向量运算, 线性代数, Dot, Det, Inverse, Transpose, MatrixExp, MatrixPower, Eigenvalues, Eigenvectors]
related: [mathematica, Mathematica列表与向量矩阵表示, 依分量运算与矩阵运算比较, 算例A四阶符号矩阵转置与矩阵向量积复算, 算例B克拉默方程组逆矩阵求解复算, 表20-6首行ca疑脱乘号之辨, Matlab线性代数算例复算, Matlab-Mathematica-Maple同题数值比较]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.5 作为列表的向量和矩阵.md"]
---

# Mathematica 矩阵与向量运算

Mathematica 允许对矩阵和向量进行**形式（符号）操作**：运算对象既可以是数值矩阵，也可以是经 `Array` 构造的符号矩阵（见 [[Mathematica列表与向量矩阵表示]]）。本条目依据《数学手册（原书第10版）》20.2.5.2 与其表 20.6，汇总矩阵运算命令及行列向量的语义约定。

## 表 20.6 矩阵的运算

| 命令 | 含义 |
|---|---|
| c*a（原文作「ca」，疑脱乘号） | 用标量 c 乘矩阵 a |
| a.b | 矩阵 a 和 b 的乘积 |
| Det[a] | 矩阵 a 的行列式 |
| Inverse[a] | 矩阵 a 的逆 |
| Transpose[a] | 矩阵 a 的转置 |
| MatrixExp[a] | 矩阵 a 的指数函数 |
| MatrixPower[a, n] | 矩阵 a 的 n 次幂 |
| Eigenvalues[a] | 矩阵 a 的本征值 |
| Eigenvectors[a] | 矩阵 a 的本征向量 |

（「本征值/本征向量」为物理学传统译名，通行译名作「特征值/特征向量」。首行之辨见 [[表20-6首行ca疑脱乘号之辨]]。）

## 行向量与列向量不作区分

Mathematica 中对于行向量和列向量不做区分：

- `r.v` 相应于线性代数中一个矩阵被一个**列向量右乘**时的乘积；
- `v.r` 的意思是被一个**行向量左乘**；
- 矩阵与向量的乘积仍是一个向量。

由于矩阵的乘法一般不是交换的（原书回指 4.1.4「矩阵的计算」，第 365 页），`.` 两侧操作数的位置决定语义。

## 与依分量运算之辨

`a.b`（矩阵乘积）与 `MatrixExp[a]`（矩阵指数）须同 `a*b`（依分量乘积）与 `Exp[a]`（依分量指数）严格区分，详见 [[依分量运算与矩阵运算比较]]。

## 算例

- **算例 A**：`r = Array[a,{4,4}]` 的 `Transpose[r]` 与 `r.v`（`v = Array[u,4]`），演示符号矩阵的形式运算，逐项复算通过（[[算例A四阶符号矩阵转置与矩阵向量积复算]]）。
- **算例 B**：克拉默法则方程组 p·t = b，`Det[p] = 13 ≠ 0`，解 `t = p⁻¹b = {−1, 2, 3}`，复算通过；原文 In[4] 作 `Inverse[p]` 疑脱「.b」（[[算例B克拉默方程组逆矩阵求解复算]]、[[In4之Inverse-p与Out4解向量不对应疑脱点b之辨]]）。

## 跨系统视角

算例 B 的方程组适合作 Matlab、Mathematica、Maple 同题比较素材，参见 [[Matlab线性代数算例复算]] 与 [[Matlab-Mathematica-Maple同题数值比较]]。