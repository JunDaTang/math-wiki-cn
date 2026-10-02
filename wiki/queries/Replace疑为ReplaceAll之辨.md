---
type: query
title: "Replace[t, u->v] 之「每个出现」表述疑为 ReplaceAll 之辨"
tags: [Mathematica, Replace, ReplaceAll, 替换算子, 疑讹]
related: [sources/10-数学手册原书第10版--9-2023-重要算子--ztnien, findings/In1替换算例复算, concepts/Rule变换规则与替换算子, entities/mathematica, queries/20-2-3全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# Replace[t, u->v] 之「每个出现」表述疑为 ReplaceAll 之辨

## 问题

源文写道：`Replace[t, u->v]` 或 `t /. u->v` 意思是表达式 t 中 u 的每个出现将被替换为表达式 v。按 Mathematica 官方语义（可独立复核的背景）：

- `t /. u->v` 中的 `/.` 实为 **ReplaceAll**：替换表达式各层中 u 的每个出现；
- `Replace[t, u->v]` 默认只作用于整个表达式 t 本身（第 0 层），并不替换其内部的每个出现。

故书中「每个出现将被替换」的描述对应 ReplaceAll 的行为，与 Replace 并称疑脱「All」，或原书表述本就不精。

## 待查

1. 原版（德文/英文）此句是否作 ReplaceAll，抑或原文即作 Replace？
2. 若原书即作 Replace，属知识性小误还是排版简省？

## 已验证的相关事实

`In[1]:= x + y^2 /. y -> a + b` 的算例复算通过（见 [[findings/In1替换算例复算]]），其中 `y^2` 内的 y 被替换，正是 ReplaceAll 的行为。

## 关联

- 概念页：[[concepts/Rule变换规则与替换算子]]