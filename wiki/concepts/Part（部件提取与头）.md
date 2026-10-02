---
type: concept
title: "Part（部件提取与头）"
tags: [mathematica, Part, 表达式, 部件提取]
related: [表达式（Mathematica）, FullForm（完整形式）, mathematica]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.1 Mathematica的基本结构要素.md"]
---

# Part（部件提取与头）

**Part 是 [[entities/mathematica]] 的内置函数，用于分离（提取）表达式的部件**：`Part[expr, i]` 取出表达式 expr 中编号为 i 的元素，其中 i 是对应元的数（元素按 [[concepts/表达式（Mathematica）]] 的约定以 1, …, n 编号）；当 i = 0 时得到的是该表达式的头。

## 关键脱文警示

《数学手册（原书第10版）》20.2.1 节源文作「特别 = 时得到的是该表达式的头」，句中脱「i = 0」，按上下文应为「特别 **i = 0** 时得到的是该表达式的头」。若不校勘，读者无法从文本得知 `Part[expr, 0]` 的语义，将直接误导对 Part 的理解。校勘证据与背景见 [[queries/Part之i等于0脱文之辨]]。

（独立可验证背景：`Part[expr, 0]` 取头是标准 Mathematica 语义，与 `Head[expr]` 等价；现代 Wolfram Language 中 Part 亦常写作 `expr[[i]]`。手册本节未涉及双括号简写。）

## 会话示例

```
In[2] := FullForm[%]
Out[2] = Plus[1, Times[2, x], Power[x, 2]]

In[3] := Part[%, 3] 为 Out[3] = x^2
```

对 Out[2] 的表达式取第 3 个元素得到 x²，即子表达式 `Power[x, 2]` 的显示形式——它本身仍然是一个表达式。此例可与 [[concepts/FullForm（完整形式）]] 及 [[findings/式20-4与In1至In3会话转录复算]] 对读。