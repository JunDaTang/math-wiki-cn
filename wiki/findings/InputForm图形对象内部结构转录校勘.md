---
type: finding
title: InputForm 图形对象内部结构转录校勘
tags: [mathematica, 绘图, inputform, 校勘, 版本考订]
related: [Plot函数绘图与内部函数表, Graphics与Show图形对象, 图形选项（Mathematica）, Axex疑为Axes之辨, GraphicsArray与GraphicsRow比较, 20-4全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
source: "[[10-数学手册原书第10版--18-204-用mathematica绘图--f10hmv]]"
confidence: high
replicated: null
---

# InputForm 图形对象内部结构转录校勘

## 背景

20.4.4.2 指出「使用命令 InputForm[％] 可以显示图形对象的全部图像」（「全部图像」疑为「全部内容/内部结构」之表述），并给出 Plot[Sin[2 x], {x, -2 Pi, 2 Pi}] 之后 InputForm[%] 的输出块。该输出块是全节转写讹误最密集处，也是版本考订的关键证据。

## 转录（原样）

```txt
Graphics[{{}, {}, {Directive[Opacity[1.], RGBColor[0.368417, 0.506779, 0.709798], AbsoluteThickness[1.6]], Line[{{-6.283185050723043, 2.5645654335783057*^{-7}}, ..., {6.283185050723043, -2.5645654335783057*^{-7}}}], {DisplayFunction->Identity, AspectRatio->GoldenRatio(-1), Axex->{True, True}, AxesLabel->{None, None}AxesOrigin->{0, 0}, DisplayFunction :> Identity, Frame->{{False, False}, {False, False}}, FrameLabel->{{None, None}, {None, None}}, FrameTicks->{{Automatic, Automatic}, {Automatic, Automatic}}, GridLines->{None, None}, GridLinesStyle->Directive[GrayLevel[0.5, 0.4]], Method->{"DefaultBoundaryStyle" -> Automatic," ScalingFunctions" -> None}, PlotRange->{{-2 * Pi, 2 * Pi}, {-0.9999996654606427, 0.9999993654113022}}, PlotRangeClipping->True, PlotRangePadding->{{Scaled[0.02], Scaled[0.02]}, {Scaled[0.05], Scaled[0.05]}}, Ticks->{Automatic, Automatic}}]
```

## 结构解读（与正文互证）

- 图形对象由子列表组成：第一个子列表包含图形基元 `Line`（「稍作修改」，前置 `{}`、`{}` 空注记列表与 `Directive[...]` 样式指示），证实 Plot「内部算法产生函数表→Line 基元连线」的机制（[[Plot函数绘图与内部函数表]]）。
- 第二个子列表包含默认选项（AspectRatio、Axes、Frame、PlotRange、Ticks 等），证实「这些是默认选项；若要改变图像须在 Plot 命令中进行新的设置」。

## 校勘清单

1. `Axex->{True, True}` → 应为 `Axes->{True, True}`（Mathematica 无 Axex 符号，[[Axex疑为Axes之辨]]）。
2. `AspectRatio->GoldenRatio(-1)` → 应为 `AspectRatio->GoldenRatio^(-1)`（脱幂记号）。
3. `2.5645654335783057*^{-7}` → 应为 `*^-7`（Mathematica 科学记法，脱脱字符「^」）。
4. `AxesLabel->{None, None}AxesOrigin->{0, 0}` → 两者间脱逗号。
5. `DisplayFunction->Identity` 与 `DisplayFunction :> Identity` 重复出现，疑转录重复（Rule 与 RuleDelayed 并存于同一选项列表不合常理，参见 [[延迟赋值（SetDelayed与RuleDelayed）]]）。
6. `" ScalingFunctions"` 多前导空格。
7. `PlotRange->{{-2 * Pi, 2 * Pi}, ...}` 存疑：真实 InputForm 输出应为已解析的机器数（如 {-6.283185307179586, 6.283185307179586}），此处 x 区间保留符号形式，疑为转写者规范化或原书排版；而 y 区间 {-0.9999996654606427, 0.9999993654113022} 为机器数，与真实输出同型。
8. 块首 `Graphics[{{}, {}, {Directive[...` 的双空列表结构与现代 Plot 输出一致，非讹误。

## 版本考订线索

`RGBColor[0.368417, 0.506779, 0.709798]` 与 `AbsoluteThickness[1.6]` 构成的默认绘图样式为 Mathematica v10 起的特征；与式 20.43 `GraphicsArray`、表 20.17 `HiddenSurface`/`Shading` 等 pre-v6 遗留并存，构成第10版本节「旧稿局部增补、未统一版本基线」的核心证据（[[GraphicsArray与GraphicsRow比较]]）。

## 证据强度

结构解读与当代 Mathematica 输出同型，校勘各条均为无歧义的字面错误（高置信）；但本 finding 未对原输出块逐字复算，replicated 记为 null。