---
type: concept
title: "列表（Mathematica）"
created: 2026-10-02
updated: 2026-10-02
tags: [Mathematica, List, 数据结构]
related: [mathematica, FullForm（完整形式）, 表达式（Mathematica）, Part（部件提取与头）, 嵌套列表, 列表元素选取命令, 列表运算命令, Table-Range-Array列表生成命令]
sources: ["数学手册(原书第10版)/20.2.4 列表.md"]
---

# 列表（Mathematica）

列表（List）是 Mathematica 中由几个对象汇集成的一个新对象：列表中每个对象仅由其在列表中的位置来区分，元素本身可为任意 Mathematica 表达式。《数学手册(原书第10版)》20.2.4 将列表定位为 Mathematica 处理整组量的重要工具，并称后者「在高维代数和分析中是重要的」（该句疑有转写讹误，见 [[20-2-4全节系统性转写讹误清单]]）。向量、矩阵等成组对象在 Mathematica 中即以列表及 [[嵌套列表]] 表示。

## 构造与显示

若元素可以简单地枚举出来，则列表的构造由式 (20.9) 的两个等价形式确定：

```text
List[a1, a2, a3, ...]  或  {a1, a2, a3, ...}      (20.9)
```

即 `List[a1, a2, ...]` 是完整形式、`{a1, a2, ...}` 是与之等价的短形式，直接印证 [[FullForm（完整形式）]] 与 [[表达式（Mathematica）]] 建立的「完整形式—短形式」框架。Mathematica 应用于列表输出的是短形式——结果被置于花括号中：

```text
In[1] := l1 = List[a1, a2, a3, a4, a5, a6]
        → Out[1] = {a1, a2, a3, a4, a5, a6}      (20.10)
```

## 操作体系

《数学手册(原书第10版)》以三张命令表给出列表操作的完整体系：

- [[列表元素选取命令]]（表 20.3）：First、Last、Most、Rest、Part、Take、Drop——按位置从既有列表选取元素，输出可为「子列表」；
- [[列表运算命令]]（表 20.4）：Position、MemberQ、Select、Cases、FreeQ、Prepend、Append、Insert、Delete、ReplacePart——检验、扩展、缩短三类运算；
- [[Table-Range-Array列表生成命令]]（表 20.5 及 Range、Array）：按规则批量创建列表，其中 Table 常出现在涉及数学函数的时候。

## 记法与校勘注记

本节算例使用 l1、l2、a1–a6、b11–b65 等符号（参见 [[Mathematica符号命名规则]]）；转写文本存在「ll」与「l1」混写。全节 In/Out 编号跨子节回卷，与 [[Mathematica输入输出行记法]] 所载 20.2.1 的连续编号会话习惯不一致。