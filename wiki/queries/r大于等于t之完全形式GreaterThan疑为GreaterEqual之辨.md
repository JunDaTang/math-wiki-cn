---
type: query
title: "「r ≥ t 之完全形式 GreaterThan[r, t]」疑为「GreaterEqual[r, t]」之辨"
tags: [Mathematica, GreaterEqual, GreaterThan, 表20-2, 疑讹]
related: [sources/10-数学手册原书第10版--9-2023-重要算子--ztnien, findings/表20-2算子与完全形式对应转录复算, concepts/Mathematica完全形式与中置算子, entities/mathematica, queries/20-2-3全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# 「r ≥ t 之完全形式 GreaterThan[r, t]」疑为「GreaterEqual[r, t]」之辨

## 问题

表 20.2 将中置形式 `r ≥ t` 的完全形式记为 `GreaterThan[r, t]`。这是转写之讹，还是原书之误？

## 内部证据（疑讹理由）

1. 表内上一行已将 `r > t`（严格大于）的完全形式记为 `Greater[r, t]`；`≥` 若再作 GreaterThan，与严格大于的命名体系内部不谐。
2. 依 Mathematica 官方语义（可独立复核的背景）：`≥` 的完全形式是 `GreaterEqual[r, t]`。
3. 即便现代 Wolfram Language 中存在 `GreaterThan`，其亦为一元算子形式构造器（operator form，如 `GreaterThan[3]`），绝非 `≥` 的二参头部。
4. 同表其余 11 行均与实际语义一致，唯此行可疑；且本节转写层讹误密集（见 [[queries/20-2-3全节系统性转写讹误清单]]），转写致讹的可能性不低。

## 查证途径

- 对照原版（德文/英文）表 20.2 中 `r ≥ t` 一行的原文，判定 GreaterThan 是转写之讹还是原书之误。
- 若为原书之误，应在相关页面加注勘误。

## 关联

- 转录与逐行核对：[[findings/表20-2算子与完全形式对应转录复算]]
- 概念背景：[[concepts/Mathematica完全形式与中置算子]]