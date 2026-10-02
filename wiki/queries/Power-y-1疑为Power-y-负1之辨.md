---
type: query
title: "Power[y, 1] 疑为 Power[y, -1] 之辨"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, FullForm, 转写校勘, 模式匹配]
related: [模式（Mathematica）, FullForm（完整形式）, 式20-16至20-21模式定义与替换算例复算, 20-2-7全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/20.2.7 模式.md"]
---
# Power[y, 1] 疑为 Power[y, -1] 之辨

## 问题

20.2.7 节式 (20.20) 的评论称：`b/y` 的 FullForm 为 `Times[b, Power[y, 1]]`，“就结构比较而言 Times 的第二个自变量等同于该模式的结构”，故 `b/y /. y^_ -> yes` 得 `b yes`。然而 `Power[y, 1]` 与数学事实矛盾——`b/y` 的完全形式究应为 `Times[b, Power[y, -1]]`，还是纸本原即如此？

## 证据

- **数学事实**：`b/y = b·y^(−1)`，其 FullForm 只能是 `Times[b, Power[y, -1]]`；`Power[y, -1]` 与模式 `y^_`（`Power[y, _]`）结构等同，被替换为 yes，得 `Times[b, yes]` 即 `b yes`——这恰是 Out[4] 的成因。
- **反证**：若 FullForm 真为 `Times[b, Power[y, 1]]`，则 `Power[y, 1]` 会自动化简为 `y`，该表达式即 `b y`，根本无从作为 `b/y` 的内部形式存在，被检验对象自身即不成立。
- **旁证**：原文同句伴有全半角括号混杂（「Power[y, 1] ］」），提示该段转写质量不佳，脱负号可能性大。

## 倾向与待办

倾向判为脱负号之讹（或原书排印脱漏），应为 `Times[b, Power[y, -1]]`。待核对纸本以区分「转写讹误」与「排印错误」。复算记录见 [[findings/式20-16至20-21模式定义与替换算例复算]]；此点亦扩展 [[concepts/FullForm（完整形式）]] 的实例库。
