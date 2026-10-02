---
type: finding
title: "算例 A：x²cos ax 的 50 阶导数复算确认"
tags: [莱布尼茨公式, 高阶导数, 算例, 数学手册]
related: [莱布尼茨公式, 莱布尼茨公式截断计算流程, 6-1-3全节系统性转写讹误清单]
created: 2026-09-30
updated: 2026-09-30
source: "[[10-数学手册原书第10版--8-613-高阶导数--1acw7vn]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/6.1.3 高阶导数.md"]
---

# 算例 A：x²cos ax 的 50 阶导数复算确认

《数学手册》6.1.3.3 算例 A 计算 $\left(x^{2}\cos ax\right)^{(50)}$。取 $v = x^{2}$（$v' = 2x$，$v'' = 2$，$v''' = v^{(4)} = \cdots = 0$）、$u = \cos ax$（$u^{(k)} = a^{k}\cos\left(ax + k\frac{\pi}{2}\right)$），则除前三项外其他被加式均为 0（原文此句「其他的被加式均为 0,以」疑脱「所」字，见 [[queries/6-1-3全节系统性转写讹误清单]]）。原文计算（逐字转录）：

$$
\begin{array}{rl}
(uv)^{(50)} = & x^{2} a^{50}\cos\left(ax + 50\frac{\pi}{2}\right) + \frac{50}{1}\cdot 2x\, a^{49}\cos\left(ax + 49\frac{\pi}{2}\right) \\
& + \frac{50\cdot 49}{1\cdot 2}\cdot 2\, a^{48}\cos\left(ax + 48\frac{\pi}{2}\right) \\
= & a^{48}\left[(2450 - a^{2}x^{2})\cos ax - 100\,ax\sin ax\right].
\end{array}
$$

## 独立复算

莱布尼茨和式（式 6.23）中仅 $m \in \{48, 49, 50\}$ 三项非零（对应 $D^{50-m}v \neq 0$）：

- $m = 50$：$\binom{50}{50}\, D^{50}u \cdot v = a^{50}\cos(ax + 25\pi)\cdot x^{2} = -a^{50}x^{2}\cos ax$；
- $m = 49$：$\binom{50}{49}\, D^{49}u \cdot Dv = 50\cdot a^{49}\cos\left(ax + \tfrac{49\pi}{2}\right)\cdot 2x = -100\,a^{49}x\sin ax$；
- $m = 48$：$\binom{50}{48}\, D^{48}u \cdot D^{2}v = 1225\cdot a^{48}\cos(ax + 24\pi)\cdot 2 = 2450\,a^{48}\cos ax$。

角度归约：$50\cdot\frac{\pi}{2} = 25\pi \Rightarrow \cos(ax + 25\pi) = -\cos ax$；$\frac{49\pi}{2} = 24\pi + \frac{\pi}{2} \Rightarrow \cos\left(ax + \frac{49\pi}{2}\right) = -\sin ax$；$48\cdot\frac{\pi}{2} = 24\pi \Rightarrow \cos(ax + 24\pi) = \cos ax$。合并得

$$(uv)^{(50)} = a^{48}\left[(2450 - a^{2}x^{2})\cos ax - 100\,ax\sin ax\right],$$

与手册的中间步骤及最终结果完全一致。

## 结论

手册本算例的中间步骤与最终结果均正确（已独立复算）。本算例演示的多项式因子截断技巧见 [[methodology/莱布尼茨公式截断计算流程]]。