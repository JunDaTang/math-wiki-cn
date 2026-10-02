---
type: query
title: DR7 与 DR8 的 z 量词域是否应为自然数
tags: [校勘, 转写讹误, 整除法则]
related: [10-数学手册原书第10版--7-541-整除性--1bgclvy, 整除定义与dr1-dr12法则组, 5-4-1全节系统性转写讹误清单]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.4.1 整除性.md"]
---

# DR7 与 DR8 的 z 量词域是否应为自然数

## 问题

DR7（式 5.221：$a\mid b \Rightarrow a^z\mid b^z$）与 DR8（式 5.222：$a^z\mid b^z \wedge b\neq0 \Rightarrow a\mid b$）的转写均附「对每个 $z\in\mathbb{Z}$」。量词域是否应为 $\mathbb{N}$（或 $z\geqslant 1$）？

## 证据

- **DR8 反例**：取 $z=0$，则 $a^0\mid b^0$ 即 $1\mid 1$ 恒真；若 $b\neq0$，法则将推出任意 $a\mid b$（假）。故 $z=0$ 必须排除。
- **DR7**：$z<0$ 时 $a^z,b^z$ 非整数（除非 $a,b=\pm1$），陈述失去意义；$z=0$ 时 $1\mid 1$ 平凡真但无内容。
- 转写文本中该两式的数学主体已受损（「azlbz」「DRS」「b-/-」），量词域可能同样受损。

## 影响

引用 DR7/DR8 时须限定 $z\geqslant 1$（本 wiki 已按此标注为存疑复原）；需核原书确认原文的量词域。相关页面：[[findings/整除定义与dr1-dr12法则组]]。
