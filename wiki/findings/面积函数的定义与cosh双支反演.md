---
type: finding
title: 面积函数的定义与 cosh 的双支反演（式 2.207–2.210）
tags: [面积函数, 反函数, 单调性]
related: [面积函数, 面积正弦函数, 面积余弦函数, 面积正切函数, 面积余切函数]
created: 2026-09-29
updated: 2026-09-29
source: "[[sources/10-数学手册原书第10版--8-210-面积函数--1cebibi]]"
confidence: high
replicated: null
sources: ["数学手册(原书第10版)/2.10 面积函数.md"]
---

# 面积函数的定义与 cosh 的双支反演（式 2.207–2.210）

**发现**：手册将面积函数定义为双曲函数的反函数。其中 sinh x、tanh x、coth x「均严格单调，因此没有任何限制地具有唯一反函数」；cosh x 有两个单调区间，因此存在两个反函数 y = Arcosh x 与 y = −Arcosh x。四个定义式为：

$$
y = \operatorname{Arsinh} x \tag{2.207}
$$

$$
y = \operatorname{Arcosh} x \ \text{和}\ y = - \operatorname{Arcosh} x \tag{2.208}
$$

$$
y = \operatorname{Artanh} x \tag{2.209}
$$

$$
y = \operatorname{Arcoth} x \tag{2.210}
$$

**证据强度**：强，属直接证据。单调性与双支结构均可由 2.9 节的指数定义（式 2.166–2.171）直接推导。

**局限与疑点**：coth「严格单调」的表述在全域标准下不成立——coth 在 ℝ\{0} 上跨 0 比较时方向反转，仅在两支上分别严格递减；但两支值域 (−∞, −1) 与 (1, +∞) 不相交，故 coth 仍为单射，唯一反函数的结论成立。表述与结论之间存在缝隙，详见 [[queries/coth严格单调表述是否应修正为两支递减]]。

另注：「面积」命名的几何依据（双曲线扇形面积）在本节仅作前向引用（第 172 页 3.1.2.2），未给出证明，属未展开的声明，见 [[queries/双曲线扇形面积的几何解释待验证]]。