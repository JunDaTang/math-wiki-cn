---
type: concept
title: "Block-Guckenheimer-Misiuriewicz 定理"
created: 2026-10-01
updated: 2026-10-01
tags: [动力系统, 一维映射, 拓扑熵, 周期轨道, 混沌]
related: [Block, Guckenheimer, Misiuriewicz, 拓扑熵, 沙可夫斯基定理, 一维映射的混沌, Guckerheimer疑为Guckenheimer之辨, Block-Guckerheimer-Misiuriewicz熵下界湍流论证复算]
sources: ["数学手册(原书第10版)/17.2.6 一维映射的混沌.md"]
---
# Block-Guckenheimer-Misiuriewicz 定理

Block-Guckenheimer-Misiuriewicz 定理是《数学手册》(原书第10版) 17.2.6 的三个一维混沌判据之一，冠名者为 [[entities/Block]]、[[entities/Guckenheimer]]（源文拼作「Guckerheimer」，疑为转录讹）、[[entities/Misiuriewicz]]。它把周期结构转化为拓扑熵的定量下界。

## 定理陈述

设 $\varphi: I \to I$ 为紧区间到自身的连续映射。若 $\{\varphi^{k}\}$ 有一个 $2^{n} m$ 周期轨道（$m>1$，奇数），则

$$h(\varphi) \geqslant \frac{\ln 2}{2^{\,n+1}}.$$

（源文此定理陈述完整，唯「$\varphi : I\ \ I$」脱箭头与冠名拼写存疑。）

## 意义

- 与 [[concepts/沙可夫斯基定理]] 合用：任何周期非 $2$ 之幂的轨道都可写成 $2^{n}m$（$m>1$ 奇数）形式，故「存在非 2 幂周期 $\Rightarrow h(\varphi)>0$」——这是「正熵 ⟺ 非 2 幂周期 ⟺ 混沌」等价链（综合推断）的一半，见 [[concepts/一维映射的混沌]]。
- 下界随 $n$ 增大而减弱：周期中 2 的幂次越高，在沙可夫斯基序中位置越靠后，所得熵下界越小，与序的复杂性直观一致（推断性说明）。

## 推断性核验（非源文）

设 $g=\varphi^{2^{n}}$，则 $g$ 有奇周期 $m>1$ 的轨道；按通行的湍流/二阶马蹄论证，$g^{2}$ 具马蹄，故 $h(g^{2})\geqslant \ln 2$；再由熵的幂规则 $h(\varphi^{k})=k\,h(\varphi)$ 得 $2^{\,n+1} h(\varphi)\geqslant \ln 2$，即 $h(\varphi)\geqslant \ln 2/2^{\,n+1}$——指数 $n+1$ 与源文吻合。此推导为核验性重构，其前提（奇周期 $\Rightarrow$ 二阶迭代具马蹄）未见于本手册。详见 [[findings/Block-Guckerheimer-Misiuriewicz熵下界湍流论证复算]]。

## 待核问题

冠名拼写「Guckerheimer」疑为「Guckenheimer」；原始文献中该结果是否另含第四作者（Stage 1 分析提示或为 Sanders）及更精细下界 $\log\lambda_{m}/2^{\,n}$（$\lambda_{m}$ 依赖奇周期 $m$）与手册下界的关系，见 [[queries/Guckerheimer疑为Guckenheimer之辨]]。

## 边界

下界只依赖 $2^{n}m$ 形式周期的存在性，仅对区间连续映射成立；不涉高维，也不给出熵的上界或精确值。