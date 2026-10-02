---
type: concept
title: "纯函数（Mathematica）"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 纯函数, function, slot, 匿名函数]
related: [entities/mathematica, concepts/Mathematica完全形式与中置算子, concepts/Head函数与类型查询, concepts/延迟赋值（SetDelayed与RuleDelayed）, comparisons/纯函数完整形式与简写形式比较, comparisons/纯函数与命名函数定义比较, findings/式20-13至20-15纯函数算例转录复算, queries/纯函数投影记号疑脱1之辨, sources/10-数学手册原书第10版--7-2026-函数--v9sqy0]
sources: ["数学手册(原书第10版)/20.2.6 函数.md"]
---
# 纯函数（Mathematica）

纯函数（pure function）是 Mathematica 中的一类无名函数——手册 20.2.6.3 称之为「一个无名函数，一个没有赋予名称的运算」，可在不先行命名的情况下直接定义并即时调用。纯函数有两种记法：完整形式 `Function[x, body]` 与简写形式 `body&`。

## 完整形式：Function[x, body]

`Function[x, body]` 的第一个自变量指定形式参数，第二个自变量是函数主体（body），即主体是变元的函数的一个表达式。`Function` 即此表达式的头（参见 [[concepts/Head函数与类型查询]]）。调用时把实参直接接在函数表达式之后：

```text
In[1] := Function[x, x^3 + x^2]           Out[1] = Function[x, x^3 + x^2]   (20.13)
In[2] := Function[x, x^3 + x^2][c]  给出  Out[2] = c^2 + c^3                (20.14)
```

## 简写形式：body& 与 # 占位符

简写形式记作 `body&`，其中变元表示为 `#`：

```text
In[3] := (#^3 + #^2)&[c]                  Out[3] = c^2 + c^3                (20.15)
```

要点：

- `#` 是变元占位符；多变元纯函数的完整形式为 `Function[{x1, x2, ...}, body]`，简写形式主体中的变元用 `#1`, `#2`, … 表示。
- `&` 是终止记号：「用于结束表达式的符号 & 非常重要，因为从这个符号可以看出前面的表达式应该被认作一个纯函数」。它是手册表 20.2 算子家族之外的后缀算子，为 [[concepts/Mathematica完全形式与中置算子]] 的延伸证据。
- 两种记法语义等价：式 20.14 与 20.15 对同一主体给出相同输出（见 [[comparisons/纯函数完整形式与简写形式比较]]、[[findings/式20-13至20-15纯函数算例转录复算]]）。

## 特例：恒等函数与坐标投影

- `#&` 即恒等函数：对于任何自变量 x 它指派 x（原文「它指派 X」之 X 疑为小写 x 误植，见 [[queries/20-2-6全节系统性转写讹误清单]]）。
- 「类似地＃ ＆相应于在第一个坐标轴上的投影」：原文「＃ ＆」疑脱「1」，即 `#1 &`。因 `#` ≡ `#1`（同为第一变元占位符），两种读法在数学上均为真；记号考据见 [[queries/纯函数投影记号疑脱1之辨]]。

## 与命名函数定义的对照

纯函数无名、即用即弃，与经 Set/SetDelayed 赋名的函数定义（[[concepts/Set指派与清除]]、[[concepts/延迟赋值（SetDelayed与RuleDelayed）]]）构成天然对照，详见 [[comparisons/纯函数与命名函数定义比较]]。