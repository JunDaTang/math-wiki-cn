---
type: concept
title: Mathematica 完全形式与中置算子
tags: [Mathematica, 完全形式, 中置算子, FullForm, 表达式结构]
related: [entities/mathematica, concepts/Mathematica输入输出行记法, concepts/Set指派与清除, concepts/Rule变换规则与替换算子, concepts/Equal恒等判定与方程表示, queries/r大于等于t之完全形式GreaterThan疑为GreaterEqual之辨, queries/20-2未入库回指缺口]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# Mathematica 完全形式与中置算子

**完全形式与中置记法**是 [[entities/mathematica|Mathematica]] 统一表达式结构的两个侧面：Mathematica 中的一切都是形如 `头[参数1, 参数2, ...]` 的表达式；为贴近数学中的经典写法，许多基本算子可写成中置形式 `symb1 op symb2`，而无论哪种情形，这一简化记法的完整形式（full form）都是表达式 `op[symb1, symb2]`。

《数学手册（原书第10版）》20.2.3 以表 20.2 汇集了最常出现的算子及其完全形式（12 组对照的逐格转录与核对见 [[findings/表20-2算子与完全形式对应转录复算]]），重排为单列对照如下：

| 中置形式 | 完全形式 |
|---|---|
| a + b | Plus[a, b] |
| a b 或 a * b | Times[a, b] |
| a^b | Power[a, b] |
| a/b | Times[a, Power[b, -1]] |
| u -> v | Rule[u, v] |
| r = s | Set[r, s] |
| u == v | Equal[u, v] |
| w != v | Unequal[w, v] |
| r > t | Greater[r, t] |
| r ≥ t | GreaterEqual[r, t]（原表作 GreaterThan[r, t]，疑讹） |
| s < t | Less[s, t] |
| s ≤ t | LessEqual[s, t] |

## 要点

- **除法即乘逆**：`a/b` 的完全形式不是某个 Divide 头部，而是 `Times[a, Power[b, -1]]`——除法在 Mathematica 中被规约为乘法与幂的复合。
- **隐含乘法的空隙**：形如 `a b` 的乘法中，两因子之间的空隙非常重要；`ab`（无空隙）会被解析为单一符号而非乘积。这是最常见的输入错误之一。
- **关系算子同构**：`==`、`!=`、`>`、`<`、`≥`、`≤` 的完全形式分别为 Equal、Unequal、Greater、Less、GreaterEqual、LessEqual，与四则算子共享同一「头—参数」结构（见 [[concepts/Equal恒等判定与方程表示]]）。
- **求值语义由完全形式决定**：`Set[r, s]`、`Rule[u, v]` 与其延迟对应物 `SetDelayed[u, v]`、`RuleDelayed[u, v]` 的即时/延迟求值之别，正是在完全形式层面定义的（见 [[concepts/Set指派与清除]]、[[concepts/Rule变换规则与替换算子]]、[[concepts/延迟赋值（SetDelayed与RuleDelayed）]]、[[comparisons/即时赋值与延迟赋值比较]]）。

`r ≥ t` 一行按原表转录为 `GreaterThan[r, t]`，与 Mathematica 实际语义不符，辨析见 [[queries/r大于等于t之完全形式GreaterThan疑为GreaterEqual之辨]]。

FullForm 可将任一表达式显示为完全形式；该函数及「头」（Head）的正式定义位于手册尚未入库的 20.2.1/20.2.2 小节（见 [[queries/20-2未入库回指缺口]]）。