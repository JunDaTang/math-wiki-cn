---
type: finding
title: k 阶等差级数的通项与求和公式（式 1.53c/1.53d）
created: 2026-09-29
updated: 2026-09-29
tags: [有限级数, 差分, 二项式系数]
related: [k阶等差级数, 差分, 二项式系数, 等差级数]
sources: ["数学手册(原书第10版)/1.2 有限级数.md"]
source: "[[10-数学手册原书第10版--7-12-有限级数--2sdpdk]]"
confidence: high
replicated: null
---

# k 阶等差级数的通项与求和公式（式 1.53c/1.53d）

手册 1.2.2.2 给出 k 阶等差级数（k 阶差分 $\Delta^k a_i$ 为常数的有限级数）的通项与前 n 项和公式：

$$
a_i = a_0 + \binom{i}{1}\Delta a_0 + \binom{i}{2}\Delta^2 a_0 + \cdots + \binom{i}{k}\Delta^k a_0 \quad (i = 1, 2, \cdots, n),
$$

$$
s_n = \binom{n+1}{1}a_0 + \binom{n+1}{2}\Delta a_0 + \binom{n+1}{3}\Delta^2 a_0 + \cdots + \binom{n+1}{k+1}\Delta^k a_0.
$$

两者都由差分表首列 $a_0, \Delta a_0, \cdots, \Delta^k a_0$ 与二项式系数完全确定。

## 验证状态

- 证据类型：直接陈述（手册编号公式），无证明。
- 入库分析阶段的推导性核验：将通项式对 $i$ 从 0 到 $n$ 求和，并使用 hockey-stick 恒等式 $\sum_{i=0}^{n}\binom{i}{j} = \binom{n+1}{j+1}$，即可由 (1.53c) 得到 (1.53d)。
- 数值抽查（直接代入，非本源内容）：取 $a_i = i^2$（二阶等差：$a_0 = 0$，$\Delta a_0 = 1$，$\Delta^2 a_0 = 2$），$n = 2$ 时 $s_2 = \binom{3}{1}\cdot 0 + \binom{3}{2}\cdot 1 + \binom{3}{3}\cdot 2 = 5 = 0^2 + 1^2 + 2^2$，符合 (1.53d)。

## 指标约定注意

(1.53c/1.53d) 沿用 1.2.1–1.2.3 的 **0 起指标**：$s_n$ 表示 $a_0, \cdots, a_n$ 共 $n+1$ 项之和。这与 1.2.4 特殊求和公式 (1.55)–(1.63) 及 1.2.5 均值定义的 1 起指标不同，套用公式时须注意项数差异。

## 关联

概念背景见 [[concepts/k阶等差级数]] 与 [[concepts/差分]]；系数结构见 [[concepts/二项式系数]] 与 [[concepts/帕斯卡三角形]]。手册未为 (1.53c) 命名，其与 Newton 前向差分公式的关系见 [[queries/手册是否在别处命名k阶等差级数通项公式]]。
