---
type: finding
title: arctan 的和差公式分段体系（式 2.159–2.160）
tags: [和差公式, arctan, 加法定理, 主值]
related: [反正切函数, 加法定理, 主值, 反余切函数, arcsin与arccos的和差公式]
created: 2026-09-29
updated: 2026-09-29
source: "[[10-数学手册原书第10版--11-28-测圆或反三角函数--1yi9enf]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/2.8 测圆或反三角函数.md"]
---

# arctan 的和差公式分段体系（式 2.159–2.160）

手册 2.8.7 给出 arctan 的和差公式，判据为 $xy$ 与 $\pm1$ 的比较：

$$\arctan x+\arctan y=\begin{cases}\arctan\frac{x+y}{1-xy}, & xy<1,\\ \pi+\arctan\frac{x+y}{1-xy}, & x>0,\ xy>1,\\ -\pi+\arctan\frac{x+y}{1-xy}, & x<0,\ xy>1,\end{cases} \tag{2.159}$$

$$\arctan x-\arctan y=\begin{cases}\arctan\frac{x-y}{1+xy}, & xy>-1,\\ \pi+\arctan\frac{x-y}{1+xy}, & x>0,\ xy<-1,\\ -\pi+\arctan\frac{x-y}{1+xy}, & x<0,\ xy<-1,\end{cases} \tag{2.160}$$

## 结构观察

- 和与差呈现镜像对称：和公式以 $xy<1$ 为基本段、$xy>1$ 时按 $x$ 的符号加 $\pm\pi$；差公式以 $xy>-1$ 为基本段、$xy<-1$ 时按 $x$ 的符号加 $\pm\pi$。
- 这些公式是 [[加法定理]] $\tan(\alpha\pm\beta)$ 的逆向使用，分段条件保证结果落回主值区间 $(-\frac{\pi}{2},\frac{\pi}{2})$。
- **边界留白**（非错误）：$xy=\pm1$ 未覆盖，此时和/差为 $\pm\frac{\pi}{2}$，公式右端分母为零、$\arctan$ 趋于 $\pm\frac{\pi}{2}$，属手册惯用的严格不等式口径。
- 手册未给 arccot 的和差公式；需要时可经 $\operatorname{arccot}x=\frac{\pi}{2}-\arctan x$（手册约定，见 [[反余切函数]]）由本组公式导出。

## 验证状态

式 2.159–2.160 在 $x=\pm1$、$x=y=\sqrt3$（$xy=3>1$ 的 $+\pi$ 分支）、$x=1/y=-1$ 邻域等边界点抽样核验通过。相关概念见 [[反正切函数]]。