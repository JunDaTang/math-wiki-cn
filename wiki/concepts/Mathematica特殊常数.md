---
type: concept
title: "Mathematica 特殊常数"
tags: [Mathematica, 常数, Pi, E, Degree, Infinity, I]
related: [mathematica, Mathematica数的四种基本类型, Mathematica谓词检验算子, Mathematica中数的表示与转换]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# Mathematica 特殊常数

Mathematica 特殊常数是系统中预定义、能以任意精度调入（求值）的符号常数。《数学手册（原书第10版）》20.2.2.2（[[sources/10-数学手册原书第10版--21-2022-mathematica中数的类型--gq11qw]]）列举五种：

| 符号 | 所表示的数 | 转写备注 |
|---|---|---|
| Pi | π | |
| E | e（自然常数） | 源稿「以符号 表示的 e」处符号 E 脱失 |
| Degree | 从角度到弧度的变换因子 π/180° | 源稿印作 π/180°；「°」是否原书所有待核（见 [[queries/20-2-2全节系统性转写讹误清单]]） |
| Infinity | ∞ | 源稿「表示符号 ∞ Infinity」文句粘连，疑为「以符号 Infinity 表示的 ∞」 |
| I | 虚单位 | |

## 要点

- 「能以任意精度被调入」指这些常数可作任意精度求值，例如 `N[E, 20] = 2.7182818284590452354`（式 20.6a，见 [[concepts/Mathematica中数的表示与转换]]）。
- 它们是符号而非四种数的类型的字面量：`NumberQ[π]` 为 False 而 `NumericQ[π]` 为 True（[[concepts/Mathematica谓词检验算子]]）。符号常数与 Integer/Rational 同处精确一侧，经 N 进入浮点一侧，类型学定位见 [[comparisons/Mathematica精确数与浮点数类型学比较]]。
- 本节未涉及这些常数的符号运算性质（如 Pi 的恒等式），那属于符号计算的一般内容（参见 [[concepts/公式操作]]）。

## 边界

本页仅关于 Mathematica 的常数命名与语义；Maple、Matlab 的常数记法各不相同（参见 [[sources/10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm]]），不应外推。