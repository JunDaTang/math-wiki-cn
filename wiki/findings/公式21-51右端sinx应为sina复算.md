---
type: finding
title: "公式 21.51 右端 sin x 应为 sin a 复算"
created: 2026-10-02
updated: 2026-10-02
tags: [勘误, 复算, 定积分, 校勘]
related: [条目51右端sinx疑为sina之辨, 21-8全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
source: "[[10-数学手册原书第10版--7-218-定积分--1rtpy2p]]"
confidence: high
replicated: true
---
# 公式 21.51 右端 sin x 应为 sin a 复算

手册 21.51 按原文转写为

$$\int_0^\infty\frac{dx}{1+2x\cos a+x^2}=\frac{a}{\sin x}\qquad\left(0<a<\frac{\pi}{2}\right),$$

右端分母的 x 是左端积分哑变量，不应出现——右端应为参数 a 的函数。

## 复算证据（直接）

1. **部分分式**：$1+2x\cos a+x^2=(x+e^{ia})(x+e^{-ia})$，展开复算得 $\int_0^\infty\frac{dx}{1+2x\cos a+x^2}=\frac{a}{\sin a}$。
2. **特值双吻合**：a→0 时右端 →1，恰为 $\int_0^\infty\frac{dx}{(1+x)^2}=1$；a=π/2 时右端 =π/2，恰为 $\int_0^\infty\frac{dx}{1+x^2}=\frac{\pi}{2}$。

与同被积函数在 [0,1] 上的 21.50（值 a/(2 sin a)）共用 a/sin a 骨架，进一步支持勘正为 a/sin a。刊本确认待 [[条目51右端sinx疑为sina之辨]]。