---
type: concept
title: 延迟赋值（SetDelayed 与 RuleDelayed）
tags: [Mathematica, SetDelayed, RuleDelayed, 延迟求值, 延迟赋值]
related: [entities/mathematica, concepts/Set指派与清除, concepts/Rule变换规则与替换算子, concepts/Mathematica完全形式与中置算子, comparisons/即时赋值与延迟赋值比较]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# 延迟赋值（SetDelayed 与 RuleDelayed）

**延迟赋值**是 [[entities/mathematica|Mathematica]] 中与即时求值相对的两组算子的统称：`u := v`（完全形式 `SetDelayed[u, v]`）与 `u :> v`（完全形式 `RuleDelayed[u, v]`）。据《数学手册（原书第10版）》20.2.3（式 20.8a–20.8b）：

```
u := v  的 FullForm 是 SetDelayed[u, v]     (20.8a)
u :> v  的 FullForm 是 RuleDelayed[u, v]    (20.8b)
```

（原书 (20.8b) 左端排作 `u :-> v`，系排版形；标准输入形式为 `u :> v`。）

## 语义

- 指派或变换规则在此同样有效，直到它被改变（改变途径与 Set/Rule 相同：新指派、`x = .` 即 `Unset[x]`、`Clear[x]`，见 [[concepts/Set指派与清除]]）。
- 尽管左手边总是被右手边取代，但只有当**调用左手边的那一刻**，右手边才第一次算出值来——右端的求值被推迟到每次实际使用之时。

## 与即时算子的对照

Set/Rule 在指派或建立规则之时即刻求出右端的值，此后每次调用左端都被这个**已求值**的右端取代；SetDelayed/RuleDelayed 则把求值推迟到调用时刻。逐项对照见 [[comparisons/即时赋值与延迟赋值比较]]。该语义与 Mathematica 官方文档一致，可独立复核。

转录与复算见 [[findings/式20-8a至20-8b延迟赋值完全形式转录复算]]；完全形式的对应结构见 [[concepts/Mathematica完全形式与中置算子]]。