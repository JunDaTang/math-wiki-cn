---
type: query
title: 热导方程例中 cλ 疑为 cρ
created: 2026-10-01
updated: 2026-10-01
tags: [转写讹误, 热传导方程, 热导方程, 例C]
related: [热传导方程, 式13-120至13-127高斯斯托克斯格林积分定理转录复算, 热导方程a²未定义]
sources: ["数学手册(原书第10版)/13.3 向量场中的积分.md"]
---

# 热导方程例中 cλ 疑为 cρ

## 疑点

13.3.3 定理例 C 推导热导方程：热平衡给出

$$\iiint_{v}\left[c\varrho\,\frac{\partial T}{\partial t}-\operatorname{div}(\lambda\operatorname{grad}T)\right]\mathrm{d}v=0,$$

其中 $c$ 为比热容、$\varrho$ 为密度、$\lambda$ 为热导率。逐点推出应为

$$c\varrho\,\frac{\partial T}{\partial t}=\operatorname{div}(\lambda\operatorname{grad}T),$$

但转写正文的结果式写作"$c\lambda\,\partial T/\partial t=\operatorname{div}(\lambda\operatorname{grad}T)$"。

## 论证

被积函数连续时体积分恒为零蕴含被积函数逐点为零，左端系数只能取 $c\varrho$；且推导第一步（区域热量变化率 $\mathrm{d}Q/\mathrm{d}t=\iiint_v c\varrho\,\partial T/\partial t\,\mathrm{d}v$）也写作 $c\varrho$。"$c\lambda$"与推导链自相矛盾，疑为转写讹误（或原书排版误植）。

## 待办

- 原书扫描页确认；同时确认 $a^2=\lambda/(c\varrho)$ 是否在原书给出而转写丢失（见 [[热导方程a²未定义]]）。