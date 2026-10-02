---
type: finding
title: 21.14 双表 tanh 疑为 sinh 四条复算
tags: [闭式复算, 转写讹误, 傅里叶变换]
related: [21-14双表tanh与sinh之辨, 傅里叶积分闭式复算法, 傅里叶余弦变换, 傅里叶正弦变换]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/21.14 傅里叶变换.md"]
source: "[[10-数学手册原书第10版--10-2114-傅里叶变换--12suskw]]"
confidence: high
replicated: false
---

# 21.14 双表 tanh 疑为 sinh 四条复算

[[sources/10-数学手册原书第10版--10-2114-傅里叶变换--12suskw]] 中四条表值出现 $\tanh$，闭式复算均应为 $\sinh$：

| 位置 | $f(t)$ | 转录值（涉 tanh 支） | 复算值 |
|---|---|---|---|
| 21.14.1-40（ω>a 支） | $\frac{t\sin(at)}{t^2+b^2}$ | $-\frac{\pi}{2}e^{-b\omega}\tanh(ab)$ | $-\frac{\pi}{2}e^{-b\omega}\sinh(ab)$ |
| 21.14.1-41（ω>a 支） | $\frac{\sin(at)}{t(t^2+b^2)}$ | $\frac{\pi}{2}b^{-2}e^{-b\omega}\tanh(ab)$ | $\frac{\pi}{2}b^{-2}e^{-b\omega}\sinh(ab)$ |
| 21.14.2-48（两支） | $\frac{\sin(at)}{b^2+t^2}$ | $\frac{\pi}{2}\frac{e^{-ab}}{b}\tanh(b\omega)$ 与 $\frac{\pi}{2}\frac{e^{-b\omega}}{b}\tanh(ab)$ | 两支 tanh 均应为 $\sinh$ |
| 21.14.2-57（ω<a 支） | $\frac{t\cos(at)}{b^2+t^2}$ | $-\frac{\pi}{2}e^{-ab}\tanh(b\omega)$ | $-\frac{\pi}{2}e^{-ab}\sinh(b\omega)$ |

**推导**：积化和差后用 $\int_0^\infty\frac{\cos kt}{t^2+b^2}dt=\frac{\pi}{2b}e^{-b|k|}$ 与 $\int_0^\infty\frac{t\sin kt}{t^2+b^2}dt=\frac{\pi}{2}e^{-b|k|}\operatorname{sgn}k$，两支合并即得 $\sinh$。

**互证**：同构的 51 号 $\frac{\cos(at)}{b^2+t^2}$（$\cosh/\cosh$ 双支）复算通过，与 sinh 型结构一致；40/41/48/57 号的另一支（$\cosh$ 支）亦均复算通过，唯 tanh 支不符。

**数值锚点**（$a=2,b=1,\omega=1$，对 21.14.2-48 之 ω<a 支）：数值复算 0.2498；sinh 式给 0.2498；tanh 式给 0.1620。21.14.2-57 之 ω<a 支锚点为 −0.2498 对 −0.1620。

判定针对转录层，属原书抑或转写之误见 [[queries/21-14双表tanh与sinh之辨]]。