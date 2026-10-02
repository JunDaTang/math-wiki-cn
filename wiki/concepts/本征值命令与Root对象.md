---
type: concept
title: 本征值命令与 Root 对象（Eigenvalues、Eigenvectors、Eigensystem）
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 本征值, Root对象, 希尔伯特矩阵]
related: [mathematica, Mathematica矩阵与向量运算, 希尔伯特矩阵与条件数警告]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---
# 本征值命令与 Root 对象（Eigenvalues、Eigenvectors、Eigensystem）

Mathematica 确定矩阵本征值与本征向量的命令族（理论背景回指第 421 4.6）：Eigenvalues[m] 生成方阵 m 的本征值的一个列表，Eigenvectors[m] 创建 m 的特征向量的一个列表，Eigensystem[m] 则给出两者。如果 N[m] 被用来代替 m，那么将得到数值特征值。

## n > 4 界限与 Root 对象

一般来说，如果矩阵的阶数大于四（n > 4），则得不到任何代数表达式，因为特征多项式的次数大于四；在这种情形，应该求数值特征值。符号计算返回 Root[...] 对象——精确但非显式的表示，源称这类答案「可能是没用的」。

## 希尔伯特矩阵例（H₅）

```text
In[1] := h = Table[1/(i + j - 1), {i, 5}, {j, 5}]      → 五维所谓希尔伯特矩阵
In[2] := Eigenvalues[h]
Out[2] = {Root[-1 + 307505 #1 - 1022881200 #1² + …]}
Out[3] = {1.56705, 0.208534, 0.0114075, 0.000305898, 3.28793×10⁻⁶}
```

（Out[3] 之前疑脱 In[3] := Eigenvalues[N[h]]，见 [[queries/希尔伯特Out3前疑脱In3之辨]]。）

数值谱与已知值一致；Root 多项式系数经独立验证：307505 = tr(H₅⁻¹)（H₅⁻¹ 对角元 25+4800+79380+179200+44100 之和，即本征值倒数之和）、1022881200 = e₃/e₅（本征值倒数之成对和）。谱比 λmax/λmin = 1.56705/3.28793×10⁻⁶ ≈ 4.8×10⁵，定量印证希尔伯特矩阵的病态性（见 [[concepts/希尔伯特矩阵与条件数警告]]）。

## 关联

算例复算（含 Root 系数验证）见 [[findings/20-3-3线性方程组与本征值算例复算]]；关联 [[concepts/Mathematica矩阵与向量运算]]。