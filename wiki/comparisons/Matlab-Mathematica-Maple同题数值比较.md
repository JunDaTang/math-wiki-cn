---
type: comparison
title: Matlab、Mathematica、Maple 同题数值比较
created: 2026-10-02
updated: 2026-10-02
tags: [比较, Matlab, Mathematica, Maple, 数值计算]
related: [10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm, matlab, mathematica, maple, 交互程序系统与计算机代数系统, 跨系统求根复算]
sources: ["数学手册(原书第10版)/19.8.4 交互程序系统和计算机代数系统的应用.md"]
---
# Matlab、Mathematica、Maple 同题数值比较

手册在 Matlab 小节明言「在后面 Mathematica、Maple 的数值应用中，将同样讨论这些问题」，三小节因此构成一组同题跨系统对照。以下按五个同题问题整理（数值复算状态见各发现页）。

## 同题 1：10 点数据集

数据：{1.70045, 1.2523, 0.638803, 0.423479, 0.249091, 0.160321, 0.0883432, 0.0570776, 0.0302744, 0.0212794}（横坐标对应 1..10）。

- Matlab：plot 图形表示；三次插值样条与四阶最佳逼近多项式（图 19.19(a)），由 interp1/polyfit 实现；
- Mathematica：Fit[l, {1,x,x²,x³,x⁴}, x] 四次最小二乘多项式（图 19.21(a)）；Interpolation[l]（图 19.21(b)）。

差异：Matlab 小节样条与最佳逼近两法并用；Mathematica 小节中 Fit 为离散最小二乘（[[concepts/平均逼近]]）、Interpolation 为插值——插值精确过数据点，拟合不然（f1(1)≈1.7319≠1.70045，见 [[findings/Mathematica-Fit系数与e的1减0点5x级数之说不符]]）。

## 同题 2：x⁶ + 3x² − 5 = 0

| 系统 | 命令 | 输出 |
|---|---|---|
| Matlab | roots(p)（伴随矩阵特征值） | 六根：±1.0743、±0.8673±1.1529i |
| Mathematica | NSolve（可指定精度 n） | 六根：±1.07432、±0.867262±1.15292I |
| Maple | fsolve(eq, x)；fsolve(eq, x, complex) | 默认仅两实根 ±1.074323739；complex 给全部根 |

三系统一致且经复算证实（[[findings/跨系统求根复算]]）。

## 同题 3：e^(−x³) − 4x² = 0

| 系统 | 命令 | 输出 |
|---|---|---|
| Matlab | fzero（三个初值） | 0.4741、−0.5413、−1.2085（每次一解、依赖初值） |
| Maple | fsolve(eq, x)；fsolve(eq, x, x=−2..0) | 0.4740623572、−0.5412548544（非多项式常只返回一个解） |

两系统结果一致（[[findings/跨系统求根复算]]）。

## 同题 4：∫ e^(−x²) dx（大区间/无穷区间）

| 系统 | 命令 | 结果 |
|---|---|---|
| Matlab | quad / quadl on [−1000,1000]，容差 10⁻¹⁰ | 1.77245385094233（585 次）/ 1.77245385090571（768 次） |
| Mathematica | NIntegrate on (−∞,∞) | 1.77245 |
| Mathematica | NIntegrate on [−1000,1000]，默认选项 | 1.34946·10⁻²⁶（**错**，峰值丢失） |
| Mathematica | 同上 + MinRecursion→3、MaxRecursion→10 | 1.77245 |
| Maple | evalf(int(…))；readlib('evalf/int') 后 _NCrule | 前者报错；后者 1.772453851（10 位） |

基准 √π = 1.772453850905516；三系统经正确选项后一致（[[findings/quad与quadl求值次数复算]]、[[findings/NIntegrate峰值丢失与递归选项复算]]、[[findings/Maple积分与dsolve算例复算]]）。CAS 端的失败案例正是 [[concepts/交互程序系统与计算机代数系统]] 告诫的证据。

## 同题 5：y′ = ¼(x²+y²)、y(0) = 0

- Matlab：ode45 于 [0,1]（图 19.20(a)）；
- Maple：dsolve(…, numeric)，r(0.5) 给 y(x)(.5) = 0.01041860472（级数复算证实）；
- Mathematica 小节未讨论此题（其 NDSolve 算例为摩擦运动与傅科摆）。

此题回指 19.4.1.2，与 [[findings/式19-99四阶龙格—库塔格式与算例复算]] 同题。

## 机制对照总表

| 问题类型 | Matlab | Mathematica | Maple |
|---|---|---|---|
| 线性方程组 | `\`（[[concepts/反斜杠算符]]，自动分派） | —（本源未讨论） | —（本源未讨论） |
| 多项式根 | roots（伴随矩阵特征值） | NSolve | fsolve（complex） |
| 超越方程 | fzero（初值依赖） | — | fsolve（区间/选项） |
| 拟合/插值 | interp1/polyfit/interp2/griddata | Fit / Interpolation | — |
| 数值积分 | quad / quadl | NIntegrate（递归选项、奇点列出） | evalf(int(…))、'evalf/int' |
| ODE 数值解 | ode45 / ode113 / 刚性程序 | NDSolve（InterpolatingFunction） | dsolve(…, numeric) |
| 精度控制 | IEEE 双精度、容差参数 | AccuracyGoal/PrecisionGoal/WorkingPrecision | Digits、evalf(expr,n) |