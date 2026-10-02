---
type: concept
title: k 阶等差级数
created: 2026-09-29
updated: 2026-09-29
tags: [有限级数, 差分, 二项式系数]
related: [等差级数, 差分, 二项式系数, 帕斯卡三角形, 有限级数, k阶等差级数的差分表示公式]
sources: ["数学手册(原书第10版)/1.2 有限级数.md"]
---

# k 阶等差级数

k 阶等差级数是其项构成的序列 $a_0, a_1, a_2, \cdots, a_n$ 的 k 阶差分 $\Delta^k a_i$ 为常数的有限级数。它是《数学手册(原书第10版)》1.2.2.2 对一阶等差级数（见 [[concepts/等差级数]]）的推广：$k=1$ 时即通常的等差级数，幂和（如 $\sum i^2$、$\sum i^3$）都是其典型例子。

## 高阶差分

一阶差分为 $\Delta a_i = a_{i+1} - a_i$；高阶差分按递推式 (1.53a) 计算：

$$
\Delta^{v} a_i = \Delta^{v-1} a_{i+1} - \Delta^{v-1} a_i \quad (v = 2, 3, \cdots, k).
$$

各阶差分可排成差分表（三角模式，式 1.53b）方便读取，详见 [[concepts/差分]]。

## 通项与求和公式

手册给出（式 1.53c、1.53d）：

$$
a_i = a_0 + \binom{i}{1}\Delta a_0 + \binom{i}{2}\Delta^2 a_0 + \cdots + \binom{i}{k}\Delta^k a_0 \quad (i = 1, 2, \cdots, n),
$$

$$
s_n = \binom{n+1}{1}a_0 + \binom{n+1}{2}\Delta a_0 + \binom{n+1}{3}\Delta^2 a_0 + \cdots + \binom{n+1}{k+1}\Delta^k a_0.
$$

即通项与前 n 项和都由差分表首列 $a_0, \Delta a_0, \cdots, \Delta^k a_0$ 与 [[concepts/二项式系数]] 完全表出；求和公式中系数 $\binom{n+1}{j+1}$ 的结构正是 [[concepts/帕斯卡三角形]] 的斜向求和（hockey-stick 恒等式 $\sum_{i}\binom{i}{j} = \binom{n+1}{j+1}$）。

## 未命名的公式

手册对式 (1.53c) 未作命名。（可独立验证的背景：该式即 Newton 前向差分公式的序列形式——以等距点列上的各阶差分为系数的二项式展开；此名称与语境不见于手册 1.2 节。）手册是否在别处（如第 7 章级数或数值分析章节）命名或推导此式，见 [[queries/手册是否在别处命名k阶等差级数通项公式]]。

验证状态与指标约定注意见 [[findings/k阶等差级数的差分表示公式]]。
