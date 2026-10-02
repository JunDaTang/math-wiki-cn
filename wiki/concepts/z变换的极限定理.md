---
type: concept
title: "Z变换的极限定理"
created: 2026-10-01
updated: 2026-10-01
tags: [z变换, 极限定理, 初值定理, 终值定理]
related: [z变换, z逆变换, 初值与终值定理, z变换四种逆变换方法选用流程]
sources: ["数学手册(原书第10版)/15.4 Z变换.md"]
---

# Z变换的极限定理

Z变换的极限定理是与拉普拉斯变换极限性质（式 15.7b，见 [[concepts/初值与终值定理]]）类似的、联系原序列与其变换 $F(z)$ 的极限命题（《数学手册》15.4.1.2, 3.）。

## （a）初值与逐项恢复

若 $F(z)=\mathcal{Z}\{f_n\}$ 存在，则

$$f_0=\lim_{z\to\infty}F(z)\tag{15.108}$$

此处 $z$ 可以沿着实轴或其他任何路径趋向无穷大。由于级数

$$z\{F(z)-f_0\}=f_1+f_2\frac1z+f_3\frac1{z^2}+\dots,\qquad z^2\{F(z)-f_0-f_1/z\}=f_2+f_3\frac1z+f_4\frac1{z^2}+\dots\tag{15.109/15.110}$$

本身明显是 Z变换，类似于 (15.108) 可得

$$f_1=\lim_{z\to\infty}z\{F(z)-f_0\},\qquad f_2=\lim_{z\to\infty}z^2\{F(z)-f_0-f_1/z\},\ \dots\tag{15.111}$$

通过这种方式，原序列 $\{f_n\}$ 可根据其变换 $F(z)$ **逐项恢复**——这是 Z逆变换的方法之四（见 [[concepts/z逆变换]]）。

## （b）终值定理（单向性）

若 $\lim_{n\to\infty}f_n$ 存在，则

$$\lim_{n\to\infty}f_n=\lim_{z\to1+0}(z-1)F(z)\tag{15.112}$$

**单向性警示**：上述命题**不可逆**——根据 (15.112)，只有能保证 $\lim_{n\to\infty}f_n$ 存在时，才能确定其值。反例：$f_n=(-1)^n$，则 $\mathcal{Z}\{f_n\}=\dfrac{z}{z+1}$，且 $\lim_{z\to1+0}(z-1)\dfrac{z}{z+1}=0$，但 $\lim_{n\to\infty}(-1)^n$ 不存在。此单向性是 (15.112) 专属命题，(15.108)/(15.111) 不受此限（它们对任意可变换序列成立）。

## 离散—连续对偶

| 拉普拉斯（连续） | Z变换（离散） |
|---|---|
| $f(+0)=\lim_{p\to\infty}pF(p)$ | $f_0=\lim_{z\to\infty}F(z)$（15.108） |
| $\lim_{t\to\infty}f(t)=\lim_{p\to0}pF(p)$ | $\lim_{n\to\infty}f_n=\lim_{z\to1+0}(z-1)F(z)$（15.112，单向） |

对应关系 $z\to\infty\leftrightarrow p\to\infty$、$z\to1+0\leftrightarrow p\to0+0$ 源于代换 $z=e^p$。复算核验（含反例验证）见 [[findings/式15-105至15-112-z变换定义收敛与极限定理转录复算]]。