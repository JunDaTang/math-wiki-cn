---
type: finding
title: NIntegrate 峰值丢失与递归选项复算
created: 2026-10-02
updated: 2026-10-02
tags: [复算, Mathematica, 数值积分, 递归选项]
related: [10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm, mathematica, 交互程序系统与计算机代数系统, In3之Exp-x2与积分限讹误之辨]
source: "10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/19.8.4 交互程序系统和计算机代数系统的应用.md"]
---
# NIntegrate 峰值丢失与递归选项复算

## 摘要

Mathematica 的 NIntegrate 在超大区间上以默认选项会丢失 x=0 处的峰值，返回错误值 1.34946·10⁻²⁶；增大 MinRecursion/MaxRecursion 后得到正确值 1.77245 = √π（复算证实）。此为「CAS 数值程序基于有限点数值表、答案可能仍然是错的」这一告诫（[[concepts/交互程序系统与计算机代数系统]]）的直接证据。

## 转录

```txt
A: In[1] := NIntegrate[Exp[-x^2], {x, -Infinity, Infinity}]      Out[1] = 1.77245.
B: In[2] := NIntegrate[1/x^2, {x, -1, 1}]
   Power::infy: Infinite expression 1/0 encountered.
   NIntegrate::inum: Integrand ComplexInfinity is not numerical at {x} = {0}.

In[3] := NIntegrate[Exp[-x^2], {x, -1000, 1000}]     （源文此行严重乱码，依上下文复原）
   NIntegrate::ploss: 数值积分因失去精度停止。无法达到要求的精度或准确度的目标；
   怀疑有如下情况：高振荡的被积函数或积分的真值为 0.
   Out[3] = 1.34946·10^-26
In[4] := NIntegrate[Exp[-x^2], {x, -1000, 1000}, MinRecursion -> 3, MaxRecursion -> 10]
   Out[4] = 1.77245
```

（In[3] 原文乱码之辨见 [[queries/In3之Exp-x2与积分限讹误之辨]]。）

## 复算

- √π = 1.772453850905516：例 A 的 1.77245 与 In[4] 的 1.77245 均为其截断，**证实**；
- In[3] 的 1.34946·10⁻²⁶ 与真值相差 26 个数量级，确为峰值丢失：积分区域太大，Mathematica（默认选项下）找不到 x=0 的峰值，**机制与数值均可复核**；
- 例 B：被积函数在 x=0 处不连续（奇点），系统认知并给出警告——但正文强调「然而，答案可能仍然是错的」。

## 机制（据本源）

- Mathematica 使用问题区域内大量点的数值表并认知极点，但使用某些预定的选项进行数值积分，在某些特殊情况下是不充分的；
- 参数 MinRecursion 与 MaxRecursion 确定 Mathematica 在问题区域工作的最小和最大递归步数，默认选项为 6；若此值增加，则即使运行变慢，但结果更好；
- 类似地可用式 (19.292) 在积分上下限间列出奇点 x_i：NIntegrate[fun, {x, xa, x₁, x₂, …, xe}]，使结果更准确。

## 置信

confidence: high；replicated: true（√π 为独立基准）。