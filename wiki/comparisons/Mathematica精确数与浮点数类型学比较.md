---
type: comparison
title: "Mathematica 中精确数与浮点数的类型学比较"
tags: [Mathematica, 类型系统, 精确算术, 浮点数, 比较分析]
related: [Mathematica数的四种基本类型, Mathematica谓词检验算子, Mathematica特殊常数, Mathematica中数的表示与转换, 公式操作, 数值计算（计算机代数应用领域）]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# Mathematica 中精确数与浮点数的类型学比较

依据《数学手册（原书第10版）》20.2.2.1–20.2.2.2（[[sources/10-数学手册原书第10版--21-2022-mathematica中数的类型--gq11qw]]），Mathematica 的四种数的类型沿「精确—近似」轴分层。本页并置两侧特征与判定规则。

## 比较表

| 维度 | 精确一侧：Integer、Rational | 近似一侧：Real |
|---|---|---|
| 表示 | 任意长精确整数；互素分数 Integer/Integer | 浮点数，任意给定精度，输入形如 nnnn.mmmm |
| 运算含义 | 精确算术，无舍入误差 | 带精度的浮点算术 |
| 尾部小数点 | nnn 为 Integer | nnn. 即被判为 Real（Head[51.] = Real，IntegerQ[2.] = False） |
| 向另一侧的转换 | Rationalize[x, dx]：由浮点求给定精度下的最佳有理逼近 | N[x, n]：由精确数（含符号常数）求 n 位浮点 |
| 谓词 | IntegerQ 等类型检验 | NumberQ 覆盖四类字面量 |

（转换命令详见 [[concepts/Mathematica中数的表示与转换]]。）

## Complex 的跨层地位

Complex（number + number*I）的实部和虚部可属任何数的类型，整个数的类型由「最宽」分量决定：`5.731 + 0 I` → Real（`0 I` 化简为精确 0），`5.731 + 0. I` → Complex（`0.` 为近似零）。复数不构成第三个精度层，而是两层的组合闭包。

## 符号常数的定位

Pi、E、Degree、Infinity、I（[[concepts/Mathematica特殊常数]]）不是数的类型的字面量（NumberQ[π] = False），但具数值性（NumericQ[π] = True）且可任意精度求值（N[E, 20]）。它们与 Integer/Rational 同处精确一侧，经 N 进入近似一侧——谓词分工见 [[concepts/Mathematica谓词检验算子]]。

## 与「公式操作 vs 数值计算」的对应

这一分层是 [[concepts/公式操作]]（符号、精确）与 [[concepts/数值计算（计算机代数应用领域）]]（数值、近似）二分在数据类型层面的具体化。精确解的浮点代入风险另见 [[queries/符号解浮点代入的相消风险]]。

## 边界

本页结论仅由 20.2.2 节支持、仅对 Mathematica 成立；跨系统（Matlab/Maple）同题数值比较见 [[comparisons/Matlab-Mathematica-Maple同题数值比较]]。