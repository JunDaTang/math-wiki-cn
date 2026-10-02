---
type: query
title: "例题 1/(z−a) 分式分子丢失"
created: 2026-10-01
updated: 2026-10-01
tags: [转写讹误, 复积分, 数学手册]
related: [式14-33a至14-43复积分定义定理与例题转录复算, 14-2全节系统性转写讹误清单, 14-2未入库回指缺口]
sources: ["数学手册(原书第10版)/14.2 复平面中的积分.md"]
---

# 例题 1/(z−a) 分式分子丢失

14.2.1.2.5 例题的转写文本为：

> (C)∮ z − a ~ dz = 2πi Res f(z)∣_{z=a} = 2πi

其中被积函数的分式 $\frac{1}{z-a}$ 的分子「1/」在转写中丢失，「~」为转写噪声；复原后应为：

$$(C)\oint \frac{1}{z-a}\,\mathrm{d}z = 2\pi\mathrm{i}\,\operatorname{Res} f(z)\big|_{z=a} = 2\pi\mathrm{i}$$

（$f(z) = \frac{1}{z-a}$，C 为以逆时针方向围绕 $a$ 的闭曲线，图 14.34。）复原后数值复算无误（见 [[findings/式14-33a至14-43复积分定义定理与例题转录复算]]）。

## 待决问题

- 原书中 $\operatorname{Res} f(z)|_{z=a}$ 之后是否显式写出「= 1」（即 $2\pi\mathrm{i}\cdot\operatorname{Res} = 2\pi\mathrm{i}\cdot 1$）？转写疑还吞掉该步，建议对照原书图版确认。
- Res 记号在本节未定义即使用，其定义在 14.3.5.5（未入库），见 [[queries/14-2未入库回指缺口]]。