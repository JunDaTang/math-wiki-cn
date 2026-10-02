---
type: concept
title: Set 指派与清除
tags: [Mathematica, Set, 指派, Unset, Clear, 即时求值]
related: [entities/mathematica, concepts/Mathematica完全形式与中置算子, concepts/Rule变换规则与替换算子, concepts/延迟赋值（SetDelayed与RuleDelayed）, comparisons/即时赋值与延迟赋值比较]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# Set 指派与清除

**Set 指派与清除**是 [[entities/mathematica|Mathematica]] 中以 `r = s`（完全形式 `Set[r, s]`）实现的值绑定机制，及其解除机制。据《数学手册（原书第10版）》20.2.3：

## 指派语义

- `Set[r, s]` 将右手边表达式 s 求值（s 如一个数）后，把该值指派给左手边的表达式 r（例如一个变元）。
- 由此开始，r 表示这个值，直到该指派被改变为止。
- 典型情况：进行指派后右手边即刻求出值来；因此后面每次调用时，左手边将被这个已算出值的右手边取代。

## 清除途径

指派的改变或解除有三条途径：

1. 作出一个新的指派（以新值覆盖旧值）；
2. `x = .`，即 `Unset[x]`，去除对 x 的指派；
3. `Clear[x]`，去除到目前为止的所有指派结构。

## 与相关机制的关系

- `Set` 的延迟对应物是 `SetDelayed`（`u := v`）：右端不在指派时求值，而在左端被调用时才首次求值，见 [[concepts/延迟赋值（SetDelayed与RuleDelayed）]] 与 [[comparisons/即时赋值与延迟赋值比较]]。
- `Rule`（`u -> v`）与 Set 共享「右手边即刻求值」的即时语义，但建立的是变换规则而非值绑定，见 [[concepts/Rule变换规则与替换算子]]。
- 中置形式 `r = s` 与完全形式 `Set[r, s]` 的对应关系见 [[concepts/Mathematica完全形式与中置算子]]。

以上语义与 Mathematica 官方文档一致，可独立复核。