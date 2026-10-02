---
type: finding
title: arcsin 与 arccos 的和差公式分段体系（式 2.155–2.158）
tags: [和差公式, arcsin, arccos, 加法定理, 主值]
related: [反正弦函数, 反余弦函数, 加法定理, 主值, 式2-155与2-156编号及条件行错乱如何复原, 式2-158前是否缺失arccos差公式标题行]
created: 2026-09-29
updated: 2026-09-29
source: "[[10-数学手册原书第10版--11-28-测圆或反三角函数--1yi9enf]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/2.8 测圆或反三角函数.md"]
---

# arcsin 与 arccos 的和差公式分段体系（式 2.155–2.158）

手册 2.8.5–2.8.6 给出 arcsin 与 arccos 的和差公式，结果依条件分段以保证落回主值区间：

$$\arcsin x+\arcsin y=\begin{cases}\arcsin\left(x\sqrt{1-y^{2}}+y\sqrt{1-x^{2}}\right), & xy\leqslant0\ \text{或}\ x^{2}+y^{2}\leqslant1,\\ \pi-\arcsin\left(x\sqrt{1-y^{2}}+y\sqrt{1-x^{2}}\right), & x>0,\ y>0,\ x^{2}+y^{2}>1,\\ -\pi-\arcsin\left(x\sqrt{1-y^{2}}+y\sqrt{1-x^{2}}\right), & x<0,\ y<0,\ x^{2}+y^{2}>1,\end{cases} \tag{2.155}$$

$$\arcsin x-\arcsin y=\begin{cases}\arcsin\left(x\sqrt{1-y^{2}}-y\sqrt{1-x^{2}}\right), & xy\geqslant0\ \text{或}\ x^{2}+y^{2}\leqslant1,\\ \pi-\arcsin\left(x\sqrt{1-y^{2}}-y\sqrt{1-x^{2}}\right), & x>0,\ y<0,\ x^{2}+y^{2}>1,\\ -\pi-\arcsin\left(x\sqrt{1-y^{2}}-y\sqrt{1-x^{2}}\right), & x<0,\ y>0,\ x^{2}+y^{2}>1,\end{cases} \tag{2.156}$$

$$\arccos x+\arccos y=\begin{cases}\arccos\left(xy-\sqrt{1-x^{2}}\sqrt{1-y^{2}}\right), & x+y\geqslant0,\\ 2\pi-\arccos\left(xy-\sqrt{1-x^{2}}\sqrt{1-y^{2}}\right), & x+y<0,\end{cases} \tag{2.157}$$

$$\arccos x-\arccos y=\begin{cases}-\arccos\left(xy+\sqrt{1-x^{2}}\sqrt{1-y^{2}}\right), & x\geqslant y,\\ \arccos\left(xy+\sqrt{1-x^{2}}\sqrt{1-y^{2}}\right), & x<y,\end{cases} \tag{2.158}$$

## 结构观察

- **判据不对称**：arcsin 的和差按 $xy$ 的符号与 $x^{2}+y^{2}$ 是否超过 1 分三段（对应和/差是否越出 $[-\frac{\pi}{2},\frac{\pi}{2}]$）；arccos 的和按 $x+y$ 的符号分两段、差按 $x,y$ 的大小分两段。
- 这些公式是 [[加法定理]] $\sin(\alpha\pm\beta)$、$\cos(\alpha\pm\beta)$ 的逆向使用：先用加法定理算出和/差的正弦或余弦，再依分段条件选取回到主值区间的方式。

## 转写问题（登记）

- 式 2.155–2.156 在转写文本中编号漂移、条件行「(x < 0, y < 0, x² + y² > 1)」孤立出现又随 −π 分支重复；上式为复原后的结构，复原依据见 [[式2-155与2-156编号及条件行错乱如何复原]]。
- 式 2.158 前的等式左端「arccos x − arccos y =」在转写中丢失；上式左端为按主值域推断的复原（$x\geqslant y$ 时 $\arccos x-\arccos y\leqslant0$，取负号分支），见 [[式2-158前是否缺失arccos差公式标题行]]。

## 验证状态

式 2.155–2.158 在 $x=\pm1$、$x=1/y=-1$ 等边界点抽样核验通过（含分段边界的归属）；2.158 复原的左端亦核验通过。相关概念见 [[反正弦函数]]、[[反余弦函数]]。