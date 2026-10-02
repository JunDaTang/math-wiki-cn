---
type: methodology
title: 模糊关系矩阵的 sup-min 复合计算流程
created: 2026-09-30
updated: 2026-09-30
tags: [模糊关系, 关系复合, 计算流程, 数学手册]
related: [concepts/模糊关系的复合, concepts/模糊关系矩阵, concepts/t-范数, methodology/if-then模糊推理的复合计算流程, comparisons/三种复合方式比较]
sources: ["数学手册(原书第10版)/5.9.3 模糊值关系.md"]
---
# 模糊关系矩阵的 sup-min 复合计算流程

依据 5.9.3.2.1（式 5.371–5.373），在有限全域上计算模糊关系的复合 $T=R\circ S$。

## 步骤

1. **设定全域与关系**：$X=\{x_1,\dots,x_n\}$，$Y=\{y_1,\dots,y_m\}$，$Z=\{z_1,\dots,z_l\}$；$R\in F(X\times Y)$（从 $X$ 到 $Y$ 的关系），$S\in F(Y\times Z)$（从 $Y$ 到 $Z$ 的关系）。
2. **写出矩阵表示**：$R=(r_{ij})$，$S=(s_{jk})$，其中 $r_{ij}=\mu_R(x_i,y_j)$，$s_{jk}=\mu_S(y_j,z_k)$（式 5.372）。
3. **逐元素计算**：对每对 $(i,k)$（$i=1,\dots,n$；$k=1,\dots,l$），

   $$t_{ik}=\sup_j\min\{r_{ij},s_{jk}\}\tag{5.373}$$

   其中 $j$ 取遍 $1,\dots,m$；有限情形 sup 即最大值 max。
4. **组装结果**：$T=R\circ S=(t_{ik})$，是 $X\times Z$ 上的模糊关系矩阵。逆关系可顺便读出：$R^{-1}=(r_{ij})^{\mathrm T}$（转置）。

## 为什么这样算（原理）

复合沿共享的中间全域 $Y$ 进行（式 5.371）：

$$\mu_{R\circ S}(x,z)=\sup_{y\in Y}\{\min\{\mu_R(x,y),\mu_S(y,z)\}\}$$

- min 对应「经由同一中间元素 $y$ 时两个关系同时成立」的逻辑与；
- sup 对应「存在这样的 $y$」的存在量化（逻辑或），无限全域下最大值可能不存在而上确界仍存在。

因此矩阵运算中**用上确界代替求和、用极小值代替乘法**，结果不是通常的矩阵乘积——这是与 [[concepts/邻接矩阵]] 幂运算（通常算术）的本质区别。

## 变体

将第 3 步的 min 换为通常乘积得 max-乘积复合；换为平均得 max-平均复合（见 [[comparisons/三种复合方式比较]]）。注记 A：一般地任何 t-范数可代替 min（见 [[concepts/t-范数]]）。

## 注意事项

- 原文 5.9.3.2.1 开头「还设 $R,S\in F(G)$，其中 $G\subseteq X\times Z$」疑为「$R\circ S\in F(X\times Z)$」之讹，见 [[queries/5-9-3全节系统性转写讹误清单]]。
- 六条运算法则（式 5.374–5.379）仅对本流程的 sup-min 复合陈述，见 [[findings/模糊关系复合六法则]]。