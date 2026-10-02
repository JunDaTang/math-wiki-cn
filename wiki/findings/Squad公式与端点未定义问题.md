---
type: finding
title: Squad 公式与端点未定义问题（式 4.150）
created: 2026-09-30
updated: 2026-09-30
tags: [四元数, 插值, 样条, Squad]
related: [Squad, Slerp, 四元数]
sources: ["数学手册(原书第10版)/4.4.3 四元数的应用.md"]
source: "[[10-数学手册原书第10版--10-443-四元数的应用--1robxiu]]"
confidence: medium
replicated: null
---

# Squad 公式与端点未定义问题（式 4.150）

**发现**：《数学手册（原书第10版）》4.4.3.1 给出以 Slerp 为基元的序列样条插值 Squad：双层 Slerp 嵌套、外参 2t(1−t)；辅助点 s_i 的公式需要 q_{i−1} 与 q_{i+1}，因而**第一个与最后一个区间未被定义**，书中给出补救（s₀ = q₀、s_N = q_N 或补定义 q₋₁、q_{N+1}）。

## 公式（照录）

```latex
Squad(q_i, q_{i+1}, s_i, s_{i+1}, t)
  = Slerp( Slerp(q_i, q_{i+1}, t), Slerp(s_i, s_{i+1}, t), 2t(1-t) )       (4.150)

s_i = q_i exp( −( log(q_i⁻¹ q_{i+1}) + log(q_i⁻¹ q_{i-1}) ) / 4 )
```

## 要点

- 所得曲线类似贝济埃（Bezier）曲线，但代替线性插值保持了球面插值。
- 算法产生对四元数序列 q₀, q₁, …, q_N 的插值曲线。
- 端点区间未定义问题属于 Squad 本身，与 Lerp 的非等距缺陷、Slerp 的最短连接条件分属不同算法。
- 书中另点名 nlerp、log-lerp、islerp、四元数德卡斯特里奥样条（拼作 de Casteeljau）等算法，无展开。

## 复核状态

本条目为书中陈述的直接记录（直接证据）；分析者未对 (4.150) 做独立推导复核。Squad 为计算机图形学标准算法属背景知识，非本书主张。