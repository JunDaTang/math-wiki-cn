---
type: concept
title: "Head 函数与类型查询"
tags: [Mathematica, 类型系统, Head, 类型检查]
related: [mathematica, Mathematica数的四种基本类型, Mathematica谓词检验算子, Mathematica输入输出行记法]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# Head 函数与类型查询

Head[x] 是 Mathematica 的内建命令，返回表达式 x 的「头」（head），即其类型标识；对数而言，它返回 Integer、Rational、Real 或 Complex 四者之一，因而是查询数的类型归属的入口操作（四种类型见 [[concepts/Mathematica数的四种基本类型]]）。（背景知识，可独立验证：Mathematica 中一切表达式都具有 `head[参数]` 的统一结构，Head 即取其头部，故此命令的用途并不限于数的类型查询。）本页内容依据《数学手册（原书第10版）》20.2.2.1（[[sources/10-数学手册原书第10版--21-2022-mathematica中数的类型--gq11qw]]）。

## 源稿算例

```text
In[1] := Head[51]      Out[1] = Integer
In[2] := Head[51.]     Out[2] = Real
```

（In/Out 记法见 [[concepts/Mathematica输入输出行记法]]。）两个算例直接演示了「尾部小数点规则」：尾部小数点使 51. 被判为 Real 类型。

## 与谓词检验的关系

Head 返回类型名，而以 Q 结尾的谓词算子（[[concepts/Mathematica谓词检验算子]]）在逻辑检验意义上返回布尔常数 True/False；两者构成「取类型」与「验类型」的互补操作。

## 边界

本页仅关于 Mathematica；Head 的语法与语义不应外推至 Matlab 或 Maple。