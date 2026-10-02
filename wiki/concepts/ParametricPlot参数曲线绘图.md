---
type: concept
title: ParametricPlot 参数曲线绘图
tags: [mathematica, 绘图, 参数曲线, 螺线]
related: [Plot函数绘图与内部函数表, 图形选项（Mathematica）, 式20-45参数曲线螺线与次摆线复算, 20-4未入库回指缺口]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# ParametricPlot 参数曲线绘图

`ParametricPlot` 是 Mathematica 描绘由参数形式给出的曲线的专用命令（式 20.45）：

```mathematica
ParametricPlot[{fx(t), fy(t)}, {t, t1, t2}]          (20.45)
```

它「提供了在一个图形中显示多条曲线的可能性」，此时命令中必须给出若干曲线的一个列表。

## AspectRatio->Automatic：自然形态

利用选项 `AspectRatio->Automatic`，Mathematica「以其自然形式显示曲线」，即不因缺省高宽比 1:GoldenRatio 而变形（[[图形选项（Mathematica）]]）。原文此处转写作 `AspectRatio_lutomatic_1`，系 `AspectRatio->Automatic` 之讹（[[20-4全节系统性转写讹误清单]]）。

## 算例（20.4.6）

```mathematica
In[1] := ParametricPlot[{t   Cos[t], t   Sin[t]}, {t, 0, 3 Pi}, AspectRatio->Automatic]
In[2] := ParametricPlot[{Exp[0.1 t] Cos[t], Exp[0.1 t] Sin[t]}, {t, 0, 3 Pi},
         AspectRatio->Automatic]
In[3] := ParametricPlot[{t - 2 Sin[t], 1 - 2 Cos[t]}, {t, -Pi, 11 Pi}, AspectRatio -> 0.3]
```

- In[1] 为**阿基米德螺线**（回指第 136 页 2.14.1）；转写「t   Cos[t]」的多空格在 Mathematica 中即乘法（空格分隔的相邻因子相乘），未必为脱乘号之讹。
- In[2] 为**对数螺线**（回指第 137 页 2.14.3）。
- In[3] 为**次摆线**（回指第 132 页 2.13.2），此时反而显式取 `AspectRatio -> 0.3` 压扁纵横比以呈现其扁平周期形态。

复算记录见 [[式20-45参数曲线螺线与次摆线复算]]；所回指的手册前部章节均未入库，见 [[20-4未入库回指缺口]]。三维对应命令见 [[Plot3D与ParametricPlot3D三维绘图]]。