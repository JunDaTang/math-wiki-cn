---
type: query
title: 情形III条件c之α疑为u之辨
created: 2026-10-01
updated: 2026-10-01
tags: [转写勘误, 二次优化, 库恩—塔克条件, 18-2-2]
related: [库恩—塔克条件, 二次优化, 18-2-2全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/18.2.2 特殊非线性优化问题.md"]
---
# 情形 III 条件 c) 之「α」疑为「u」之辨

## 疑点

手册 (18.51c) 转写为 $\boldsymbol{\alpha}\geqslant\boldsymbol{0},\ \boldsymbol{y}\geqslant\boldsymbol{0}$，其中「α」在本节未定义。

## 判断依据

1. 情形 III 中唯一的对偶变量是 $\boldsymbol{u}$（$A\boldsymbol{x}\leqslant\boldsymbol{b}$ 的乘子）：b) 中出现 $\boldsymbol{A}^{\mathrm{T}}\boldsymbol{u}$，d) 的互补条件是 $\boldsymbol{y}^{\mathrm{T}}\boldsymbol{u}=0$。
2. a) 定义的 $\boldsymbol{y}$ 是 $A\boldsymbol{x}\leqslant\boldsymbol{b}$ 的松弛量；不等式约束的乘子须非负，即 $\boldsymbol{u}\geqslant\boldsymbol{0}$——与情形 I 的 c)（$\boldsymbol{y},\boldsymbol{u}\geqslant\boldsymbol{0}$）结构一致。
3. 「α」与「u」在转写中字形易混。

## 判断

(18.51c) 应为 $\boldsymbol{u}\geqslant\boldsymbol{0},\ \boldsymbol{y}\geqslant\boldsymbol{0}$（置信度很高）。复算详情见 [[findings/式18-47至18-51三情形库恩—塔克条件复算]]；全节讹误清单见 [[queries/18-2-2全节系统性转写讹误清单]]。