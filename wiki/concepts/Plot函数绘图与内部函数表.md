---
type: concept
title: Plot 函数绘图与内部函数表
tags: [mathematica, 绘图, plot, 函数表]
related: [Graphics与Show图形对象, 图形选项（Mathematica）, 图形基元（Mathematica）, InputForm图形对象内部结构转录校勘, 式20-39至20-43函数绘图与Show复算, 式20-44a-b贝塞尔函数绘图复算, 奇点邻域高精度端点绘图法, 模式（Mathematica）]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# Plot 函数绘图与内部函数表

`Plot` 是 Mathematica 中供函数图形表示的专用命令（式 20.39）。其机制为：Mathematica 通过内部算法产生一个**函数表**，接着利用图形基元从这个表产生图形——`InputForm[%]` 证实所用基元为 `Line`，即图形对象表达式的第一个子列表包含「（稍作修改的）Line 基元」，第二个子列表包含所给图形所需的（默认）选项。

## 命令签名

```mathematica
Plot[f[x], {x, xmin, xmax}]                          (20.39)
Plot[{f1[x], f2[x], ...}, {x, xmin, xmax}]           (20.41)
```

函数的图形被表示在 x = xmin 与 x = xmax 之间的定义域上；式 20.41 在同一个图形中显示不同的函数。

## 默认行为与选项后置

Mathematica 描绘图形时使用某些默认图形选项：坐标轴自动绘制，刻度由相应的 x 值标记，缺省 `AspectRatio` 为 1:GoldenRatio（图 20.3 中整个宽与整个高之比 1:0.618 可观察）。若要在某个位置改变图像，「在主输入后必须在 Plot 命令中进行新的设置」，且选项可一个接一个连给多个，如式 20.40：

```mathematica
In[1] := Plot[Sin[2 x], {x, -2 Pi, 2 Pi}]
In[2] := Plot[Sin[2 x], {x, -2 Pi, 2 Pi}, AspectRatio -> 1]   (20.40)
```

`AspectRatio -> 1` 使图像按等长的 x 轴和 y 轴描绘。更多选项见 [[图形选项（Mathematica）]]。

## 算例族

- **指数函数族**（20.4.5.1）：以模式定义 `f[x_] := 2^x` 等（[[模式（Mathematica）]]）五个函数，分三图绘制（其中两组用 `PlotStyle->Dashing` 虚线区分），再 `Show[{p1, p2, p3}, PlotRange -> {0, 18}, AspectRatio -> 1.2]` 合并（图 20.4a）；e^x 已内置无需定义。
- **y = x + ArcCoth[x]**（20.4.5.2）：两支分别绘制后 `Show` 合并，并手工设定 `Ticks`、`AxesOrigin`；奇点 ±1 邻域的高精度端点取法见 [[奇点邻域高精度端点绘图法]]。
- **贝塞尔函数**（20.4.5.3，式 20.44a–b）：`Plot[{BesselJ[0, z], BesselJ[2, z], BesselJ[4, z]}, {z, 0, 10}, PlotLabel->TraditionalForm[...]]` 两组，再以 `GraphicsRow` 并排（[[式20-44a-b贝塞尔函数绘图复算]]）。

复算记录见 [[式20-39至20-43函数绘图与Show复算]]；内部结构剖析见 [[InputForm图形对象内部结构转录校勘]]。