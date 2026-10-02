---
type: concept
title: Equal 恒等判定与方程表示
tags: [Mathematica, Equal, 恒同判定, 方程表示, 关系算子]
related: [entities/mathematica, concepts/Mathematica完全形式与中置算子, concepts/Rule变换规则与替换算子]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# Equal 恒等判定与方程表示

**Equal** 是 [[entities/mathematica|Mathematica]] 中以 `u == v`（完全形式 `Equal[u, v]`）表示的算子，兼具恒同判定与方程表示两重角色。据《数学手册（原书第10版）》20.2.3 节末：

- 如果 u、v 是恒同的，表达式 `u == v`（即 `Equal[u, v]`）回复 True。
- Equal 用于处理方程（原句「Equal 用千如处理方程中」有脱讹，「千」为「于」之讹）。

## 说明

- 在表 20.2 的关系算子族中，Equal 与 Unequal、Greater、Less、GreaterEqual、LessEqual 并列，完全形式均为 `算子[左端, 右端]` 的统一结构，见 [[concepts/Mathematica完全形式与中置算子]]。
- 「恒同」的判定较宽。依 Mathematica 官方语义（独立可复核的背景，用以界定书中「恒等」一词的含义）：仅当两端可被确认为同一表达式时 `Equal[u, v]` 才化简为 True；否则 `u == v` 保持未求值形式，正可用作方程的符号表示。
- 方程求解（20.1 节的符号求解算例见 [[findings/式20-1至20-3c符号与数值求解算例转录复算]]）以 Equal 表示方程、以 [[concepts/Rule变换规则与替换算子|Rule]] 表示解并代入，二者共同衔接方程处理主题。