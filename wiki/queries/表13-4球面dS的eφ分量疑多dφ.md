---
type: query
title: 表 13.4 球面 dS 的 eφ 分量疑多 dφ
created: 2026-10-01
updated: 2026-10-01
tags: [转写讹误, 表13-4, 球面坐标系, 面元]
related: [线元面元与体积元, 表13-4线元面元体积元转录复算]
sources: ["数学手册(原书第10版)/13.3 向量场中的积分.md"]
---

# 表 13.4 球面 dS 的 e_φ 分量疑多 dφ

## 疑点

表 13.4 球面坐标系 $\mathrm{d}\vec S$ 的 $\vec{\mathrm{e}}_\varphi$ 分量转写为

$$\vec{\mathrm{e}}_\varphi\, r\,\mathrm{d}r\,\mathrm{d}\vartheta\,\mathrm{d}\varphi,$$

含**三个**微分元。面元是二重微分元（由曲面上两个参数产生），三个微分元量纲不符；且同表另两个分量（$\vec{\mathrm{e}}_r\,r^{2}\sin\vartheta\,\mathrm{d}\vartheta\,\mathrm{d}\varphi$、$\vec{\mathrm{e}}_\vartheta\,r\sin\vartheta\,\mathrm{d}r\,\mathrm{d}\varphi$）均恰含两个微分元。

## 复核（独立推导）

在 $\varphi=\text{const}$ 半平面上，$\partial\vec r/\partial r=\vec{\mathrm{e}}_r$，$\partial\vec r/\partial\vartheta=r\,\vec{\mathrm{e}}_\vartheta$，故

$$\left|\frac{\partial\vec r}{\partial r}\times\frac{\partial\vec r}{\partial\vartheta}\right|\mathrm{d}r\,\mathrm{d}\vartheta = \left|\vec{\mathrm{e}}_r\times r\vec{\mathrm{e}}_\vartheta\right|\mathrm{d}r\,\mathrm{d}\vartheta = r\,\mathrm{d}r\,\mathrm{d}\vartheta,$$

方向为 $\vec{\mathrm{e}}_\varphi$。故正确形式应为 $\vec{\mathrm{e}}_\varphi\, r\,\mathrm{d}r\,\mathrm{d}\vartheta$。

## 结论倾向

多余的 $\mathrm{d}\varphi$ 为转写讹误（高置信度：量纲论证＋独立推导一致）；但需原书扫描页最终确认是否存在原书排版异常。

## 待办

- 获取原书表 13.4 扫描页比对。