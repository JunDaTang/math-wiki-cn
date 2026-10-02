---
type: query
title: 情形I-II条件b之y疑为v之辨
created: 2026-10-01
updated: 2026-10-01
tags: [转写勘误, 二次优化, 库恩—塔克条件, 18-2-2]
related: [库恩—塔克条件, 二次优化, 18-2-2全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/18.2.2 特殊非线性优化问题.md"]
---
# 情形 I/II 条件 b) 之「y」疑为「v」之辨

## 疑点

手册 18.2.2.2 库恩—塔克条件表中，情形 I 与情形 II 的条件 b) 均转写为

$$2\boldsymbol{C}\boldsymbol{x}-\boldsymbol{y}+\boldsymbol{A}^{\mathrm{T}}\boldsymbol{u}=-\boldsymbol{p}$$

其中出现的是 $\boldsymbol{y}$（$A\boldsymbol{x}\leqslant\boldsymbol{b}$ 的松弛量），而记号 (18.50) 已另行定义 $\boldsymbol{v}=\partial L/\partial\boldsymbol{x}=\boldsymbol{p}+2\boldsymbol{C}\boldsymbol{x}+\boldsymbol{A}^{\mathrm{T}}\boldsymbol{u}$。

## 判断依据

1. **记号互证**：c) 中 $\boldsymbol{x},\boldsymbol{v},\boldsymbol{y},\boldsymbol{u}\geqslant\boldsymbol{0}$ 四变量并列，d) 中 $\boldsymbol{x}^{\mathrm{T}}\boldsymbol{v}+\boldsymbol{y}^{\mathrm{T}}\boldsymbol{u}=0$——$\boldsymbol{v}$ 与 $\boldsymbol{y}$ 分立出现，但 b) 中却只有 $\boldsymbol{y}$，$\boldsymbol{v}$ 无来源。
2. **独立推导**：$\boldsymbol{x}\geqslant\boldsymbol{0}$ 约束的对偶乘子 $\boldsymbol{v}$ 满足 $\boldsymbol{v}=\boldsymbol{p}+2\boldsymbol{C}\boldsymbol{x}+\boldsymbol{A}^{\mathrm{T}}\boldsymbol{u}\geqslant\boldsymbol{0}$，移项即 $2\boldsymbol{C}\boldsymbol{x}-\boldsymbol{v}+\boldsymbol{A}^{\mathrm{T}}\boldsymbol{u}=-\boldsymbol{p}$；若用 $\boldsymbol{y}$ 则该条件无法由一阶原理导出。
3. 情形 III（$\boldsymbol{x}$ 自由、无 $\boldsymbol{v}$）的 b) 为 $2\boldsymbol{C}\boldsymbol{x}+\boldsymbol{A}^{\mathrm{T}}\boldsymbol{u}=-\boldsymbol{p}$，恰是令 $\boldsymbol{v}=\boldsymbol{0}$ 的退化——与 $\boldsymbol{v}$ 的解释吻合。

## 判断

b) 中的「y」应为「v」（置信度很高）。复算详情见 [[findings/式18-47至18-51三情形库恩—塔克条件复算]]；全节讹误清单见 [[queries/18-2-2全节系统性转写讹误清单]]。