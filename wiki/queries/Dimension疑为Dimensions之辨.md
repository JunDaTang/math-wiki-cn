---
type: query
title: "「Dimension[list]」疑为「Dimensions[list]」之辨"
tags: [mathematica, Dimensions, 函数名, 转写讹误, 校勘]
related: [10-数学手册原书第10版--15-2025-作为列表的向量和矩阵--o3sbi7, Mathematica列表与向量矩阵表示, 20-2-5全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.5 作为列表的向量和矩阵.md"]
---

# 「Dimension[list]」疑为「Dimensions[list]」之辨

## 疑点

原文 20.2.5.1：「运算 Dimension[list] 给出一个矩阵的大小（行列数），矩阵的结构由一个列表给定。」

## 分析

Mathematica 中查询列表/矩阵尺寸的内置函数名为 `Dimensions`（复数），并无名为 `Dimension` 的内置尺寸查询函数（此为可独立验证的公开文档背景）。两种可能：

1. **转写脱 s**（最可能）：中文释义「行列数」为复数语义，与 `Dimensions` 的复数形式呼应；
2. 原书排印即误。

## 佐证与影响

- 若为 `Dimensions`，则 `Dimensions[Array[b,{6,5}]]` 应返回 `{6,5}`，与式 (20.12) 的 (n,m) 型语义吻合；
- 已并入 [[20-2-5全节系统性转写讹误清单]] 类别四；[[Mathematica列表与向量矩阵表示]] 的命令一览表中已按 `Dimensions` 转录并加注。

## 待办

- [ ] 原书核对；若确认脱 s，在转录中以 `Dimensions[list]` 修正并加注。