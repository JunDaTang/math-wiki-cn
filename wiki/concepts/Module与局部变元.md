---
type: concept
title: Module 与局部变元（Mathematica）
tags: [mathematica, module, 局部变元, 作用域, 程序设计]
related: [concepts/Do与While循环, concepts/列表（Mathematica）, concepts/Set指派与清除, concepts/延迟赋值（SetDelayed与RuleDelayed）, entities/mathematica, findings/式20-24与20-26循环与模块语法转录复算, findings/式20-27-sumq过程式算例复算, comparisons/过程式与函数式sumq实现比较]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
---
# Module 与局部变元（Mathematica）

`Module` 是 Mathematica 中用于定义和使用局部变元的程序设计构造：包含在其变元列表中的变元或常数仅在该模块内部局部可用，而在模块内指派给它们的值在模块之外即告无效。《数学手册（原书第10版）》20.2.9 将其定位为 Mathematica 在循环结构之外提供的另一项程序设计能力（式 20.26）。

## 语法

```
Module[{t1, t2, ...}, procedure]    (20.26)
```

## 例 A：局部累加变元

```
In[1] := sumq[n_] :=
         Module[{sum = 1.},
           Do[sum = sum + N[Sqrt[i]], {i, 2, n}];
           sum];
```

此定义中 `sum` 为模块局部变元并以 `1.`（恰为 √1 项）为初值，故随后的 `Do` 循环（见 [[concepts/Do与While循环]]）自 i = 2 起累加；调用 `sumq[30]` 得 112.083（复算见 [[findings/式20-27-sumq过程式算例复算]]）。模块内的 `sum = 1.`、`sum = sum + ...` 属 [[concepts/Set指派与清除]] 所述 Set 指派在局部作用域中的运用，而函数定义本身 `sumq[n_] := ...` 则为 [[concepts/延迟赋值（SetDelayed与RuleDelayed）]] 之 SetDelayed。

## 与相邻概念的关系

- `Module` 的变元列表 `{sum = 1.}` 本身是 [[concepts/列表（Mathematica）]] 意义上的列表；
- 与函数式实现的对照（例 B 不须变元 sum 及其初始值）见 [[comparisons/过程式与函数式sumq实现比较]]；
- 本来源仅介绍 `Module` 一种局部化构造，未涉及 Mathematica 其余作用域机制，相关内容不据本页推断。