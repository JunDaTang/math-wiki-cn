---
type: concept
title: "表达式（Mathematica）"
tags: [mathematica, 表达式, 语法, 计算机代数系统]
related: [mathematica, FullForm（完整形式）, Part（部件提取与头）, Mathematica符号命名规则, 交互程序系统与计算机代数系统]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.1 Mathematica的基本结构要素.md"]
---

# 表达式（Mathematica）

**表达式（expression）是 [[entities/mathematica]] 的基本结构要素**：Mathematica 中的对象被组织为形如 `obj_0[obj_1, ..., obj_n]`（式 20.4）的统一结构。obj₀ 称为表达式的**头**（head），对它指派了数 0；objᵢ（i = 1, …, n）称为表达式的**元素**或**自变量**，可以用它们的数 1, …, n 指称。此定义出自《数学手册（原书第10版）》20.2.1 节。

（独立可验证背景：在 Wolfram Language 的官方语义中「一切皆表达式」——数、符号、图形乃至程序本身都具有头与元素的结构，头可用 Head 查询。手册本节仅就基本结构要素立论，未展开此普遍性。）

## 句法（式 20.4）

```
obj_0[obj_1, obj_2, ..., obj_n]
```

要点：

- **头**：在许多情形中，表达式的头是一个算子或函数，元素则是头所作用的运算对象或变元。
- **头也可以是表达式**：头作为一个表达式的元素本身也可以是表达式，故表达式可任意嵌套（如 `Plus[1, Times[2, x], Power[x, 2]]` 中 Times、Power 均为子表达式的头）。
- **方括号的专用性**：Mathematica 中的方括号专门用来表示一个表达式，只能用于这种关系。

## 表示法：中缀仅为便利

数学算式既可按键盘的中缀形式键入（如 `x^2 + 2*x + 1`），也可按更漂亮也更可取的形式 x² + 2x + 1 键入；但其内部表示是前缀的完整形式（FullForm），如 `Plus[1, Times[2, x], Power[x, 2]]`。所有单一的数学算子都存在用于内部表示的前缀形式，项表示法只是 Mathematica 的一个方便功能。详见 [[concepts/FullForm（完整形式）]]。

## 部件提取

表达式的部分可以被分离：`Part[expr, i]` 取出编号为 i 的元素（编号 1, …, n），i = 0 时得到该表达式的头（源文此处脱「i = 0」，见 [[queries/Part之i等于0脱文之辨]]）。详见 [[concepts/Part（部件提取与头）]]。

## 会话记号（In / Out / % / 分号 / SHIFT ENTER）

- 输入以 `In[k] :=` 编号、输出以 `Out[k] =` 编号；SHIFT 与 ENTER 键一起按下时触发求值。
- Mathematica 分析输入后将其**复原为数学标准形式**（如 `x^2 + 2x + 1` 的输出为 `1 + 2x + x^2`，由例可见多项式按升幂排列）。
- **% 引用**：方括号中的符号 % 告诉 Mathematica 这次输入的自变量是上一次的输出。
- **输出抑制**：如果输入以分号结束，则输出将被禁止。

19.8.4 节的 Mathematica 算例同样使用 In/Out 记法，两节记法一致（见 [[sources/10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm]]）。注意：以上为 Mathematica 的交互机制，不应未经核对即套用于 [[entities/maple]] 或 [[entities/matlab]]（如 % 引用并非三系统通用记法）；跨系统对照见 [[comparisons/Matlab-Mathematica-Maple同题数值比较]]。

## 符号

构成表达式的符号遵循 Mathematica 的命名规则（字母数字序列、不以数字开头、允许 $、区分大小写、保留符号大写或 $ 开头、用户符号建议小写开头），详见 [[concepts/Mathematica符号命名规则]]。