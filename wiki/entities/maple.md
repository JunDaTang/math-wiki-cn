---
type: entity
title: Maple
created: 2026-10-02
updated: 2026-10-02
tags: [计算机代数系统, 数值计算, 数值软件]
related: [10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm, matlab, mathematica, evalf与evalhf, 龙格—库塔法（四阶）]
sources: ["数学手册(原书第10版)/19.8.4 交互程序系统和计算机代数系统的应用.md"]
---
# Maple

Maple 是一种计算机代数系统，能用内置逼近法求解许多数值数学问题；计算要求的节点数（整体精度）可由全局变量 Digits 的任意值规定（据本源 19.8.4.3）。（可独立验证的背景：Maple 最初由加拿大 Waterloo 大学的符号计算研究组开发，现由 Maplesoft 发行。）本源将其作为与 [[entities/matlab]]、[[entities/mathematica]] 同题对照的第三个系统（[[comparisons/Matlab-Mathematica-Maple同题数值比较]]）。

## 交互形式

启动后显示符号 Prompt，表示准备输入；输入与输出通常连在一行中，由箭头算子 → 分开。

## 精度控制

- Digits：规定计算精度的全局变量；选取比规定值大的值会导致计算速度降低。
- [[concepts/evalf与evalhf]]：evalf(expr, n)（式 19.293）以任意 n 位精度求值，默认由 Digits 确定；evalhf 用硬件双精度加速但损失精度。

## 方程的数值解

fsolve(eqn, var, option)（式 19.294）：确定实数解；若 eqn 是多项式形式，则结果都是（全部）实根；若不是多项式形式，则很可能仅返回一个解。选项见表 19.8：complex（确定一个复根，或多项式的所有根）、maxsols=n（至少 n 个根，仅对多项式方程）、fulldigits（保证不减少计算中用到的位数）、intervall（在给定区间内求根；源文拼写）。算例复算见 [[findings/跨系统求根复算]]。

## 数值积分

evalf(int(f(x), x=a..b), n)（式 19.295）：Maple 通过使用（预置）逼近公式计算定积分——当被积函数太复杂或原函数不能表示成基本函数时正是这种情况。某些情况下（尤其积分区间太大）该方法失效，可 readlib('evalf/int') 载入库中另一逼近程序，以 'evalf/int'(f, x=a..b, 精度, _NCrule) 调用；第三个参数规定精度，最后一个规定逼近法的内部记号。正文称之为「自适应牛顿法」，与 _NCrule（Newton–Cotes）存在张力（[[queries/自适应牛顿法疑为牛顿柯特斯法之辨]]）。算例复算见 [[findings/Maple积分与dsolve算例复算]]。

## 微分方程的数值解

dsolve(deqn, var, numeric)（式 19.296）：选项 numeric 作为第三参量，deqn 含实际的微分方程和初值条件；运算结果是一个程序，记为 r 时用命令 r(t) 得到独立变量在 t 处的解函数值。Maple 应用龙格—库塔法得到该结果（回指 19.4.1.2，参见 [[concepts/龙格—库塔法（四阶）]]）；相对误差和绝对误差的默认精度为 10^(−Digits+3)，用户可通过整体符号 _RELERR 与 _ABSERR 修改默认容许误差。y′=¼(x²+y²)、y(0)=0 算例的复算见 [[findings/Maple积分与dsolve算例复算]]。