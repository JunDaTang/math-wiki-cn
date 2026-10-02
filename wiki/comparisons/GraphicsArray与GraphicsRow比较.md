---
type: comparison
title: GraphicsArray 与 GraphicsRow 比较
tags: [mathematica, 绘图, 版本考订, 多图排列]
related: [Graphics与Show图形对象, InputForm图形对象内部结构转录校勘, 图形选项（Mathematica）, 式20-39至20-43函数绘图与Show复算, 式20-44a-b贝塞尔函数绘图复算, 20-4全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# GraphicsArray 与 GraphicsRow 比较

`GraphicsArray` 与 `GraphicsRow` 是 Mathematica 中功能重叠但属于不同世代的两个多图排列命令。《数学手册（原书第10版）》20.4 节对二者的**混用**是本节最具复用价值的结构性发现：反映第10版在旧稿基础上局部增补、未全面统一版本基线。

## 对照表

| 维度 | `Show[GraphicsArray[list]]`（式 20.43） | `GraphicsRow[{bj0, bj1}]`（20.4.5.3 In[3]） |
|---|---|---|
| 功能 | 将图像一个接一个从上到下摆放，或安排成**矩阵形式**（二维布局） | 将图像**横排**成一行 |
| 调用方式 | 须经 `Show` 包装显示 | 直接调用即显示 |
| 所属世代 | Mathematica 5 及更早的多图排列命令 | v6（2007）起引入的新命令族（可独立验证的背景：同期另有 GraphicsColumn、GraphicsGrid 等变体） |
| 在本节的地位 | 20.4.4.2 的命令签名（式 20.43），无算例配图 | 20.4.5.3 贝塞尔函数例的实际用例（图 20.5 两幅接连显示） |

## 版本张力的证据链

- 旧世代特征：式 20.43 `GraphicsArray`；表 20.17 之 `HiddenSurface`、`Shading`（pre-v6 3D 选项）。
- 新世代特征：`GraphicsRow`（v6+）；InputForm 输出块的默认样式 `Directive[Opacity[1.], RGBColor[0.368417, 0.506779, 0.709798], AbsoluteThickness[1.6]]` 似为 v10 起（[[InputForm图形对象内部结构转录校勘]]）。
- 结论：本节文字与旧命令承自旧稿，而 InputForm 输出块与部分用例为后续版本环境下的增补；界定本节的 Mathematica 版本基线仍为开放问题（见下方待办与审查建议）。

## 使用注意

若按本节复算：在现代 Mathematica 中 `GraphicsArray` 已属弃用/遗留命令，多图排列宜改用 `GraphicsRow`/`GraphicsColumn`/`GraphicsGrid`；式 20.43 的语义（含矩阵排列）由 `GraphicsGrid` 承接。