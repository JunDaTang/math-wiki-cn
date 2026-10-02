---
type: finding
title: 约化为主值的四条公式及 arccos 的奇偶分裂（式 2.141–2.144）
tags: [主值, 约化公式, 反三角函数, arc_k]
related: [主值, 反三角函数, 反正弦函数, 反余弦函数, 反正切函数, 反余切函数, 反三角函数单调区间分解与定义域值域表]
created: 2026-09-29
updated: 2026-09-29
source: "[[10-数学手册原书第10版--11-28-测圆或反三角函数--1yi9enf]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/2.8 测圆或反三角函数.md"]
---

# 约化为主值的四条公式及 arccos 的奇偶分裂（式 2.141–2.144）

手册 2.8.2 指出：$k=0$ 时得到主值，用不含指标的记号表示（$\arcsin x\equiv\operatorname{arc}_0\sin x$）；不同反函数的值可利用主值经下列公式计算：

$$\operatorname{arc}_{k}\sin x=k\pi+(-1)^{k}\arcsin x \tag{2.141}$$

$$\operatorname{arc}_{k}\cos x=\begin{cases}(k+1)\pi-\arccos x, & k\text{ 为奇数},\\ k\pi+\arccos x, & k\text{ 为偶数};\end{cases} \tag{2.142}$$

$$\operatorname{arc}_{k}\tan x=k\pi+\arctan x \tag{2.143}$$

$$\operatorname{arc}_{k}\cot x=k\pi+\operatorname{arccot} x \tag{2.144}$$

## 结构不对称性（本节最有复用价值的发现）

- **arcsin** 带 $(-1)^k$ 反转因子：正弦的单调区间以 $k\pi$ 为中心、交替升降，奇数 $k$ 分支须经反射再平移。
- **arccos** 需按 $k$ 奇偶分裂为两种平移：余弦的单调区间 $[k\pi,(k+1)\pi]$ 按 $k$ 奇偶朝不同方向覆盖主值区间 $[0,\pi]$。
- **arctan/arccot** 均为纯 $k\pi$ 平移：二者周期恰为 $\pi$，各分支只差一个周期平移。

这是四者单调区间位置差异（见 [[反三角函数单调区间分解与定义域值域表]]）的直接推论。

## 算例（原文照录）

- A：$\arcsin0=0$，$\operatorname{arc}_k\sin0=k\pi$。
- B：$\operatorname{arccot}1=\frac{\pi}{4}$，$\operatorname{arc}_{k}\cot1=\frac{\pi}{4}+k\pi$。
- C：$\arccos\frac12=\frac{\pi}{3}$，$\operatorname{arc}_k\cos\frac12=\begin{cases}-\frac{\pi}{3}+(k+1)\pi, & k\text{ 为奇数},\\ \frac{\pi}{3}+k\pi, & k\text{ 为偶数},\end{cases}$ 与式 2.142 完全吻合。

注：计算器给出的是反三角函数的主值。

## 验证状态

式 2.141–2.145 在 $x=\pm1$ 等边界点做了抽样符号/数值核验，全部通过；算例 A–C 与公式一致。相关概念见 [[主值]]。