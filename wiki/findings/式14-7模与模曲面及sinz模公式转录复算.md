---
type: finding
title: 式 14.7 模与模曲面及 sin z 模公式转录复算
tags: [转录复算, 模, 模曲面, sinz]
related: [模曲面, 解析函数]
created: 2026-10-01
updated: 2026-10-01
sources: ["数学手册(原书第10版)/14.1.2 解析函数.md"]
source: "[[sources/10-数学手册原书第10版--9-1412-解析函数--6ka1tv]]"
confidence: high
replicated: true
---

# 式 14.7 模与模曲面及 sin z 模公式转录复算

## 转录（直接证据）

手册原文（14.1.2.3）：

$$
|w| = |f(z)| = \sqrt{[u(x,y)]^2 + [v(x,y)]^2} = \varphi(x,y).\tag{14.7}
$$

例 A（属 $f(z) = \sin z$ 的断言）：函数 $\sin z = \sin x \cosh y + \mathrm{i}\cos x \sinh y$ 的绝对值是 $|\sin z| = \sqrt{\sin^2 x + \sinh^2 y}$，图 14.2(a) 展示了其模曲面。例 B（属 $w = e^{1/z}$ 的断言）：其模曲面在图 14.2(b) 中展示。

## 复算（独立验证）

$|\sin z|^2 = \sin^2 x \cdot \cosh^2 y + \cos^2 x \cdot \sinh^2 y$。利用 $\cosh^2 y - \sinh^2 y = 1$：

$$
\sin^2 x\,(1 + \sinh^2 y) + \cos^2 x \cdot \sinh^2 y = \sin^2 x + \sinh^2 y.
$$

故 $|\sin z| = \sqrt{\sin^2 x + \sinh^2 y}$。**与原文一致，验证通过**。(14.7) 本身即复数模的定义式，自明。

## 结论

- 直接证据：手册给出 (14.7)、$\sin z$ 的模公式，并断言模曲面恒在 $z$ 平面之上、仅在函数的根处（$|f(z)| = 0$）接触平面。
- 推断验证：$\sin z$ 模公式复算通过。
- 转写噪声："即间是点 z=x+iy 之上的第个坐标"整句 garbled（当为"即它是点 $z = x + \mathrm{i}y$ 之上的第三个坐标"）；"14.2(a) 展示了"疑缺"图"字；OCR 图注块顺序与正文断言相反，疑图 14.2(a)(b) 图注错位，见 [[queries/14-1-2全节系统性转写讹误清单]]。