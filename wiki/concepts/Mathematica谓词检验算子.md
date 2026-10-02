---
type: concept
title: "Mathematica 谓词检验算子（Q 函数族）"
tags: [Mathematica, 谓词, 类型检查, NumberQ, NumericQ, PrimeQ]
related: [mathematica, Mathematica数的四种基本类型, Head函数与类型查询, Mathematica特殊常数]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# Mathematica 谓词检验算子（Q 函数族）

谓词（判据）是 Mathematica 中一组以 Q 结尾的检验算子，它们总是在逻辑检验（包括类型检查）的意义上回答布尔常数 True 或 False。《数学手册（原书第10版）》20.2.2.1（[[sources/10-数学手册原书第10版--21-2022-mathematica中数的类型--gq11qw]]）列举的数相关谓词为 NumberQ、IntegerQ、EvenQ、OddQ、PrimeQ，并以 NumericQ 与 NumberQ 对照，点出「表面上不是一个数」的对象仍可具有数值性。

## 源稿算例

```text
In[3] := NumberQ[51]           Out[3] = True      (20.5a)
        NumberQ[π]             Out[3] = False     （x = π 时）
        NumericQ[π]            True               （源稿讹作「Num.ericQ ［兀］」）
In[4] := IntegerQ[2.]          Out[4] = False
In[5] := PrimeQ[1075643]       Out[5] = True      (20.5b)
In[6] := PrimeQ[1075641]       Out[6] = False     (20.5c)
```

## NumberQ 与 NumericQ 之辨

NumberQ 检验对象是否「表面上是一个数」，即是否为四种数的类型的字面量（[[concepts/Mathematica数的四种基本类型]]），故 `NumberQ[π]` 为 False；NumericQ 检验对象是否具有数值含义，故 `NumericQ[π]` 为 True。符号常数 π（[[concepts/Mathematica特殊常数]]）不是数的类型的字面量，但可按任意精度求值——两个谓词的分工对应「类型成员资格」与「可数值求值性」两个不同层面。这是本节最具复用价值的教学点之一，其复算与讹误复原见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]] 与 [[queries/NumericQ断裂与兀为pi之讹]]。

## 复算状态

算例 (20.5a)–(20.5c) 及 NumberQ/NumericQ 对照全部复算一致；其中 1075641 = 3·7·17·23·131 已手工分解验证为复合数，PrimeQ[1075643] 的完整素性验证（试除至 √1075643 ≈ 1037）待机验。详见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]]。

## 边界

谓词的命名与语义仅对 Mathematica 成立；Matlab、Maple 有各自的检验机制，不应跨系统外推（跨系统同题算例见 [[comparisons/Matlab-Mathematica-Maple同题数值比较]]）。