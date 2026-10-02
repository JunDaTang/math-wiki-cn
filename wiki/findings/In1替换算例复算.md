---
type: finding
title: "In[1] 替换算例复算"
tags: [Mathematica, 替换算子, ReplaceAll, Rule, 算例复算]
related: [concepts/Rule变换规则与替换算子, concepts/Mathematica输入输出行记法, queries/Replace疑为ReplaceAll之辨]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.3 重要算子.md"]
source: "[[sources/10-数学手册原书第10版--9-2023-重要算子--ztnien]]"
confidence: high
replicated: true
---

# In[1] 替换算例复算

## 转录（源文档）

```
In[1]:= x + y^2 /. y -> a + b
Out[1] = (a + b)^2 + x
```

## 复算结论

复算**通过**：对 `x + y^2` 施行 `/. y -> a + b`，得 `(a + b)^2 + x`。各项次序（幂项在前、x 在后）亦合 Mathematica 的规范序（standard order），与 Out[1] 完全一致。

## 附注

- 该算例是 [[concepts/Mathematica输入输出行记法]]（In[n]/Out[n] 行记法）在 20.2.3 的又一实例。
- 源文将 `/.` 与 `Replace[t, u->v]` 并称且描述为「每个出现将被替换」；按官方语义 `/.` 为 ReplaceAll（替换各层的每个出现），而 `Replace` 默认只作用于整个表达式。书中表述对应 ReplaceAll 的行为，见 [[queries/Replace疑为ReplaceAll之辨]]。算例中 `y^2` 内的 y 被替换，正是 ReplaceAll 行为的体现。

## 证据性质

直接证据：算例原文转录。复算为实际符号演算，可在任一 Mathematica 环境重演（replicated: true）。置信度：高。