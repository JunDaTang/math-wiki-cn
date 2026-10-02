---
type: concept
title: 图形选项（Mathematica）
tags: [mathematica, 绘图, 图形选项]
related: [图形命令与相对绝对尺寸, Graphics与Show图形对象, Plot函数绘图与内部函数表, Plot3D与ParametricPlot3D三维绘图, 二维与三维图形选项比较, Rule变换规则与替换算子, 表20-14至20-17基元命令选项表转录]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# 图形选项（Mathematica）

图形选项是 Mathematica 中「对于整个图像的显示具有影响」的设置，区别于只作用于局部基元的图形命令（[[图形命令与相对绝对尺寸]]）。选项以 Rule（规则）形式给出（`名字 -> 值`，参见 [[Rule变换规则与替换算子]]），置于命令主参数之后且「可以一个接一个地同时给出若干选项」；对已生成的图形，可经 `Show[plot, options]` 以新选项更新重显（[[Graphics与Show图形对象]]）。

## 表 20.16 一些图形选项（原样转录）

```txt
AspectRatio -> w 设置高宽比 w. Automatic, 由绝对坐标确定 w;
默认设置为 w = 1 : GoldenRatio
Axes -> True 画坐标轴
Axes -> False 不画坐标轴
Axes -> {True, False} 仅显示 x 轴
Frame -> True 显示框
GridLines -> Automatic 显示网格线
AxesLabel -> {x_symbol, y_symbol} 以给定符号表示轴
Ticks -> Automatic 自动表示刻度标记; 使用 None 它们将被禁止
Ticks -> {{x₁, x₂, …}, {y₁, y₂, …}} 将刻度标记置于给定的节点处
```

## 表 20.17 3D 图形选项（原样转录）

```txt
Boxed 默认设置是 True; 它描绘一个环绕曲面的三维框
HiddenSurface 设置曲面的不透明度; 默认设置是 True
ViewPoint 指定空间中的点 (x, y, z)，由此处观察曲面. 默认值是 {1.3, -2.4, 2}
Shading 默认设置是 True; 在曲面上加阴影; False 得到白色曲面
PlotRange 对于值 All 可以选择 {za, ze}, {{xa, xe}, {ya, ye}, {za, ze}}. 默认是 Automatic
```

原书注明表 20.17 仅列举少数几个，「已知的 2D 图形选项没有包括在内。它们可以在类似的意义下被应用」（[[二维与三维图形选项比较]]）；选项 ViewPoint「特别重要」，利用它可以选取非常不同的观察视角。详细解释参见原书文献 [20.7]、[20.11]（未展开，[[20-4未入库回指缺口]]）。

## AspectRatio 默认值：本节反复强调的知识点

Mathematica 以缺省方式制作图形的高宽比为 1:GoldenRatio（沿 x 方向长度与沿 y 方向长度之比 1:1/1.618 = 1:0.618），会使圆变形为椭圆；选项值 `Automatic` 由绝对坐标确定、确保图像不变形。此默认在 20.4.1（式 20.37a–b 特意设 `AspectRatio->Automatic`）、图 20.3（Sin[2x] 图中宽高比 1:0.618 可观察）与 20.4.6（参数曲线自然形态）中反复出现；`InputForm[%]` 证实其为 `AspectRatio->GoldenRatio^(-1)`（[[InputForm图形对象内部结构转录校勘]]）；`AspectRatio->1` 则令 x、y 轴等长（式 20.40）。

## 在专用命令中的体现

`PlotRange`（抛物面例按所要求 z 值给定 {0, 25}）、`PlotLabel->TraditionalForm`（BesselJ 例）、`PlotStyle->Dashing`（指数族例）、`Ticks` 与 `AxesOrigin`（ArcCoth 例）等，均见 [[Plot函数绘图与内部函数表]]、[[Plot3D与ParametricPlot3D三维绘图]] 及相应复算页。版本注意：`HiddenSurface`、`Shading` 为 pre-v6 遗留选项，与 `GraphicsRow` 等 v6+ 特征并存于本节，见 [[GraphicsArray与GraphicsRow比较]]。