---
type: entity
title: NAG 图书馆
created: 2026-10-01
updated: 2026-10-01
tags: [数值程序库, NAG, FORTRAN, 统计软件, 金融数学]
related: [10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc, IMSL图书馆, Aachen图书馆, 数值方法图书馆, 19-8-3三馆目录与语言清单转录校勘, 19-8-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/19.8.3 数值方法图书馆.md"]
---
# NAG 图书馆

NAG 图书馆是数值算法组（Numerical Algorithms Group，NAG）开发的数值计算程序库，以函数与子程序形式集成大量数值方法，供科学与工程计算调用。（独立可查之公共背景：NAG 为源自英国牛津的数值计算软件组织，其 Fortran 数值库按双字母章节码组织并长期维护——此背景非出自本手册，可独立核实。）以下记载均属本手册 19.8.3.1 之转述，目录为第 10 版时点快照。

据本手册：NAG 图书馆是「用 FORTRAN 77, FORTRAN 90 等编程语言编写的函数与子函数／程序的数值方法的丰富集成」（「子函数／程序」疑为「子程序」之讹）。

## 内容概况（26 项）

编号疑为手册自拟概览，**非 NAG 官方章节码**（推断，见 [[findings/19-8-3三馆目录与语言清单转录校勘]]）。德文经校，原文照录与校记见 [[sources/10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc]]：

| # | 内容（德文，经校） | 中译 |
|---|---|---|
| 1 | Komplexe Arithmetik | 复算术 |
| 2 | Nullstellen von Polynomen | 多项式零点 |
| 3 | Wurzeln transzendenter Gleichungen | 超越方程求根 |
| 4 | Reihen | 级数 |
| 5 | Integration | 积分 |
| 6 | Gewöhnliche Differentialgleichungen | 常微分方程 |
| 7 | Partielle Differentialgleichungen | 偏微分方程 |
| 8 | Numerische Differentiation | 数值微分 |
| 9 | Integralgleichungen | 积分方程 |
| 10 | Interpolation | 插值 |
| 11 | Approxim. v. Daten d. Kurven und Flächen | 曲线与曲面数据之逼近 |
| 12 | Minima/Maxima einer Funktion | 函数极小／极大 |
| 13 | Matrixoperationen, Inversion | 矩阵运算、求逆 |
| 14 | Eigenwerte und Eigenvektoren | 特征值与特征向量 |
| 15 | Determinanten | 行列式 |
| 16 | Simultane lineare Gleichungen | 联立线性方程 |
| 17 | Orthogonalisierung | 正交化 |
| 18 | Lineare Algebra | 线性代数 |
| 19 | Einfache Berechnung von statist. Daten | 统计数据之简单计算 |
| 20 | Korrelation und Regressionsanalyse | 相关与回归分析 |
| 21 | Zufallszahlengeneratoren | 随机数生成器 |
| 22 | Nichtparametrische Statistik | 非参数统计 |
| 23 | Zeitreihenanalyse | 时间序列分析 |
| 24 | Operationsforschung | 运筹学 |
| 25 | Spezielle Funktionen | 特殊函数 |
| 26 | Mathem. und Maschinenkonstanten | 数学与机器常数 |

## 统计与金融数学软件（本手册对 NAG 之独有点名）

原文：「此外， NAG 图书馆还包含涉及统计和金融数学的大量软件」。此点名仅属 NAG，不见于 [[entities/IMSL图书馆]] 与 [[entities/Aachen图书馆]] 条目，是本手册区分三馆之关键之一。

## 覆盖特点

- 26 项概况覆盖复算术、级数、积分方程、正交化、运筹学等，为三馆中最广；
- 与第 19 章方法概念之对应（如 10↔插值、6↔常微分方程、7↔偏微分方程、17↔正交化、25↔特殊函数）见 [[sources/10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc]] 之映射表与 [[comparisons/NAG-IMSL与Aachen图书馆比较]]。

## 转写注记

原文第 7、8 项德文有 z/t 讹（Differentzal-、Differentzation），第 19 项衍句点，第 26 项含排版断词连字符；校勘见 [[findings/19-8-3三馆目录与语言清单转录校勘]]，全节讹误见 [[queries/19-8-3全节系统性转写讹误清单]]。