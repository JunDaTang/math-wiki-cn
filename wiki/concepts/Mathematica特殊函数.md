---
type: concept
title: "Mathematica特殊函数"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 特殊函数, 贝塞尔函数, 勒让德多项式, 球面调和函数]
related: [entities/mathematica, concepts/Mathematica标准函数, concepts/切比雪夫多项式, concepts/拉盖尔多项式, concepts/埃尔米特多项式, findings/表20-7与20-8函数名清单转录校勘, queries/与第10版兼容的各版本所指之辨, sources/10-数学手册原书第10版--7-2026-函数--v9sqy0]
sources: ["数学手册(原书第10版)/20.2.6 函数.md"]
---
# Mathematica特殊函数

Mathematica特殊函数指 Mathematica 内建的非初等命名数学函数。据手册 20.2.6.2，Mathematica「还认识若干特殊函数」，手册列出其中的一些（表 20.8）：贝塞尔函数、变形贝塞尔函数、勒让德多项式与球面调和函数。

## 表 20.8 特殊函数

| 函数 | Mathematica 记号 |
|---|---|
| 贝塞尔函数 $J_n(z)$ 和 $Y_n(z)$ | `BesselJ[n,z]`, `BesselY[n,z]` |
| 变形贝塞尔函数 $I_n(z)$ 和 $K_n(z)$ | `BesselI[n,z]`, `BesselK[n,z]` |
| 勒让德多项式 $P_n(x)$ | `LegendreP[n,x]` |
| 球面调和函数 $Y_l^m(\vartheta,\phi)$ | `SphericalHarmonicY[l,m,θ,φ]` |

计 6 个记号，逐一核验均为合法内建记号，表内未发现转写讹误（[[findings/表20-7与20-8函数名清单转录校勘]]）。

## 版本注记：程序包陈述的时代性

原文：「更多的这种函数可以从 Mathematica 相应的专门程序包加载。」这反映手册成书时旧版 Mathematica 以专门程序包扩展函数库的机制；现代版本中大量特殊函数已内建。故此为版本时代性 caveat，不记为转写错误，同时为 [[queries/与第10版兼容的各版本所指之辨]] 提供断代证据。

另，文称「其中的一些」，不排除原书该表更长而被本源节录（低优先存疑）。

## 与正交函数家族的平行

手册第 19 章已入库的正交函数对象——[[concepts/切比雪夫多项式]]、[[concepts/拉盖尔多项式]]、[[concepts/埃尔米特多项式]]——与勒让德多项式同属经典正交多项式/函数家族；`LegendreP` 即勒让德多项式的 Mathematica 侧对应。本节仅表列而未展开，故贝塞尔函数、勒让德多项式、球面调和函数暂不单立概念页，待后续章节实质展开再议。