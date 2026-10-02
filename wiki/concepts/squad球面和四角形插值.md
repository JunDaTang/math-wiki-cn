---
type: concept
title: Squad（球面和四角形插值）
created: 2026-09-30
updated: 2026-09-30
tags: [四元数, 插值, 样条, 计算机图形学]
related: [Slerp, Lerp, 四元数]
sources: ["数学手册(原书第10版)/4.4.3 四元数的应用.md"]
---

# Squad（球面和四角形插值）

Squad（spherical and quadrangle interpolation，球面和四角形插值）是以 [[concepts/Slerp]] 为基元、对四元数**序列** q₀, q₁, …, q_N 构造插值样条的算法，由《数学手册（原书第10版）》4.4.3.1 引入。它以类贝济埃（Bezier）曲线的方式、用球面插值代替线性插值，用于计算机绘图学中刻画穿过多个给定旋转的运动流。

## 公式

```latex
Squad(q_i, q_{i+1}, s_i, s_{i+1}, t)
  = Slerp( Slerp(q_i, q_{i+1}, t), Slerp(s_i, s_{i+1}, t), 2t(1-t) )       (4.150)

s_i = q_i exp( −( log(q_i⁻¹ q_{i+1}) + log(q_i⁻¹ q_{i-1}) ) / 4 )
```

即先在「内」边 q_i→q_{i+1} 与「外」边 s_i→s_{i+1} 上各做一次 Slerp，再以 2t(1−t)（在 t = ½ 达到 1、端点为 0）为参数在两者之间做第二次 Slerp。

## 端点区间未定义问题

s_i 的计算需要 q_{i−1} 与 q_{i+1}，故 s₀ 需要 q₋₁、s_N 需要 q_{N+1}——序列两端缺值，**第一个与最后一个区间的表达式未被定义**。书中补救：取 s₀ = q₀、s_N = q_N，或者补定义 q₋₁ 与 q_{N+1}。该问题属于 Squad，不属于 [[concepts/Lerp]]（非等距缺陷）或 [[concepts/Slerp]]（最短连接条件）。

## 相关算法（书中仅点名，无展开）

nlerp、log-lerp、islerp、四元数德卡斯特里奥样条（书中拼作 de Casteeljau，通常拼作 de Casteljau）。贝济埃曲线仅作类比。见 [[findings/Squad公式与端点未定义问题]]。