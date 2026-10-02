---
type: query
title: "「Num.ericQ ［兀］」断裂为 NumericQ[π] 之辨"
tags: [勘误, Mathematica, NumericQ, NumberQ, OCR]
related: [20-2-2全节系统性转写讹误清单, Mathematica谓词检验算子]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# 「Num.ericQ ［兀］」断裂为 NumericQ[π] 之辨

问：20.2.2.1 节「然而Num.ericQ ［兀］得出 True」应如何复原？

## 拟复原

`NumericQ[π]`——函数名断裂为「Num.ericQ」，方括号讹作全角「［］」，希腊字母 π 讹作形近汉字「兀」。

## 证据

1. 上下文：「如果 x 表面上不是一个数，例如 x = π，则输出 False。然而 [此处] 得出 True」——恰构成 NumberQ 与 NumericQ 的对照论述；
2. Mathematica 语义：NumberQ[Pi] = False、NumericQ[Pi] = True，与复原后的叙述完全一致（复算见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]]）；
3. 「兀」与 π 形近，是 OCR 的典型近形混淆。

## 影响

此讹使本节关键教学点（NumberQ 与 NumericQ 之辨，见 [[concepts/Mathematica谓词检验算子]]）险些不可读；复原后文义无歧义，置信高，可直接采信。