---
type: query
title: Axex 疑为 Axes 之辨
tags: [校勘, 转写讹误, mathematica, inputform]
related: [20-4全节系统性转写讹误清单, InputForm图形对象内部结构转录校勘, 10-数学手册原书第10版--18-204-用mathematica绘图--f10hmv]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# Axex 疑为 Axes 之辨

## 现象

20.4.4.2 的 InputForm[%] 输出块中，选项写作 `Axex->{True, True}`。

## 疑点

Mathematica 无 `Axex` 符号；该选项应为 `Axes->{True, True}`（x 误作 x 位的 e，典型的字符转写讹误）。同一输出块中 `AxesLabel`、`AxesOrigin` 拼写正常，可见是单点讹误而非系统性。

## 判定倾向

几乎可定谳为 `Axes`：图形对象默认选项列表中 x、y 两轴均画出，与 `Axes->{True, True}` 语义吻合，且 Plot 默认即画两轴（图 20.3 可观察）。

## 状态

待核对原书 PDF 定谳。上下文校勘见 [[InputForm图形对象内部结构转录校勘]]；总目：[[20-4全节系统性转写讹误清单]]。