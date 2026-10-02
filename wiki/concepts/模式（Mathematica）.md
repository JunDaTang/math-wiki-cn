---
type: concept
title: 模式（Mathematica）
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 模式匹配, 空白, 结构匹配, 编程机制]
related: [表达式（Mathematica）, FullForm（完整形式）, Rule变换规则与替换算子, 延迟赋值（SetDelayed与RuleDelayed）, 模式定义与字面定义比较, 列表（Mathematica）]
sources: ["数学手册(原书第10版)/20.2.7 模式.md"]
---
# 模式（Mathematica）

模式（Pattern）是 [[entities/mathematica]] 中代表“具有特定结构的整类表达式”的模板机制：它以空白符号 `_` 为基本元素，在被用于检查表达式时只比较结构一致性，而不检查数学相等性。模式是 Mathematica 自定义函数定义（`f[x_] := …`）与变换规则（左端为模式的 `… -> …`）的核心机制。

## 基本元素：空白与命名空白

- 空白 `_`（blank）是模式的基本元素。
- 命名空白 `x_`（读作“x 空白”）表示“具有名称 x 的某个东西”：它在匹配时约束被匹配对象，并可在定义右端以该名称引用。
- 典型用法即 20.2.7 节式 (20.16)：`f[x_] := Polynomial[x]`。用户由此定义了一个函数，其中 Polynomial[x] 是变元 x 的一个任意多项式；自此每当 `f[something]` 出现，Mathematica 就以其定义替换它。这种类型的定义称为一个模式。
- 注：`Polynomial` 并非 Mathematica 内置符号，书中此处系元记号用法；实际求值将得到字面的 `Polynomial[...]`。

## 匿名空白幂模式 y^_

`y^_` 在相应的定义中仅使用一个 `_`（不命名），即 `Power[y, _]`。它代表 y 的具有任何指数的任意次幂，因此代表具有相同结构的表达式的整个类：`y^a`、`y^Sqrt[x]`、`y^(r/q)`、`y^(-1)` 等皆与之结构一致。

## 结构匹配而非数学相等（核心辨析）

模式的本质在于它定义了一个结构。当 Mathematica 就某个模式检查一个表达式时，它是将该表达式元素的结构比作该模式的元素——**Mathematica 不检查数学相等性**。

算例（式 20.17–20.19）：

```mathematica
In[2] := l = {1, y, y^a, y^Sqrt[x], {f[y^(r/q)], 2^y}}
In[3] := l /. y^_ -> yes
Out[3] = {1, y, yes, yes, {f[yes], 2^y}}
```

- `1` 与 `y` 不被替换：尽管 y^0=1、y^1=y 在数学上成立，二者并不具有 `Power[y, 任意]` 的结构（不含 Power 头）。
- `y^a`、`y^Sqrt[x]` 被替换为 yes：结构一致。
- `f[y^(r/q)]` → `f[yes]`：替换深入嵌套表达式内部，即 `/.` 于所有层级替换所有出现——此为 [[queries/Replace疑为ReplaceAll之辨]] 的新佐证。
- `2^y` 不被替换：底数不是 y，结构不同。

## 模式比较总在 FullForm 中进行

原文评论：“模式比较总是出现在 FullForm 中。”算例（式 20.20）：

```mathematica
In[4] := b/y /. y^_ -> yes
Out[4] = b yes
```

成因：`b/y` 的 FullForm 为 `Times[b, Power[y, -1]]`，就结构比较而言，Times 的第二个自变量（`Power[y, -1]`）与模式 `y^_` 的结构等同，故被替换为 yes，得 `b yes`。（原文将 FullForm 讹作 `Times[b, Power[y, 1]]`，见 [[queries/Power-y-1疑为Power-y-负1之辨]]。）此点直接扩展 [[concepts/FullForm（完整形式）]] 与 [[concepts/Mathematica完全形式与中置算子]]：中置记法 `b/y` 的模式匹配须回到其完全形式来理解。

## 模式定义与字面定义

以模式为左端的定义（`f[x_] := x^3`）对任意实际变元生效；左端不含空白的字面定义（`f[x] := x^3`）仅当输入恰为符号 x 本身时才符合定义。两者对照详见 [[comparisons/模式定义与字面定义比较]]；其赋值机制均属 `:=`（SetDelayed），见 [[concepts/延迟赋值（SetDelayed与RuleDelayed）]]，并与 [[concepts/Set指派与清除]] 的指派语义相衔接。

## 与相关概念的关系

- [[concepts/表达式（Mathematica）]]：模式即“表达式结构类”的具体化，一切匹配皆依 [[concepts/FullForm（完整形式）]] 的结构进行。
- [[concepts/Rule变换规则与替换算子]]：模式常作变换规则左端，配合 `/.` 对整类表达式作批量替换。
- [[concepts/列表（Mathematica）]]、[[concepts/嵌套列表]]：替换可逐层穿透嵌套列表（式 20.17–20.19）。
