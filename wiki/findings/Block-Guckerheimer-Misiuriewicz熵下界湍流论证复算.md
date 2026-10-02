---
type: finding
title: "Block-Guckerheimer-Misiuriewicz 熵下界湍流论证复算"
created: 2026-10-01
updated: 2026-10-01
tags: [转录复算, 拓扑熵, 周期轨道, 一维映射]
related: [Block-Guckenheimer-Misiuriewicz定理, 拓扑熵, 沙可夫斯基定理, Block, Guckenheimer, Misiuriewicz]
sources: ["数学手册(原书第10版)/17.2.6 一维映射的混沌.md"]
source: "[[10-数学手册原书第10版--12-1726-一维映射的混沌--l6tj88]]"
confidence: medium
replicated: null
---
# Block-Guckerheimer-Misiuriewicz 熵下界湍流论证复算

（页名沿用源文拼写「Guckerheimer」，订正拼写之辨见 [[queries/Guckerheimer疑为Guckenheimer之辨]]。）

## 转录原文

```text
Block-Guckerheimer-Misiuriewicz 定理 $\varphi : I  I$ 为紧区间 到自身的连续映射，若 $\{ \varphi ^ { k } \}$ 有一个 $2 ^ { n } m$ 周期轨道 $( m > 1$ ，奇数），则 $h ( \varphi ) \geqslant { \frac { \ln 2 } { 2 ^ { n + 1 } } }$
```

（除「$\varphi : I\ \ I$」脱箭头与冠名拼写外，此定理陈述完整。）

## 复算：算术自洽核验（推断性，非源文推导）

1. 设 $g=\varphi^{2^{n}}$，则 $g$ 有周期 $m$ 的轨道（$m>1$ 奇数）。
2. 按通行的湍流/二阶马蹄论证，奇周期 $>1$ 蕴含 $g^{2}$ 具马蹄，故 $h(g^{2})\geqslant\ln 2$，即 $h(g)\geqslant\tfrac{1}{2}\ln 2$。
3. 由熵的幂规则 $h(\varphi^{k})=k\,h(\varphi)$：$h(\varphi^{2^{n}})=2^{n}h(\varphi)\geqslant\tfrac{1}{2}\ln 2$，故 $h(\varphi)\geqslant\ln 2/2^{\,n+1}$。

指数 $n+1$ 与源文下界吻合，陈述在算术上自洽。**注意**：步骤 2 的前提（奇周期 $\Rightarrow$ 二阶迭代具马蹄）为通行一维动力学结果，未见于本手册，故此核验为推断性重构，非对源文证明的复现。

## 特例与一致性（推断）

- $n=0$（奇周期 $m>1$）：$h\geqslant\tfrac{1}{2}\ln 2\approx 0.3466$。
- $n=1$（周期 $2m$）：$h\geqslant\tfrac{1}{4}\ln 2$。
- 周期中 2 的幂次越高（在沙可夫斯基序中越靠后），下界越弱——与 [[concepts/沙可夫斯基定理]] 序的复杂性直观一致。

## 待核

冠名拼写（Guckerheimer/Guckenheimer）、作者名单是否完整（Stage 1 分析提示或有第四作者 Sanders）及更精细下界 $\log\lambda_{m}/2^{\,n}$（$\lambda_{m}$ 依赖奇周期 $m$）与手册下界的关系，见 [[queries/Guckerheimer疑为Guckenheimer之辨]]。