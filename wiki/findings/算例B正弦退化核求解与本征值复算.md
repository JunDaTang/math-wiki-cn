---
type: finding
title: 算例 B 正弦退化核求解与本征值复算
tags: [算例复算, 积分方程, 退化核, 本征值, 本征函数, Cramer法则]
related: [concepts/积分方程的本征值与本征函数, concepts/退化核, methodology/退化核求解流程, entities/第二类弗雷德霍姆积分方程, queries/11-2-1全节系统性转写讹误清单]
created: 2026-09-30
updated: 2026-09-30
source: "[[sources/10-数学手册原书第10版--15-1121-具有退化核的积分方程--1pg6dhz]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/11.2.1 具有退化核的积分方程.md"]
---
# 算例 B 正弦退化核求解与本征值复算

**结论**：算例 B（核 $\sin(x+y)$，区间 $[0,\pi]$）的全部系数、$D(\lambda)$、Cramer 解与本征值/本征函数经独立复算吻合。

## 题目与分解

$$\varphi(x) = x + \lambda\int_0^{\pi}\sin(x+y)\,\varphi(y)\,\mathrm{d}y,\qquad K(x,y)=\sin(x+y)=\sin x\cos y+\cos x\sin y$$

两项退化核：$\alpha_1=\sin x,\ \beta_1=\cos y;\ \alpha_2=\cos x,\ \beta_2=\sin y$。

## 系数复算（全部吻合）

| 量 | 复算值 | 核对 |
|---|---|---|
| $c_{11}=\int_0^{\pi}\sin x\cos x\,\mathrm{d}x$ | $0$ | ✓ |
| $c_{12}=\int_0^{\pi}\cos^2 x\,\mathrm{d}x$ | $\pi/2$ | ✓ |
| $c_{21}=\int_0^{\pi}\sin^2 x\,\mathrm{d}x$ | $\pi/2$ | ✓ |
| $c_{22}=\int_0^{\pi}\cos x\sin x\,\mathrm{d}x$ | $0$ | ✓ |
| $b_{1}=\int_0^{\pi}x\cos x\,\mathrm{d}x$ | $-2$ | ✓ |
| $b_{2}=\int_0^{\pi}x\sin x\,\mathrm{d}x$ | $\pi$ | ✓ |

## 方程组、判据与解

$$A_1 - \lambda\tfrac{\pi}{2}A_2 = -2,\qquad -\lambda\tfrac{\pi}{2}A_1 + A_2 = \pi$$

$$D(\lambda) = \begin{vmatrix}1 & -\lambda\pi/2\\ -\lambda\pi/2 & 1\end{vmatrix} = 1-\lambda^2\tfrac{\pi^2}{4}$$

Cramer 法则复算：

$$A_1 = \frac{\lambda\pi^2/2 - 2}{1-\lambda^2\pi^2/4}\ ✓,\qquad A_2 = \frac{\pi(1-\lambda)}{1-\lambda^2\pi^2/4}\ ✓$$

$$\varphi(x) = x + \lambda\,\frac{(\lambda\pi^2/2-2)\sin x + \pi(1-\lambda)\cos x}{1-\lambda^2\pi^2/4}\ ✓$$

## 本征值与本征函数

$D(\lambda)=0 \Rightarrow \lambda_{1}=\dfrac{2}{\pi},\ \lambda_{2}=-\dfrac{2}{\pi}$。齐次方程 $\varphi(x)=\lambda_k\int_0^\pi\sin(x+y)\varphi(y)\,\mathrm{d}y$ 的非零解 $\varphi_k(x)=\lambda_k(A_1\sin x+A_2\cos x)$：

- $\lambda_1=2/\pi$：齐次组给出 $A_1=A_2 \Rightarrow \varphi_1(x)=A(\sin x+\cos x)$ ✓
- $\lambda_2=-2/\pi$：齐次组给出 $A_1=-A_2 \Rightarrow \varphi_2(x)=B(\sin x-\cos x)$ ✓

（$A$、$B$ 为任意常数；转写原文两处"其中 为任意常数"分别漏 "A"/"B"。）

## 记号说明（非实质差异）

一般陈述中本征函数写作 $C\sum A_k\alpha_k$（把 $\lambda$ 吸收进常数），本算例写作 $\lambda_k(A_1\sin x+A_2\cos x)$（保留 $\lambda$）——因常数任意而等价，不构成矛盾。

## 转写问题

$\varphi$ 上多余假点、"A₁ 小和 A₂"衍字"小"、$\lambda$ 上多余横线（$\bar\lambda\pi^2/2$、$\bar{\lambda_2}=-2/\pi$）等，见 [[queries/11-2-1全节系统性转写讹误清单]]，均不影响数学内容。