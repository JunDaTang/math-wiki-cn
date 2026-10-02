---
type: concept
title: Plot3D 与 ParametricPlot3D 三维绘图
tags: [mathematica, 绘图, 三维图形, 曲面]
related: [图形选项（Mathematica）, 二维与三维图形选项比较, ParametricPlot参数曲线绘图, 式20-46至20-49a三维绘图复算, 洛伦茨方程组, 20-4未入库回指缺口]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# Plot3D 与 ParametricPlot3D 三维绘图

Mathematica 提供三维图形基元与三维绘图专用命令族，可在三维空间中表示曲面（二元函数的图形）与空间曲线（例如以参数形式给定者）；「对于这些表示的引入类似于二维情形」，三维图形基元的详细描述见原书文献 [20.5]（未展开，[[20-4未入库回指缺口]]）。

## 命令签名

```mathematica
Plot3D[f[x, y], {x, xa, xe}, {y, ya, ye}]                                    (20.46)
ParametricPlot3D[{fx[t,u], fy[t,u], fz[t,u]}, {t, ta, te}, {u, ua, ue}]      (20.47)
ParametricPlot3D[{fx[t], fy[t], fz[t]}, {t, ta, te}]                         (20.48)
```

`Plot3D` 就其基本形式需要一个二元函数的定义和这两个变元的定义域，所有选项都有默认设置；式 20.47 描绘由双参数给出的曲面，式 20.48 生成由参数表示的三维曲线。三维选项（Boxed、HiddenSurface、ViewPoint、Shading、PlotRange 等，见 [[图形选项（Mathematica）]] 与 [[二维与三维图形选项比较]]）可按不同观点和视角表示观察对象。

## 算例（20.4.7.1 与 20.4.7.3）

```mathematica
In[1] := Plot3D[x^2 + y^2, {x, -5, 5}, {y, -5, 5}, PlotRange > {0, 25}]
In[2] := Plot3D[(1 - Sin[x]) (2 - cos[2 y]), {x, -2, 2}, {y, -2, 2}]
In[3] := ParametricPlot3D[{Cos[t] Cos[u], Sin[t] Cos[u], Sin[u]},
         {t, 0, 2 Pi} {u, -Pi/2, Pi/2}]
In[4] := ParametricPlot3D[{Cos[t], Sin[t], t/4}, {t, 0, 20}]           (20.49a)
```

- In[1] 为抛物面 z = x² + y²：选项 PlotRange 按所要求的 z 值给定（{0, 25}），「因为这个立体是在 z = 25 时切割的」；转写作 `PlotRange > {0, 25}` 脱箭头（[[PlotRange大于号疑为箭头之辨]]）。
- In[2] 之 `cos[2 y]` 小写：Mathematica 区分大小写，应为 `Cos[2 y]`，原样输入不可直接成图。
- In[3] 为球面参数化，两迭代器间转写脱逗号；In[4] 为螺旋线。式 20.49 仅有 a 无 b（[[式20-49无b之编号之辨]]）。

复算与校勘见 [[式20-46至20-49a三维绘图复算]]。

## 延伸

Mathematica 还提供更多命令生成密度图和轮廓图、条形图和扇形图，以及不同类型图的组合；「用 Mathematica 可以很容易地生成洛伦茨吸引子的图像（参见第 1153 17.2.4.3）」，为 [[洛伦茨方程组]] 的可视化提供侧证。