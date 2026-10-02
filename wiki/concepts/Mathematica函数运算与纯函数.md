---
type: concept
title: Mathematica 函数运算与纯函数
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 函数运算, 纯函数, 一等表达式]
related: [表达式（Mathematica）, Derivative微分算子, 函数迭代命令Nest-NestList-FoldList-FixedPoint, Apply与Map, 反函数与级数反演]
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# Mathematica 函数运算与纯函数

**函数运算**是 Mathematica 中以函数本身（而非函数值）为运算对象的一类操作。其成立的机制根据是：在 Mathematica 中函数的名称作为**表达式**处理（见 [[concepts/表达式（Mathematica）]]），因此凡可施于表达式的运算亦可施于函数——微分、反演、迭代、头替换、逐元映射皆然。此概念是《数学手册(原书第10版)》20.2.8 节的总纲，该节据此列出八类运算（反函数/级数反演、微分、Nest、NestList、FixedPoint、FixedPointList、Apply、Map）。

## 函数作为可运算的对象

源文（校读后）：「函数对于数和表达式做运算。Mathematica 也可以对函数进行运算，因为函数的名称是作为表达式来处理的，所以它们也可以当作表达式来处理。」

由此派生四族具体运算，各设专页：

- [[concepts/Derivative微分算子]]——`Derivative[1][f]` / `f′`，把微分实现为函数空间上的映射；
- [[concepts/反函数与级数反演]]——InverseFunction、InverseSeries（本源仅列名）；
- [[concepts/函数迭代命令Nest-NestList-FoldList-FixedPoint]]——Nest 族把函数嵌套进自身；
- [[concepts/Apply与Map]]——Apply 换头、Map 保头逐元施函。

## 纯函数（`#1` 与 `&` 记法）

对已定义的函数求导，Mathematica 返回的不是普通表达式而是一个**纯函数**（pure function）：

```
In[1] := f[x_] := Sin[x] Cos[x]
In[2] := f′      →  Out[2] = Cos[#1]^2 - Sin[#1]^2 &
In[3] := %[x]    →  Out[3] = Cos[x]^2 - Sin[x]^2
```

- `#1` 是第一个变元的槽位（slot），`&` 标记其左侧整体为一个无名函数；
- 纯函数可像具名函数一样被调用：`%[x]` 把 Out[2] 的纯函数施于 x，得到通常的表达式。

复算：d/dx(Sin x·Cos x) = Cos²x − Sin²x，与 Out[2]/Out[3] 吻合（[[findings/In1至In3导数纯函数算例复算]]）。

**证据性质说明**：20.2.8 正文并未系统讲解纯函数记法，仅说「f′ 被表示成一个纯函数，于是 %[x] …」；「#1 为槽位、& 为纯函数终结符」的语义解释是从算例提取、并可依 Mathematica 公开语义独立验证的背景知识，非源文原文。

## 转写警示

本节「千/于」系统性互讹、多处脱符号（如 (3) 条「函数 作用千 后被嵌套进自身 次」脱 f、x、n），引用原文须先经 [[queries/20-2-8全节系统性转写讹误清单]] 校勘。