---
type: concept
title: Rule 变换规则与替换算子
tags: [Mathematica, Rule, ReplaceAll, 替换算子, 变换规则, 公式操作]
related: [entities/mathematica, concepts/公式操作, concepts/Set指派与清除, concepts/Mathematica完全形式与中置算子, concepts/Equal恒等判定与方程表示, queries/Replace疑为ReplaceAll之辨]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
---

# Rule 变换规则与替换算子

**Rule 变换规则与替换算子**是 [[entities/mathematica|Mathematica]] 中实现符号替换的机制：`u -> v`（完全形式 `Rule[u, v]`）建立一条变换规则，配合替换算子 `/.` 使用，可将表达式中子表达式的出现替换为另一表达式。据《数学手册（原书第10版）》20.2.3：

- `Rule[u, v]` 应被看成一种变换规则，它与替换算子一同出现。
- `Replace[t, u->v]` 或 `t /. u->v`：表达式 t 中 u 的每个出现将被替换为表达式 v。
- 与 Set 一样，Rule 的典型情况是运用变换规则后右手边即刻求出值来（即时求值语义，见 [[concepts/Set指派与清除]]）。

## 已验证算例

```
In[1]:= x + y^2 /. y -> a + b
Out[1] = (a + b)^2 + x
```

复算通过，各项次序亦合 Mathematica 规范序，见 [[findings/In1替换算例复算]]。该算例同时是 [[concepts/Mathematica输入输出行记法]] 的又一实例。

## Replace 与 ReplaceAll 之辨

依 Mathematica 官方语义（独立可复核的背景）：`t /. u->v` 中的 `/.` 实为 **ReplaceAll**，作用于表达式各层的每个匹配出现；而 `Replace[t, u->v]` 默认只作用于整个表达式 t 本身。书中「每个出现将被替换」的描述对应 ReplaceAll 的行为，与 Replace 并称疑脱「All」或原书表述不精，详见 [[queries/Replace疑为ReplaceAll之辨]]。

## 与公式操作的关系

Rule 与替换算子正是 [[concepts/公式操作]]（符号替换、公式变形）在 Mathematica 中的直接实现机制；与 [[concepts/Equal恒等判定与方程表示]] 一道，构成方程的符号表示与解之代入的自然载体——20.1 节的符号求解算例（见 [[findings/式20-1至20-3c符号与数值求解算例转录复算]]）已进入方程求解语境。