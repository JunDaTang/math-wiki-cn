---
type: entity
title: Mathematica
created: 2026-10-02
updated: 2026-10-02
tags: ["计算机代数系统", "数值计算", "数值软件", "Mathematica", "符号计算", "数学软件", "Wolfram-Research", "第20章", "软件工具", "计算机代数", "wolfram", "绘图", "数学手册第20章"]
related: ["10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm", "matlab", "maple", "交互程序系统与计算机代数系统", "平均逼近", "残量平方和", "计算机代数系统", "Mathematica输入输出行记法", "公式操作", "数值计算（计算机代数应用领域）", "式20-1至20-3c符号与数值求解算例转录复算", "与第10版兼容的各版本所指之辨", "符号解浮点代入的相消风险", "wolfram-research", "20-2未入库回指缺口", "wolfram-research沃尔夫勒姆研究公司", "表达式（Mathematica）", "Mathematica数的四种基本类型", "Mathematica列表与向量矩阵表示", "Mathematica矩阵与向量运算", "entities/wolfram-research沃尔夫勒姆研究公司", "entities/maple", "entities/matlab", "concepts/计算机代数系统", "concepts/交互程序系统与计算机代数系统", "concepts/表达式（Mathematica）", "concepts/Mathematica数的四种基本类型", "concepts/Mathematica标准函数", "concepts/Mathematica特殊函数", "concepts/纯函数（Mathematica）", "concepts/Mathematica完全形式与中置算子", "concepts/Mathematica输入输出行记法", "queries/与第10版兼容的各版本所指之辨", "图形基元（Mathematica）", "图形命令与相对绝对尺寸", "图形选项（Mathematica）", "Graphics与Show图形对象", "Plot函数绘图与内部函数表", "ParametricPlot参数曲线绘图", "Plot3D与ParametricPlot3D三维绘图", "数学手册原书第10版", "10-数学手册原书第10版--26-第20章-计算机代数系统以mathematica为例--1wwef1k", "第20章未入库回指缺口", "10-数学手册原书第10版--2-目录--1srm7m", "第20章Mathematica专章未入库之辨"]
sources: ["数学手册(原书第10版)/19.8.4 交互程序系统和计算机代数系统的应用.md", "数学手册(原书第10版)/20.1 引言.md", "数学手册(原书第10版)/20.2 Mathematica的重要结构要素.md", "数学手册(原书第10版)/20.2.5 作为列表的向量和矩阵.md", "数学手册(原书第10版)/20.2.6 函数.md", "数学手册(原书第10版)/20.3 Mathematica的重要应用.md", "数学手册(原书第10版)/20.4 用Mathematica绘图.md", "数学手册(原书第10版)/第20章 计算机代数系统——以Mathematica为例.md", "数学手册(原书第10版)/目录.md"]
---

# Mathematica

Mathematica 是一款计算机代数系统（CAS），即以符号计算——对数学表达式的精确解析运算——为核心的数学软件系统，兼具符号计算、任意精度数值计算、图形可视化与程序设计能力。其开发商为 [[wolfram-research沃尔夫勒姆研究公司|Wolfram Research]]（开发商与产品身份为可独立核实的公开背景，非本维基已入库来源所载；本维基中另见该组织页）。

在本维基语料《数学手册（原书第10版）》（[[数学手册原书第10版]]）中，Mathematica 是第 20 章「计算机代数系统——以Mathematica为例」（第 1327–1366 页，据总目录）整章的讲解对象，也是第 19.8.4 节三系统比较的主题系统之一。据总目录，第 20 章是全书唯一以单一具名软件为主题的章节。

## 在本维基语料中的角色

- **第 20 章示例系统**：Mathematica 是第20章「计算机代数系统——以Mathematica为例」所采用的示例系统，手册第 20 章以其为专门对象分节介绍（20.1–20.4，结构与页码见下文目录所载）。
- **第 19.8.4 节三系统比较**：该节将其与 [[maple]]、[[matlab]] 并列同题比较（算例见下文）。
- **代表性 CAS 之一**：第 19–20 章将其与 Maple 并列为代表性计算机代数系统（见 [[计算机代数系统]]、[[交互程序系统与计算机代数系统]]）。

### 总目录所载的第20章结构

据总目录（[[10-数学手册原书第10版--2-目录--1srm7m]]），第 20 章以 Mathematica 为计算机代数系统的代表性实例，分四部分展开：

| 部分 | 标题 | 页码 | 覆盖内容 |
|---|---|---|---|
| 20.1 | 引言 | 1327–1328 | 对计算机代数系统的简要描述 |
| 20.2 | Mathematica 的重要结构要素 | 1329–1344 | 基本结构要素；数的类型；重要算子；列表；作为列表的向量和矩阵；函数；模式；函数运算；程序设计；句法、信息、消息 |
| 20.3 | Mathematica 的重要应用 | 1345–1356 | 代数表达式的操作；方程和方程组的解；线性方程组与本征值问题；微积分 |
| 20.4 | 用 Mathematica 绘图 | 1357–1366 | 基本图形元素；图形基元；图形选项；图形表示的句法；二维曲线；参数形式曲线；曲面和空间曲线 |

小节级页码的完整原文照录见 [[10-数学手册原书第10版--2-目录--1srm7m]]。

### 第20章目录页所载

依据 [[10-数学手册原书第10版--26-第20章-计算机代数系统以mathematica为例--1wwef1k]]（章节目录页）：

- Mathematica 出现于第20章章标题，并复现于 20.2「Mathematica的重要结构要素」、20.3「Mathematica的重要应用」、20.4「用Mathematica绘图」三个小节标题中。
- 由此可知手册第20章计划从**结构要素**、**应用**、**绘图**三个方面展开对 Mathematica 的介绍；但该目录页不含任何实质内容，上述规划仅为标题层面的信息。
- 就该目录页所载，Mathematica 是该章唯一被点名的示例系统（20.1 引言是否还提及其他系统，待小节正文核对，见 [[第20章未入库回指缺口]]）。

### 与手册其他部分的衔接

- 第 19 章 19.8.4「交互程序系统和计算机代数系统的应用」（第 1312 页，见 [[10-数学手册原书第10版--9-第19章-数值分析--1su8bnd]]）在数值分析语境下引入计算机代数系统的应用，与第 20 章直接衔接。
- 第 21 章「表格」为独立的数值表汇编，与本章主题无直接依赖关系。

### 断言边界与覆盖缺口

> **断言边界（重要）**：仅据目录页（总目录与第20章目录页，所载均为章节结构、页码与小节要点，不含正文实质内容），不得对 Mathematica 作以下任何断言；此类内容须以 20.1–20.4 各小节正文为据：
>
> - 版本信息或所述版本对应的历史年代；
> - 功能范围、语法细节或能力评价；
> - 与其他计算机代数系统的比较。

截至 2026-10-02，本页以下各节依已入库的小节页（19.8.4、20.1、20.2、20.2.5、20.2.6、20.3、20.4）及两个目录页（总目录、第20章目录页）整理，覆盖目录所规划的四个方面——20.1 引言（手册对 CAS 与 Mathematica 的定位性论述）、20.2 重要结构要素（以原文所述为准）、20.3 重要应用、20.4 用 Mathematica 绘图——以及第 19.8.4 节的同题比较算例；目录页本身所载仅为章节结构与页码层面的信息。尚未入库小节的回指缺口见 [[20-2未入库回指缺口]]、[[第20章未入库回指缺口]]；专章正文的入库状态辨析见 [[第20章Mathematica专章未入库之辨]]。

## 19.8.4 三系统同题比较中的数值算例

在交互程序系统与计算机代数系统（CAS）应用的同题比较中，Mathematica 与 [[matlab|Matlab]]、[[maple|Maple]] 并列举例（[[Matlab-Mathematica-Maple同题数值比较]]、[[跨系统求根复算]]）。比较覆盖的算例包括：

- **跨系统求根**（[[跨系统求根复算]]）。
- **数值积分**：NIntegrate 展示了自适应求积中峰值丢失与递归选项的作用（[[NIntegrate峰值丢失与递归选项复算]]）。
- **微分方程求解**（[[Maple积分与dsolve算例复算]]）。
- **Fit 拟合**：拟合系数与 e^(1−0.5x) 级数前四项之说不符（[[Mathematica-Fit系数与e的1减0点5x级数之说不符]]）。

## 20.1 引言：符号与数值两条腿

20.1 将 Mathematica 定位为兼具精确符号求解与数值求解的系统，以式 20.1–20.3c 的符号求解与数值求解示例给出符号/数值两条腿的纲领（源页见 [[10-数学手册原书第10版--6-201-引言--4divnh]]）。

## 20.2 结构与语言要素

20.2（重要结构要素，20.2.1–20.2.8）系统介绍其结构要素：表达式与 [[FullForm（完整形式）]]、[[列表（Mathematica）]]、[[模式（Mathematica）]]、纯函数与函数运算、程序设计（见 [[10-数学手册原书第10版--22-202-mathematica的重要结构要素--1w5xyrj]] 及各小节源页）；输入输出的行记法 In[n]/Out[n] 见 [[Mathematica输入输出行记法]]。要点：

- **万物皆表达式**：完全形式、头与 Part、符号命名规则（[[表达式（Mathematica）]]、[[FullForm（完整形式）]]、[[Part（部件提取与头）]]、[[Mathematica符号命名规则]]）。
- **数类型**：Integer、Rational、Real、Complex；精确数与浮点数、N 与精度（[[Mathematica数的四种基本类型]]）。
- **算子**：Set/SetDelayed、Rule/RuleDelayed、Equal、替换算子 /.（[[Set指派与清除]]、[[Rule变换规则与替换算子]]、[[Equal恒等判定与方程表示]]）。
- **列表与矩阵**：Table/Range/Array 生成；Transpose、Inverse、Det、点积；依分量运算与矩阵运算之别（[[列表（Mathematica）]]、[[Mathematica矩阵与向量运算]]）。
- **函数与模式**：标准函数与特殊函数（表 20-7、20-8）、纯函数、模式定义（[[纯函数（Mathematica）]]、[[模式（Mathematica）]]）。
- **函数运算**：Derivative、Nest/NestList/FoldList/FixedPoint、Apply/Map、InverseFunction/InverseSeries（反函数与级数反演）（[[Mathematica函数运算与纯函数]]）。

## 20.3 六大应用域

20.3（重要应用）给出六大应用域的命令与算例证据：

1. **代数表达式操作**：表 20.9–20.10 命令集（Expand/Factor/Collect/Together/Apart/Cancel 与 PolynomialGCD/LCM/Quotient/Remainder/MonomialList）；整数环、有理数域、高斯整数环（GaussianIntegers 选项）上的因式分解（[[代数表达式与多项式操作命令]]、[[高斯整数上的因式分解]]）。
2. **方程求解**：Solve（符号，语义上相继执行 Roots、ToRules）、NSolve（数值）、FindRoot（超越方程须初值）、Eliminate/Reduce/FindInstance（方程组）（[[Solve方程求解命令族]]）。
3. **线性方程组**：Array/Thread 建模；n=m 且 det P≠0 时 X = Inverse[P].B，LinearSolve 更快；NullSpace、RowReduce 覆盖一切情形（[[线性方程组求解命令]]）。
4. **本征值问题**：Eigenvalues/Eigenvectors/Eigensystem；n>4 无代数表达式，Root 对象或 N[m] 数值（[[本征值命令与Root对象]]）。
5. **微积分**：D/Dt 求导、Integrate 不定/定/重积分、Boole 区域积分（[[D与Dt微分命令]]、[[Integrate积分命令]]）。
6. **微分方程**：DSolve 纯函数形式通解、ProductLog 隐式解（[[DSolve微分方程求解命令]]、[[ProductLog与LambertW函数]]）。

## 能力边界（Mathematica 特定，勿外推至 Maple/Matlab）

- 符号解多项式方程至四次；可分解之高次方程例外（Solve 尝试内置运算 Expand、Decompose）。
- n>4 矩阵本征值无代数表达式（特征多项式次数大于四），符号结果为 Root 对象、须 N[m] 数值。
- 非初等不定积分（∫x^x dx）原样返回；认识某些非初等积分定义的特殊函数（椭圆函数等）。
- 超越方程符号解一般不可得，FindRoot 需初值。
- DSolve 失败时原样返回、回退数值解；源文告诫「能力不应被高估」。
- 版本时代断言（源内不可检验）：合理时间内可处理约 5000 个左右未知数的线性方程组；甚至复杂多维区域的某些偏微分方程亦可符号/数值求解。
- Notebook 单元左角「+」号可选自由格式输入或 Wolfram-Alpha 查询（借以查看积分细节）。

## 20.4 绘图专长

手册断言「绘图是 Mathematica 的一项专长」，并以可复算算例给出其绘图体系：

- 图形由内置基元组装为 `Graphics[list]` 对象，经 `Show` 显示（[[Graphics与Show图形对象]]、[[图形基元（Mathematica）]]）。
- 图形命令（指示）作用域限于所在花括号内（[[图形命令与相对绝对尺寸]]）。
- 缺省 `AspectRatio` 为 1:GoldenRatio（1:0.618），会使圆变形为椭圆；`Automatic` 保形；`InputForm[%]` 证实默认为 `AspectRatio->GoldenRatio^(-1)`（[[图形选项（Mathematica）]]、[[InputForm图形对象内部结构转录校勘]]）。
- `Plot` 内部生成函数表再以 `Line` 基元连线（[[Plot函数绘图与内部函数表]]）；命令族覆盖 ParametricPlot、Plot3D、ParametricPlot3D（[[ParametricPlot参数曲线绘图]]、[[Plot3D与ParametricPlot3D三维绘图]]）。
- 三维选项 ViewPoint 默认 `{1.3, -2.4, 2}`；可轻易生成洛伦茨吸引子的图像（[[洛伦茨方程组]]）。

## 第10版末段增补的现代功能（无算例支撑，仅记录）

- 轻松构建 GUI，利用交互功能。
- 大部分计算自动并行，并提供 Parallelize、ParallelMap 供用户自建并行程序。
- CUDALink、OpenCLFunctionLoad 可在高层编程设计极快图形卡。
- 动态交互性工具 Manipulate 可展示曲线族的参数依赖性。
- 云端工作。
- 树蓝派计算机（Raspberry Pi）已获 Mathematica 免费使用许可（译名存疑见 [[树蓝派疑为树莓派之辨]]）。

## 版本基线张力

第10版 20.4 节同时出现 pre-v6 遗留命令/选项（`GraphicsArray`、`HiddenSurface`、`Shading`）与 v6+/v10+ 特征（`GraphicsRow`、InputForm 输出的 `Directive[Opacity[1.], RGBColor[0.368417, 0.506779, 0.709798], AbsoluteThickness[1.6]]` 默认样式），反映旧稿局部增补而未统一版本基线，详见 [[GraphicsArray与GraphicsRow比较]]。相关转写讹误总目见 [[20-4全节系统性转写讹误清单]]。

## 关联

- 主题学科：[[计算机代数系统]]
- 所属手册章节：[[数学手册原书第10版]] 第20章
- 相关页面：[[wolfram-research沃尔夫勒姆研究公司]]、[[计算机代数系统]]、[[交互程序系统与计算机代数系统]]、[[Mathematica输入输出行记法]]、[[Matlab-Mathematica-Maple同题数值比较]]、[[10-数学手册原书第10版--2-目录--1srm7m]]、[[第20章Mathematica专章未入库之辨]]