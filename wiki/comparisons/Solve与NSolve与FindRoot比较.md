---
type: comparison
title: "Solve 与 NSolve 与 FindRoot 比较"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 求根, 比较, 符号-数值阶梯]
related: [Solve方程求解命令族, Equal恒等判定与方程表示, Rule变换规则与替换算子, 跨系统求根复算]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---

# Solve 与 NSolve 与 FindRoot 比较

本比较依据《数学手册（原书第10版）》20.3.2（本页 frontmatter `sources` 所列源文件）；三者构成「符号优先、数值回退」的阶梯，呼应 [[concepts/公式操作]] 与 [[concepts/数值计算（计算机代数应用领域）]] 的分工。

## 对照表

| 维度 | Solve | NSolve | FindRoot |
|---|---|---|---|
| 解的类型 | 符号解（代数表达式） | 数值解 | 数值解 |
| 适用方程 | 多项式方程与方程组（表 20.11）；方程组运算提供符号解而非数值解 | 多项式方程（例：六次方程全部六根） | 超越方程等一般方程 |
| 输入要求 | 方程（逻辑表达式）与变元 | 同左 | 需初始值：FindRoot[g, {x, xs}]，xs 为寻根初值 |
| 能力边界 | 四次以下给符号解；较高次若能经代数变换（如因式分解）化为较简单形式亦给符号解，内部尝试 Expand 与 Decompose | — | 初值选择决定收敛到不同根；超越方程常有无穷多解，应给出求解区域的一个估计 |
| 典型算例 | 例 A：x³+6x+2=0 三根（首根经 Cardano 公式复算吻合；第三根转写疑衍负号，见 [[queries/三次方程例A第三根正负号之辨]]）；例 B：六次方程六根 {−1, −1±2I, 2, 3, 4}（Vieta 关系复算吻合） | 六次方程数值六根（根和 ≈ 4、积 ≈ 2 复算吻合） | x+ArcCoth[x]−4==0：初值 1.1 → 1.00502，初值 5 → 3.72478（两根回代均等于 4，复算吻合） |

## 语义阶梯

1. 方程是逻辑表达式（[[concepts/Equal恒等判定与方程表示]]）：g = x²+2x−9==0 定义布尔值函数；% /. x->2 得 False（式 20.29a–b，替换算子见 [[concepts/Rule变换规则与替换算子]]）。
2. Roots[g,x] 给出析取命题 x == −1−√10 || x == −1+√10（20.29c）；ToRules 转为规则列表（20.29d）。书中表述：「Solve 在某种意义上相继进行了 Roots、ToRules 运算」。
3. 符号解不可得或过繁时转数值：NSolve（多项式）或 FindRoot（需初值与求解区域估计）。
4. 方程组层面另有 Eliminate、Reduce、FindInstance（表 20.11）；与单个未知数情形类似，NSolve 将给出方程组的数值解。

## 关联

- [[concepts/Solve方程求解命令族]]（命令族总纲）。
- 数值求根的程序化对应物：[[methodology/NestList实现牛顿迭代流程]]（20.2.8 手工实现牛顿迭代 vs 本节内置 FindRoot，二者依据各自的源文件）。
- 跨系统视角：[[findings/跨系统求根复算]]（19.8.4 中 Matlab/Mathematica/Maple 同题求根，依据 19.8.4 源文件）。