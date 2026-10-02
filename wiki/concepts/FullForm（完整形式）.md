---
type: concept
title: "FullForm（完整形式）"
tags: [mathematica, FullForm, 表达式, 前缀表示法]
related: [表达式（Mathematica）, Part（部件提取与头）, mathematica]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.1 Mathematica的基本结构要素.md"]
---

# FullForm（完整形式）

**FullForm 是 [[entities/mathematica]] 的内置函数，用于给出一个表达式的完整形式（full form）**——即剥去中缀/项表示法等便利记法后、以 `头[元素, ...]` 前缀结构书写的表达式本身。例如项 `x^2 + 2*x + 1`（或更漂亮也更可取的形式 x² + 2x + 1）的完整形式为：

```
Plus[1, Times[2, x], Power[x, 2]]
```

其中 Plus、Times、Power 表示相应的算术运算（加、乘、幂），分别是该表达式及各子表达式的头。

## 核心论断

本例表明：**所有单一的数学算子都存在用于内部表示的前缀形式，而项（中缀）表示法只是 Mathematica 的一个方便功能。**（《数学手册（原书第10版）》20.2.1 节）换言之，中缀算式是输入/显示层面的便利记法，内部一律为前缀表达式。

两点限定：

- 手册仅就「数学算子」立论；按 [[concepts/表达式（Mathematica）]] 的定义，表达式结构本身是普遍的，前缀形式的适用面比手册此句字面所述更宽（表述偏窄，非错误）。
- 源文此句「存在用千在内部表示」之「千」为「于」之讹，且「Plus, Power Times」处脱逗号，见 [[queries/20-2-1全节系统性转写讹误清单]]。

## FullForm 的输出仍是表达式

`FullForm[expr]` 的输出（如上式）本身也是一个表达式，因而可以继续被处理——例如用 Part 取其元素：

```
In[2] := FullForm[%]
Out[2] = Plus[1, Times[2, x], Power[x, 2]]

In[3] := Part[%, 3] 为 Out[3] = x^2
```

（In[3] 行之「为」疑为「则」，见讹误清单。）Out[3] 的 x² 即 `Power[x, 2]` 的显示形式，仍然是表达式。详见 [[concepts/Part（部件提取与头）]] 与 [[findings/式20-4与In1至In3会话转录复算]]。