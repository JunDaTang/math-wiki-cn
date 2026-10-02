---
type: finding
title: xy 核算例全链复算与 λ=3 本征值独立验证
created: 2026-10-01
updated: 2026-10-01
tags: [积分方程, 第二类弗雷德霍姆积分方程, 诺伊曼级数, 预解式, 本征值, 算例复算, 数学手册]
related: [诺伊曼级数, 预解式, 迭代核, 退化核, 本征值与本征函数]
sources: ["数学手册(原书第10版)/11.2.2 逐次逼近法、诺伊曼级数.md"]
source: "[[10-数学手册原书第10版--15-1122-逐次逼近法诺伊曼级数--1pfpk9w]]"
confidence: high
replicated: true
---

# xy 核算例全链复算与 λ=3 本征值独立验证

对 11.2.2 节例题——第二类非齐次弗雷德霍姆积分方程 $\varphi(x)=x+\lambda\int_0^1 xy\,\varphi(y)\,\mathrm{d}y$（即 $K=xy$、$f=x$）——的全链复算，并附分析者的本征值独立验证（明确标注为推导，非原文内容）。

## 迭代核链（直接证据：复算通过）

| n | K_n(x,y) | 复算 |
|---|---|---|
| 1 | xy | 通过 |
| 2 | xy/3 | 通过：$\int_0^1 x\xi\cdot\xi y\,\mathrm{d}\xi=xy\int_0^1\xi^2\mathrm{d}\xi=xy/3$（原文微分误作 dy，见 [[queries/例中K2积分微分dy应为dη]]） |
| 3 | xy/9 | 通过：归纳步 $xy/3\cdot 1/3$ |
| n | xy/3^(n−1) | 通过：归纳成立 |

## 预解式与解（直接证据：复算通过）

- $\Gamma=xy\sum_{n\ge0}(\lambda/3)^n=\dfrac{xy}{1-\lambda/3}$，为几何级数之和，$\vert\lambda\vert<3$ 收敛。原文指出：在 (11.13c) 限制下（$\vert K\vert\le M=1$）诺伊曼级数对 $\vert\lambda\vert<1$ 必定收敛，而该几何级数“甚至当 $\vert\lambda\vert<3$ 时都收敛”。
- 由 (11.14b)：$\varphi(x)=x+\lambda\int_0^1\dfrac{xy^2}{1-\lambda/3}\,\mathrm{d}y=x\Big(1+\dfrac{\lambda}{3(1-\lambda/3)}\Big)=\dfrac{x}{1-\lambda/3}$，代回原方程直接验证通过。

## 关键观察：解公式越过诺伊曼收敛域（直接证据）

解公式 $\varphi=x/(1-\lambda/3)$ 对一切 $\lambda\ne3$ 成立（含 $\vert\lambda\vert\ge3$），精确印证原文“收敛域外的 λ 并非无解，只是不能由诺伊曼级数得到解”。注意：半径 3 是 xy 核的特性（恰为 L² 界 $1/\Vert K\Vert_{L^2}=3$，因 $\Vert K\Vert_{L^2}^2=1/9$），不可外推到一般核；例题只援引了较粗的 (11.13c)（半径 1），未指出 (11.13d) 恰好给出真实半径 3。

## λ=3 为本征值（分析者独立推导，非原文内容）

- **齐次方程有非平凡解**：$\varphi=3x\int_0^1 y\varphi(y)\,\mathrm{d}y$ 取 $\varphi=cx$，右端 $=3x\cdot c\int_0^1 y^2\mathrm{d}y=cx$，成立，故 λ=3 是本征值（Fredholm 约定 $\varphi=\lambda K\varphi$）。
- **λ=3、f=x 时非齐次无可解性**：设 $c=\int_0^1 y\varphi(y)\,\mathrm{d}y$，则 $\varphi=x+3cx$，代入得 $c=1/3+c$，矛盾，无解。
- 以上与解公式在 λ=3 处的极点、以及原文末段“不是本征值的任意 λ”的措辞精确吻合。

## 强度

高（直接证据：全链复算 + 代回验证）；本征值部分为分析者推导，数学自洽且与原文措辞及极点位置吻合，但非原文明言。