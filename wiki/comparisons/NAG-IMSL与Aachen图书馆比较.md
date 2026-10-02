---
type: comparison
title: "NAG、IMSL 与 Aachen 图书馆比较"
created: 2026-10-01
updated: 2026-10-01
tags: [数值程序库, NAG, IMSL, Aachen, 比较]
related: [10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc, NAG图书馆, IMSL图书馆, Aachen图书馆, 数值方法图书馆]
sources: ["数学手册(原书第10版)/19.8.3 数值方法图书馆.md"]
---
# NAG、IMSL 与 Aachen 图书馆比较

三馆同为 [[concepts/数值方法图书馆]] 之实例，且均由本手册 19.8.3 同一节（19.8.3.1–19.8.3.3）转述，可比性由同源转述保证。所有比较均以该节之内容概况目录为据：目录为第 10 版时点快照，编号疑为手册自拟概览而非官方章节码。

## 总对比

| 维度 | [[entities/NAG图书馆]] | [[entities/IMSL图书馆]] | [[entities/Aachen图书馆]] |
|---|---|---|---|
| 机构／来源 | Numerical Algorithms Group（数值算法组） | International Mathematical and Statistical Libraries（国际数学和统计图书馆） | [[entities/g-engeln-mullges]]（Fachhochschule Aachen）与 [[entities/f-reutter]]（RWTH Aachen）收集之方法 |
| 实现语言 | FORTRAN 77、FORTRAN 90 等 | FORTRAN 77、FORTRAN 90 | BASIC、QUICKBASIC、FORTRAN 77、FORTRAN 90、C、MODULA 2*、TURBO PASCAL* |
| 目录结构 | 单一概况 26 项 | 三部分：一般数学方法（12）＋统计问题（20）＋特殊函数（10） | 单一概况 10 项 |
| 统计内容 | 有（概况含统计类多项；另含统计与金融数学大量软件） | 最深：20 项专题 | 无 |
| 金融数学 | 有（本手册唯一点名） | 未见记载 | 无 |
| 特殊函数 | 概况 1 项（Spezielle Funktionen） | 独立成部分（10 项） | 无 |
| 定位 | 全面生产型 | 全面生产型、统计特深 | 教学型：特别适于研究数值数学的单个算法 |

（*MODULA 2 与 TURBO PASCAL 系自原文「MODULATURBO PASCAL」复原，见 [[queries/19-8-3全节系统性转写讹误清单]]。）

## 定位之别：生产型 vs 教学型

NAG 与 IMSL 面向实际计算之全面覆盖；Aachen 图书馆明言「特别适于研究数值数学的单个算法」，且其语言清单含 BASIC、QUICKBASIC、TURBO PASCAL、MODULA 2 等教学向语言，佐证其定位。此隐含之两类库之别为本节结构之深层对照。

## 覆盖面比较（以目录为据）

三份目录粒度不一（NAG 26 项概览、IMSL 分部列举、Aachen 10 项），下述「独有」仅为目录层面之表观差异，非严格功能对比：

- **共同覆盖**：线性方程组／矩阵运算与特征值（NAG 13–16、IMSL 数学 1–2/9、Aachen 2–4）、插值（NAG 10、IMSL 数学 3、Aachen 6）、逼近（NAG 11、IMSL 数学 3、Aachen 5）、积分（NAG 5、IMSL 数学 4、Aachen 8）、微分方程（NAG 6–7、IMSL 数学 5、Aachen 9–10）、极值／优化（NAG 12、IMSL 数学 8）、随机数生成器（NAG 21、IMSL 统计 18）、非参数统计（NAG 22、IMSL 统计 6）、概率分布（IMSL 数学 11/统计 17）、时间序列分析（NAG 23、IMSL 统计 8）。
- **NAG 概况独有**：复算术（1）、级数（4）、积分方程（9）、正交化（17）、运筹学（24）、行列式（15）；偏微分方程单列（7，IMSL 数学 5 未分常/偏，Aachen 无）。
- **IMSL 独有**：变换（Transformationen）单列；Weierstrass 函数两见（数学 10「Elliptische Funktionen, Funktionen von Weierstrass…」与特殊函数 9「Elliptische Integrale von Weierstrass…」）；统计专题群（方差分析、定类与离散数据分析、随机性检验、协方差与因子分析、判别分析、聚类分析、抽样调查、寿命与可靠性、多维标度、密度与风险函数估计、行式打印机图形等）。
- **Aachen 独有**：多项式样条明列（Polynomsplines，项 6）；有理插值明列；非线性方程组单列（项 3）；数值求积与求体积（Quadratur und Kubatur）单列（项 8）；常微分方程初值与边值问题分列（项 9、10）。

## 目录条目与第 19 章方法概念的映射

| 概念页 | NAG | IMSL | Aachen |
|---|---|---|---|
| [[concepts/多项式插值]]、[[concepts/三角插值]] | 10 Interpolation | 数学 3 | 6（含有理插值与 Polynomsplines） |
| [[concepts/三次插值样条]]、[[concepts/B样条（基样条）]] | 概况未单列 | 概况未单列 | 6（Polynomsplines） |
| [[concepts/平均逼近]]、[[concepts/切比雪夫逼近（一致逼近）]] | 11 | 数学 3 | 5 |
| [[concepts/常微分方程初值问题]] | 6 | 数学 5（未分初值/边值） | 9 |
| [[concepts/常微分方程边值问题]] | 6 | 数学 5（未分初值/边值） | 10 |
| [[concepts/差分法（偏微分方程）]]、[[concepts/有限元方法]] | 7 | 数学 5（未注明偏微分） | — |
| [[concepts/正交函数系与标准正交化]] | 17 Orthogonalisierung | — | — |
| [[concepts/切比雪夫多项式]]、[[concepts/拉盖尔多项式]]、[[concepts/埃尔米特多项式]] | 25 Spezielle Funktionen | 特殊函数部分（10 项） | — |

（「—」或「未单列」仅指目录概况层面，非功能缺失之断言。）

## 依据与限制

- 同源依据：[[sources/10-数学手册原书第10版--12-1983-数值方法图书馆--x50upc]] 之 19.8.3.1–19.8.3.3；
- IMSL 统计／特殊函数两表经复原，见 [[queries/IMSL统计问题与特殊函数目录交错之辨]]；
- 时效性：第 10 版时点快照，三馆现行内容必有出入；
- 编号非官方章节码，比较仅在手册概览层面成立。