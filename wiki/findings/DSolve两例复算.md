---
type: finding
title: "DSolve 两例复算"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 复算, 微分方程, ProductLog]
related: [DSolve微分方程求解命令, 纯函数（Mathematica）]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
source: "[[10-数学手册原书第10版--20-203-mathematica的重要应用--tsdw5a]]"
confidence: high
replicated: true
---

# DSolve 两例复算

## 例 A：y′(x) − y(x)tanx = cos x（手册 9.1.1.2 之例）

书中通解（纯函数形式）：y = C[1]Sec[x] + Sec[x](x/2 + Sin[2x]/4)。

**复算成立**：记 F = C[1] + x/2 + Sin[2x]/4，则 y = F·sec x，y′ = F′sec x + F sec x tan x，其中 F′ = 1/2 + Cos[2x]/2 = (1+cos2x)/2 = cos²x。于是

y′ − y tanx = F′sec x = cos²x·sec x = cos x ✓。

`y[x] /. %1` 得解值、以及对 y′[x] 或 y[1] 做替换的说明，与纯函数语义一致（[[concepts/纯函数（Mathematica）]]）。

## 例 B：y′(x)·x·(x − y(x)) + y²(x) = 0（手册 9.1.1.2, 2. 之例）

书中隐式解：y[x] → −x·ProductLog[−E^(−C[1])/x]（转写「C[i]」为「C[1]」之讹）。

**复算成立（代换推导）**：令 v = y/x，则 y = vx、y′ = v + xv′，方程化为

(1−v)(v + xv′) + v² = 0 → v + xv′(1−v) = 0 → (1−v)/v dv = −dx/x。

积分得 ln v − v = −ln x + C，即 y·e^(−y/x) = e^C，亦即 (y/x)·e^(−y/x) = e^C/x。令 s = y/x，则 (−s)e^(−s) = −e^C/x；按 ProductLog 定义（z = w e^w 中 w 的主解）得 −s = ProductLog[−e^C/x]，故 y = −x·ProductLog[−e^C/x]。以 C = −C[1] 改写积分常数即得书中形式 ✓。

## 附带断言（书中原文主张）

- 如果 Mathematica 不能解一个微分方程，那么它将返回到输入而没有任何评论；
- 若符号解过于复杂，可求数值解（回指手册第 1321 页 19.8.4.2, 5.）；
- 甚至在复杂的多维区域 Mathematica 也能求某些偏微分方程的符号解和数值解。

## 证据性质

例 A 为回代直接验证；例 B 为代换法完整重推导，均属直接证据。命令语义见 [[concepts/DSolve微分方程求解命令]]。