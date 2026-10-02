---
type: concept
title: Graphics 与 Show 图形对象
tags: [mathematica, 绘图, 图形对象, 表达式]
related: [图形基元（Mathematica）, 图形选项（Mathematica）, Plot函数绘图与内部函数表, GraphicsArray与GraphicsRow比较, 表达式（Mathematica）, Set指派与清除, FullForm（完整形式）, InputForm图形对象内部结构转录校勘]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# Graphics 与 Show 图形对象

`Graphics[list]` 与 `Show` 是 Mathematica 图形体系的操作骨架：前者由图形基元的列表生成图形对象，后者显示并重显图形。按《数学手册（原书第10版）》20.4.1，`Graphics[list]`（其中 list 是图形基元的一个列表）调用后从列出的对象生成一个图，这个对象列表可以遵从有关图像显示的一列选项。

## 图形对象是表达式

图形对象可用 `Set` 赋给变元（如 `g = Graphics[...]`、`g1 = Graphics[{o1, o2}]`，[[Set指派与清除]]），是 [[表达式（Mathematica）]] 的一等公民；用命令 `InputForm[%]`「可以显示图形对象的全部图像」——即揭示其内部结构：由基元子列表（含 `Line`）与默认选项子列表组成（[[InputForm图形对象内部结构转录校勘]]、[[FullForm（完整形式）]]）。

## Show 的用法谱系

- `Show[g]`：显示图形对象（式 20.37a–b 之后，得图 20.1）。
- `Show[g2, Axes -> True]`：显示并激活选项（式 20.38b，得图 20.2b）。
- `Show[plot, options]`（式 20.42）：「早先的图像可以由其他选项进行更新」。
- `Show[{p1, p2, p3}, PlotRange -> {0, 18}, AspectRatio -> 1.2]`：合并多个已生成图形并以新选项重显（指数函数族例 In[6]）。
- `Show[GraphicsArray[list]]`（式 20.43）：将图像一个接一个地从上到下摆放出来，或安排成矩阵形式（list 代表图形对象列表）。

## 版本张力

式 20.43 的 `GraphicsArray` 为 Mathematica 5 时代命令（v6 起弃用），而 20.4.5.3 贝塞尔函数例用 `GraphicsRow[{bj0, bj1}]`（v6+）横排两图——二者混用是本节（第10版旧稿局部增补）最重要的结构性特征，详见 [[GraphicsArray与GraphicsRow比较]]。

## 算例

式 20.37a–b（g 与 `Show[g]` → 图 20.1）与式 20.38a–b（g1、g2 与 `Show[g2, Axes->True]` → 图 20.2）的完整转录与复算见 [[式20-37至20-38b图形对象构建算例复算]]；Plot/Show 配合的函数绘图见 [[式20-39至20-43函数绘图与Show复算]]。