---
type: entity
title: Aachen 图书馆
created: 2026-10-01
updated: 2026-10-01
tags: [数值程序库, Aachen, 教学软件, BASIC, FORTRAN, 数值分析]
related: [10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc, NAG图书馆, IMSL图书馆, 数值方法图书馆, g-engeln-mullges, f-reutter, 19-8-3三馆目录与语言清单转录校勘]
sources: ["数学手册(原书第10版)/19.8.3 数值方法图书馆.md"]
---
# Aachen 图书馆

Aachen 图书馆是一部以 [[entities/g-engeln-mullges]]（Fachhochschule Aachen）与 [[entities/f-reutter]]（Rheinisch-Westfälische Technische Hochschule Aachen）收集的数值方法公式为基础的数值方法程序库；据本手册 19.8.3.3，其程序**特别适于研究数值数学的单个算法**，即教学与算法研究定位，与 [[entities/NAG图书馆]]、[[entities/IMSL图书馆]] 之全面生产型覆盖形成对照。以下记载均属该小节转述，目录为第 10 版时点快照。

## 方法来源与实现语言

以两位学者收集的数值方法公式为基础，使用 BASIC、QUICKBASIC、FORTRAN 77、FORTRAN 90、C、MODULA 2、TURBO PASCAL 等程序语言——末两项（MODULA 2、TURBO PASCAL）由原文「MODULATURBO PASCAL」复原（疑为两项之讹合），见 [[queries/19-8-3全节系统性转写讹误清单]]。语言清单含 BASIC、QUICKBASIC、TURBO PASCAL、MODULA 2 等教学向语言，与其定位相合。

## 内容概况（10 项，德文经校）

| # | 内容（德文，经校） | 中译 |
|---|---|---|
| 1 | Numerische Verfahren zur Lösung nichtlinearer und speziell algebraischer Gleichungen | 非线性方程及代数方程之数值解法 |
| 2 | Direkte und iterative Verfahren zur Lösung linearer Gleichungssysteme | 线性方程组之直接与迭代解法 |
| 3 | Systeme nichtlinearer Gleichungen | 非线性方程组 |
| 4 | Eigenwerte und Eigenvektoren von Matrizen | 矩阵特征值与特征向量 |
| 5 | Lineare und nichtlineare Approximation | 线性与非线性逼近 |
| 6 | Polynomiale und rationale Interpolation sowie Polynomsplines | 多项式与有理插值及多项式样条 |
| 7 | Numerische Differentiation | 数值微分 |
| 8 | Numerische Quadratur und Kubatur | 数值求积与求体积 |
| 9 | Anfangswertprobleme bei gewöhnlichen Differentialgleichungen | 常微分方程初值问题 |
| 10 | Randwertprobleme bei gewöhnlichen Differentialgleichungen | 常微分方程边值问题 |

（原文 1、2 作 Losung，1 作 G leichungen，7 作 N umerische，9、10 作 gewohnlichen；校记见 [[findings/19-8-3三馆目录与语言清单转录校勘]]。）

## 覆盖特点

集中于数值代数（非线性方程与方程组、线性方程组、特征值）、逼近与插值（含多项式样条）、数值微分、求积与求体积、常微分方程初值与边值问题。概况中不含统计与特殊函数部分（对照 [[entities/IMSL图书馆]]），亦无金融数学之记载（该点名仅属 [[entities/NAG图书馆]]）。

与第 19 章方法概念之对应：条目 6 ↔ [[concepts/多项式插值]]、[[concepts/三次插值样条]]、[[concepts/B样条（基样条）]]；条目 5 ↔ [[concepts/平均逼近]]、[[concepts/切比雪夫逼近（一致逼近）]]；条目 9–10 ↔ [[concepts/常微分方程初值问题]]、[[concepts/常微分方程边值问题]]。

## 开放问题

本馆对应之 Engeln-Müllges/Reutter 出版物（德文数值数学教材及其配套程序集）待识别，以坐实其身份与年代。