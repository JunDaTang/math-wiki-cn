---
type: concept
title: 函数迭代命令 Nest、NestList、FoldList 与 FixedPoint
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 函数迭代, Nest, NestList, FoldList, FixedPoint, FixedPointList]
related: [Mathematica函数运算与纯函数, 列表运算命令, Table-Range-Array列表生成命令]
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# 函数迭代命令 Nest、NestList、FoldList 与 FixedPoint

这是 Mathematica 中「把同一函数反复施于初值」的命令族，属 20.2.8 定义的函数运算：函数名既是表达式，便可以被嵌套进自身。各命令的分工在于——是否显示中间值、是否自动终止、变元是否累进。

## Nest：嵌套 n 次，只给终值

`Nest[f, x, n]`：函数 f 作用于 x 后被嵌套进自身 n 次，结果为

```
f[f[···f[x]···]]   （共 n 层 f）
```

## NestList：嵌套 n 次，列出全程

`NestList[f, x, n]`：显示列表

```
{x, f[x], f[f[x]], ...}
```

即从初值到第 n 次嵌套的全部中间值（含初值共 n+1 项——20.2.8 (6) 的算例 `NestList[g, 4.6, 4]` 输出 5 项，与此一致）。

## FoldList：双变元函数的迭代

`FoldList[f, x, list]`：对两个变元的函数做迭代（源文仅此一句定义，未给算例）。

## FixedPoint / FixedPointList：迭代至不动点

- `FixedPoint[f, x]`：重复应用该函数直到结果不再改变，返回终值；
- `FixedPointList[f, x]`：显示应用 f 后结果的连续列表，直到这个值不再改变（源文未给算例）。

## 应用：牛顿法求根

20.2.8 (6) 以 NestList 与 FixedPoint 实现牛顿法，在 3π/2 邻域求 x cos x = sin x 的根：

```
In[1] := f[x_] := x - Tan[x]
In[2] := f′[x]  →  Out[2] = 1 - Sec[x]^2
In[3] := g[x_] := x - f[x]/f′[x]
In[4] := NestList[g, 4.6, 4] → Out[4] = {4.6, 4.54573, 4.50615, 4.49417, 4.49341}
In[5] := FixedPoint[g, 4.6]  → Out[5] = 4.49341
```

数值经独立复算逐位吻合，根 4.49341 精确至 6 位有效数字（[[findings/牛顿法NestList-FixedPoint求根算例复算]]）；作为可复现流程的整理见 [[methodology/NestList实现牛顿迭代流程]]。

## 覆盖不对称与未验证之说

- FoldList、FixedPointList 仅提名或一句定义，无算例——语义细节待 Mathematica 官方文档或原书补证；
- 源文称 FixedPoint「直到结果不再改变」，未说明终止判定（SameTest）与精度控制；随后的「该结果还可以达到更高的精度」无演示，属未验证陈述。

## 转写警示与同域命令

源文 (3)「函数 作用千 后被嵌套进自身 次」脱 f、x、n 三符号，(4) 标题「N estList」衍空格、「最终的 被嵌套 次」脱符号、列表尾部衍「}」，(5)(6)「对千」「应用 后」等讹——引用须依 [[queries/20-2-8全节系统性转写讹误清单]] 校勘。NestList 产出列表，与 [[concepts/列表运算命令]]、[[concepts/Table-Range-Array列表生成命令]] 的列表构造/运算命令同域，但语义核心是函数迭代而非列表操作。