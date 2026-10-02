---
type: entity
title: IMSL 图书馆
created: 2026-10-01
updated: 2026-10-01
tags: [数值程序库, IMSL, FORTRAN, 统计软件, 特殊函数]
related: [10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc, NAG图书馆, Aachen图书馆, 数值方法图书馆, 19-8-3三馆目录与语言清单转录校勘, IMSL统计问题与特殊函数目录交错之辨]
sources: ["数学手册(原书第10版)/19.8.3 数值方法图书馆.md"]
---
# IMSL 图书馆

IMSL 图书馆（国际数学和统计图书馆，International Mathematical and Statistical Libraries）是商业性数值与统计程序库，供科学与统计计算调用。（独立可查之公共背景：IMSL 之 Fortran 库历史上分为 MATH/LIBRARY（数学）、STAT/LIBRARY（统计）与 SFUN/LIBRARY（特殊函数）三部分——此背景非出自本手册，可独立核实，且与下述「三部分」结构相合。）以下记载均属本手册 19.8.3.2 之转述，目录为第 10 版时点快照。

据本手册：IMSL 图书馆「同时包含三部分：一般数学方法、统计问题、特殊函数」；子图书馆（原文如此）包含用 FORTRAN 77、FORTRAN 90 编写的函数和子程序。编号疑为手册自拟概览，非 IMSL 官方章节码。

## 一般数学方法（12 项，德文经校）

| # | 内容（德文，经校） | 中译 |
|---|---|---|
| 1 | Lineare Systeme | 线性方程组 |
| 2 | Eigenwerte | 特征值 |
| 3 | Interpolation und Approximation | 插值与逼近 |
| 4 | Integration und Differentiation | 积分与微分 |
| 5 | Differentialgleichungen | 微分方程 |
| 6 | Transformationen | 变换 |
| 7 | Nichtlineare Gleichungen | 非线性方程 |
| 8 | Optimierung | 最优化 |
| 9 | Vektor- und Matrixoperationen | 向量与矩阵运算 |
| 10 | Elliptische Funktionen, Funktionen von Weierstrass und verwandte Funktionen | 椭圆函数、Weierstrass 函数及相关函数 |
| 11 | Wahrscheinlichkeitsverteilungen | 概率分布 |
| 12 | Verschiedene Funktionen | 杂项函数 |

（原文 4 作 Differentzation、5 作 Differentzalgleichungen、10 作 Ellipische，校记见 [[findings/19-8-3三馆目录与语言清单转录校勘]]。）

## 统计问题（20 项，经复原）

本表自交错转写**复原**：转写中本表 11–18 与特殊函数 1–5 交错错位，复原依据（编号自洽＋主题自洽）见 [[queries/IMSL统计问题与特殊函数目录交错之辨]] 与 [[findings/19-8-3三馆目录与语言清单转录校勘]]：

| # | 内容（德文，经校） | 中译 |
|---|---|---|
| 1 | Grundlegende Kennzahlen | 基本统计量 |
| 2 | Regression | 回归 |
| 3 | Korrelation | 相关 |
| 4 | Varianzanalyse | 方差分析 |
| 5 | Kategoriale und diskrete Datenanalyse | 定类与离散数据分析 |
| 6 | Nichtparametrische Statistik | 非参数统计 |
| 7 | Anpassungstests und Test auf Zufälligkeit | 拟合检验与随机性检验 |
| 8 | Zeitreihenanalyse und Vorhersage | 时间序列分析与预测 |
| 9 | Kovarianz- und Faktoranalyse | 协方差与因子分析 |
| 10 | Diskriminanz-Analyse | 判别分析 |
| 11 | Cluster-Analyse | 聚类分析 |
| 12 | Stichprobenerhebung | 抽样调查 |
| 13 | Lebensdauerverteilungen und Zuverlässigkeit | 寿命分布与可靠性 |
| 14 | Mehrdimensionale Skalierung | 多维标度 |
| 15 | Schätzung der Dichte- und Hasard- bzw. Risikofunktion | 密度函数与风险函数之估计 |
| 16 | Zeilendrucker-Grafik | 行式打印机图形 |
| 17 | Wahrscheinlichkeitsverteilungen | 概率分布 |
| 18 | Zufallszahlen-Generatoren | 随机数生成器 |
| 19 | Hilfsalgorithmen | 辅助算法 |
| 20 | Mathematische Hilfsmittel | 数学工具 |

## 特殊函数（10 项，经复原）

| # | 内容（德文，经校） | 中译 |
|---|---|---|
| 1 | Elementare Funktionen | 初等函数 |
| 2 | Trigonometrische und hyperbolische Funktionen | 三角与双曲函数 |
| 3 | Exponentialfunktion und verwandte | 指数函数及相关 |
| 4 | Gamma-Funktionen und verwandte | Gamma 函数及相关 |
| 5 | Fehler-Funktionen und verwandte | 误差函数及相关 |
| 6 | Bessel-Funktionen | Bessel 函数 |
| 7 | Kelvin-Funktionen | Kelvin 函数 |
| 8 | Bessel-Funktionen gebrochener Ordnung | 分数阶 Bessel 函数 |
| 9 | Elliptische Integrale von Weierstrass und verwandte Funktionen | Weierstrass 椭圆积分及相关函数 |
| 10 | Verschiedene Funktionen | 杂项函数 |

（原文「Gamma —Funktionen」等之破折号疑为连字符之转写衍入，复原为连字符；统计 7 之 Anpassungtests 疑脱连接 s。）

## 特点

- 统计部分 20 项为三馆最深：聚类分析、判别分析、多维标度、寿命分布与可靠性、密度与风险函数估计、行式打印机图形等统计专题皆独详于本馆概况；
- 特殊函数独立成部分，且 Weierstrass 函数两见（数学 10 与特殊函数 9）；
- 本手册未言及 IMSL 含金融数学软件——该点名仅属 [[entities/NAG图书馆]]。

## 转写注记

统计与特殊函数两表在原转写中交错错位（双栏排版被拉平），须对照原书复核；德文讹字（Ellipische、Zuf lligkeit、Grapfik、Schatzung、Zuverl ssigkt. 等）见 [[findings/19-8-3三馆目录与语言清单转录校勘]] 与 [[queries/19-8-3全节系统性转写讹误清单]]。