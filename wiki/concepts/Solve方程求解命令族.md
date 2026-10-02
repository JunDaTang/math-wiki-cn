---
type: concept
title: Solve 方程求解命令族（Solve、NSolve、FindRoot 与方程组运算）
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 方程求解, Solve, NSolve, FindRoot]
related: [mathematica, Equal恒等判定与方程表示, 线性方程组求解命令]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---
# Solve 方程求解命令族（Solve、NSolve、FindRoot 与方程组运算）

Mathematica 解方程与方程组的命令族。源文纲领：如果一个方程能够明确地在代数数域中求解，那么解将借助根式来表示；如果它不能给出封闭形式的解，那么至少可以找到具有给定精度的数值解。方程在 Mathematica 中被看作逻辑表达式（见 [[concepts/Equal恒等判定与方程表示]]）；Solve 在某种意义上相继进行了 Roots 与 ToRules 运算。

## 多项式方程与四次界限

- Mathematica 以符号形式解**直到四次**的多项式方程，因为对这些方程可以给出具有代数表达式形式的解。
- 较高次的代数方程若能通过代数变换（比如因式分解）变为比较简单的形式，Mathematica 仍提供符号解；在这些情形中，Solve 尝试运用内置运算 Expand、Decompose。源例：六次方程 x⁶−6x⁵+6x⁴−4x³+65x²−38x−120 = 0 被内部工具成功分解因式，六根 {−1, −1−2I, −1+2I, 2, 3, 4}「毫无困难地解决」——此即「直到四次」断言的明示限定。
- 一般三次方程的符号解与 Cardano 公式吻合；因项的长度，解列表仅明确显示第一项。源文建议：如果要解具有给定系数 a、b、c 的一个方程，最好用命令 Solve 处理该方程本身，而不是将 a、b、c 代入解公式。
- 数值解用 NSolve（源例：六次方程之六数值根）。

## 超越方程与 FindRoot

超越方程一般来说不可能有符号形式的解，且常常具有无穷多的解；在这些情形中，应该给出 Mathematica 必须在其中求解的区域的一个估计——这用 FindRoot[g, {x, xs}] 做到，其中 xs 是用来寻找根的初始值。源例 x + ArcCoth[x] − 4 = 0：初值 1.1 得根 1.00502，初值 5 得根 3.72478（多根须换初值）。

## 方程组运算（表 20.11）

```text
Solve[{l1 == r1, l2 == r2, ...}, vars]    关于 vars 解给定的方程组
Eliminate[{l1 == r1, ...}, vars]          从方程组消去 vars
Reduce[{l1 == r1, ...}, vars]             化解方程组并给出可能的解
FindInstance[expr, vars]                  找出一个使 expr 为真的 vars 的例证
```

这些运算提供的是符号解而非数值解；与一个未知数的情形类似，命令 NSolve 将给出数值解。线性方程组另见 [[concepts/线性方程组求解命令]]（源称其解在第 1351 页 20.3.3 中讨论）。

## 关联

三命令之别见 [[comparisons/Solve与NSolve与FindRoot比较]]；算例复算（含三次方程第三根讹残之辨）见 [[findings/20-3-2方程求解算例复算]]。