---
type: concept
title: "Table、Range 与 Array 列表生成命令"
created: 2026-10-02
updated: 2026-10-02
tags: [Mathematica, 列表生成, Table, Range, Array]
related: [列表（Mathematica）, 嵌套列表, Table与Array与Range比较, mathematica]
sources: ["数学手册(原书第10版)/20.2.4 列表.md"]
---

# Table、Range 与 Array 列表生成命令

Table、Range 与 Array 是 Mathematica 中按规则创建 [[列表（Mathematica）]] 的三个内建命令。《数学手册(原书第10版)》20.2.4.4 指出：Mathematica 中有好几种运算用于创建列表，其中之一是表 20.5 显示的命令 Table，它常出现在涉及数学函数的时候；运算 Range 产生连续数或等间距数（算术序列）的一个列表；命令 Array 使用函数（相对于 Table 使用的函数值）创建列表。三者的语义分工比较见 [[Table与Array与Range比较]]。

## 表 20.5 Table 运算（逐字转录）

| 命令 | 说明 |
|---|---|
| Table[f, {imax}] | 创建 f 具有 imax 值: f(1), f(2),···, f(imax) 的一个列表 |
| Table[f, {i, imin, imax}] | 创建 f 具有从 imin 到 imax 的值的一个列表 |
| Table[f, {i, imin, imax, di}] | 和上面一个相同, 但增量为 di |

首行释义与 Mathematica 实际语义疑似冲突：`Table[f, {imax}]` 不含迭代变量，实际产生 imax 个 f 的拷贝；欲得函数值序列须 `Table[f[i], {i, imax}]` 或 `Array[f, imax]`。见 [[Table首行imax释义与Mathematica语义之辨]]。

## 高维嵌套形式

表达式 `Table[f, {i, i1, i2}, {j, j1, j2}, ...]` 产生一个高维、多重嵌套表（见 [[嵌套列表]]）。二项式系数算例：

```text
In[1] := Table[Binomial[7, i], {i, 0, 7}]]    ← 转录衍一右括号
         → Out[1] = {1, 7, 21, 35, 35, 21, 7, 1}

In[2] := Table[Binomial[i, j], {i, 1, 7}, {j, 0, i}]
         → Out[2] = {{1,1},{1,2,1},{1,3,3,1},{1,4,6,4,1},{1,5,10,10,5,1},
                     {1,6,15,20,15,6,1},{1,7,21,35,35,21,7,1}}
```

In[2] 得到直至 7 次的二项式系数（帕斯卡三角第 1–7 行，内层迭代上界依赖外层变量 i）。复算见 [[Table-Range-Array二项式系数算例复算]]。

## Range 与 Array

```text
Range[n]            产生列表 {1, 2, ..., n}
Range[n1, n2]       产生从 n1 到 n2、步长为 1 的数（算术序列）的列表
Range[n1, n2, dn]   步长为 dn
Array[Exp, 5]       产生 {e, e², e³, e⁴, e⁵}
```

（源文此处转写有「Range[nl, n2] Range[n1, n2, dn]」脱连词「和」与「到」、「nl」为「n1」之讹，见 [[20-2-4全节系统性转写讹误清单]]。）