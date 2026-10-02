---
type: entity
title: Mₙ（n 阶方阵环）
created: 2026-09-30
updated: 2026-09-30
tags: [环论, 矩阵环, 非交换环, 零因子, 线性代数, 数学手册, 5-3-7]
related: [concepts/环, concepts/零因子, concepts/整区, entities/典型矩阵群gln-sln-on-son-un-sun, findings/环与域标准例子组, comparisons/整区除环与域比较]
sources: ["数学手册(原书第10版)/5.3.7 环和域.md"]
---
# Mₙ（n 阶方阵环）

Mₙ 是全体 n 阶实（或复）元素方阵组成的集合，在矩阵加法与乘法下构成的一个环；它是本节例 B 给出的「非交换、含单位元、含零因子」的环的标准例子，与只含可逆元的 [[entities/典型矩阵群gln-sln-on-son-un-sun]] 形成对照（后者属群论对象，前者是环论对象）。

## 环结构

- 对矩阵加法与乘法构成**非交换环**；
- 有单位元，即恒等矩阵；
- 含零因子，故不是 [[concepts/整区]]。

## 零因子算例（n = 2，已复算）

$$
\begin{pmatrix} 1 & 0 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 0 & 0 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}
$$

两个因子均非零矩阵而乘积为零矩阵，故均为 Mₙ 的零因子（见 [[concepts/零因子]]）。源文以 $\binom{0}{0}$ 等错排表示 2×2 矩阵，此处已按矩阵乘法逐项复核 ✓。

## 在类型层级中的位置

Mₙ 展示了「有单位元素环」不必然无零因子、也不必然交换，是 [[comparisons/整区除环与域比较]] 中最常用的反例来源之一。