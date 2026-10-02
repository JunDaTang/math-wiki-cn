---
type: concept
title: Apply 与 Map（头替换与逐元映射）
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, Apply, Map, 头替换, 逐元映射]
related: [Mathematica函数运算与纯函数, Part（部件提取与头）, FullForm（完整形式）, 列表运算命令]
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# Apply 与 Map（头替换与逐元映射）

Apply 与 Map 是 Mathematica 中把一个函数施加于表达式结构的两种基本方式，均属 20.2.8 的函数运算。《数学手册(原书第10版)》以两条定义式给出其语义：

```
Apply[f, {a, b, c, ...}]  →  f[a, b, c, ...]          (20.22)
Map[f,   {a, b, c, ...}]  →  {f[a], f[b], f[c], ...}  (20.23)
```

## Apply：替换表达式的头

Apply 用 f 替换目标表达式的**头**（头与部件的概念见 [[concepts/Part（部件提取与头）]]）：

```
In[1] := Apply[Plus, {u, v, w}]                → Out[1] = u + v + w
In[2] := Apply[List, a + b + c]                → Out[2] = {a, b, c}
In[3] := FullForm[Apply[List, Plus[a, b, c]]]  → Out[3] = List[a, b, c]
```

源文结论（校读后）：「函数运算 Apply 以所求的 List 来代替所考虑的表达式 Plus 的头」。In[3] 借 [[concepts/FullForm（完整形式）]] 揭示机制：`a + b + c` 即 `Plus[a, b, c]`，头 Plus 换成 List 后得 `List[a, b, c]`。

## Map：保持头，逐元素施加函数

对一个有定义的函数 f，Map 生成一个列表，其元素是 f 施于原列表各元素时的值；且 Map 可以被应用于更一般的表达式：

```
In[1] := f[x_] := x^2
In[2] := Map[f, {u, v, w}]      → Out[2] = {u^2, v^2, w^2}
In[3] := Map[f, Plus[a, b, c]]  → Out[3] = a^2 + b^2 + c^2
```

In[3] 中 Plus 的头保持不动，只有各变元被 f 逐个替换。

## 表述张力

源文 (8) 先称「Map 生成一个列表」，随后演示的 In[3] 却输出非列表的 `a^2 + b^2 + c^2`；源文自己以「Map 可以被应用于更一般的表达式」一句调和。这是定义句表述偏窄造成的张力，非讹误。

## 复算与对照

五条算例经独立复算全部吻合（[[findings/式20-22至20-23与Apply-Map算例转录复算]]）；两者的系统对照见 [[comparisons/Apply与Map比较]]。另可参看 [[comparisons/依分量运算与矩阵运算比较]]：Map 正是「依分量运算」得以实现的机制（该比较页属 20.2.5 矩阵语境，此处仅作机制回指）。