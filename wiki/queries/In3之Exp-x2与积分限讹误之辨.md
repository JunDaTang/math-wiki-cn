---
type: query
title: In[3] 之 Exp[-x^2] 与积分限讹误之辨
created: 2026-10-02
updated: 2026-10-02
tags: [转写讹误, Mathematica, NIntegrate]
related: [10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm, mathematica, NIntegrate峰值丢失与递归选项复算, 19-8-4全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/19.8.4 交互程序系统和计算机代数系统的应用.md"]
---
# In[3] 之 Exp[-x^2] 与积分限讹误之辨

## 疑点

源文（19.8.4.2 数值积分）：「五 [3] :=Nintegrate[Exp[ x/\2],{x, 1000,1000}]」——行首标签、被积函数与积分限三处均乱码。

## 依上下文复原

据前后文（默认选项下「因为积分区域太大，Mathematica 找不到 x=0 的峰值」、Out[3]=1.34946·10⁻²⁶、In[4] 的对照命令），应为：

```txt
In[3] := NIntegrate[Exp[-x^2], {x, -1000, 1000}]
```

即：五[3]→In[3]、Nintegrate→NIntegrate、Exp[x/\2]→Exp[−x^2]（负号丢失、「^」讹为「/\」）、{x, 1000,1000}→{x, −1000, 1000}（负号与千位分隔丢失）。

## 状态

复原与上下文完全相容，且 In[4]（加 MinRecursion→3、MaxRecursion→10 后得 1.77245=√π）证实为同一积分（[[findings/NIntegrate峰值丢失与递归选项复算]]）；待原书逐字确认。