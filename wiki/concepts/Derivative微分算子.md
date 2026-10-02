---
type: concept
title: Derivative 微分算子（f′）
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 微分, Derivative, 算子, 纯函数]
related: [Mathematica函数运算与纯函数, 表达式（Mathematica）, Set指派与清除]
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# Derivative 微分算子（f′）

Derivative 是 Mathematica 中把微分实现为**作用于函数的算子**的结构。据《数学手册(原书第10版)》20.2.8 (2)（校读后）：「函数的微分可以看成函数空间中的一个映射。Mathematica 中，微分算子是 `Derivative[1][f]`，或简记为 `f′`。如果定义了函数，则其导数可以由 f′ 得到。」这正是 [[concepts/Mathematica函数运算与纯函数]] 总纲的实例：微分施于函数本身，而非施于某个函数值。

## 算例一：f′ 不带变元，得到纯函数

```
In[1] := f[x_] := Sin[x] Cos[x]
In[2] := f′      →  Out[2] = Cos[#1]^2 - Sin[#1]^2 &
In[3] := %[x]    →  Out[3] = Cos[x]^2 - Sin[x]^2
```

复算：d/dx(Sin x·Cos x) = Cos²x − Sin²x（即 cos 2x），吻合。Out[2] 的 `#1`/`&` 即纯函数记法（见 [[concepts/Mathematica函数运算与纯函数]]）；`%[x]` 将其施于 x。源文 Out[3] 误作小写 `cos/sin`，系转写讹误（[[queries/20-2-8全节系统性转写讹误清单]]）。

## 算例二：f′[x] 带变元，得到关于 x 的表达式

```
In[1] := f[x_] := x - Tan[x]
In[2] := f′[x]  →  Out[2] = 1 - Sec[x]^2
```

复算：d/dx(x − tan x) = 1 − sec²x，吻合。此例出自 20.2.8 (6) 牛顿法算例（[[findings/牛顿法NestList-FixedPoint求根算例复算]]），与算例一形成对照：`f′` 返回纯函数，`f′[x]` 返回把该纯函数施于 x 的结果。

## 校勘注

源文 (2) 条「……函数空间中的一个映射Mathematica 中……」两句粘连，上引已按文义断开；其余大小写与空格讹误见 [[queries/20-2-8全节系统性转写讹误清单]]。