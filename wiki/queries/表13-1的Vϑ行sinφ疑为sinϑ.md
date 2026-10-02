---
type: query
title: 表 13.1 的 V_ϑ 行 sin φ 疑为 sin ϑ
created: 2026-10-01
updated: 2026-10-01
tags: [数学手册, 讹误, 坐标变换, 矛盾]
related: [10-数学手册原书第10版--14-131-向量场理论的基本概念--qrwpe3, 笛卡儿柱面与球面坐标系向量分量表示比较, 表13-1与式13-18至13-25坐标系变换转录复算]
sources: ["数学手册(原书第10版)/13.1 向量场理论的基本概念.md"]
---
# 表 13.1 的 V_ϑ 行 sin φ 疑为 sin ϑ

## 矛盾

表 13.1（笛卡儿、柱面、球面坐标系中向量分量的关系）倒数第二行（$V_\vartheta$ 行）**笛卡儿列**作：

$$V_x\cos\vartheta\cos\varphi + V_y\cos\vartheta\sin\varphi - V_z\sin\varphi,$$

而式 (13.21) 第二式作：

$$V_\vartheta = V_x\cos\vartheta\cos\varphi + V_y\cos\vartheta\sin\varphi - V_z\sin\vartheta.$$

两处的末项 $\sin\varphi$ 与 $\sin\vartheta$ 直接矛盾。

## 复算判定

以单位向量点积投影（$\vec{e}_\vartheta = \cos\vartheta\cos\varphi\,\vec{i} + \cos\vartheta\sin\varphi\,\vec{j} - \sin\vartheta\,\vec{k}$）独立重建，式 (13.21) 正确；表内 $-V_z\sin\varphi$ 为讹误。表 13.1 其余各行（柱面列、球面列全部，以及笛卡儿列其余各行）复算均正确。

## 开放问题

- 该讹误系原书印刷错误还是 OCR/转写引入？需对照原书（原书第 10 版）确认。
- 若为原书即误，应在引用表 13.1 时附勘误注记；若为转写引入，直接修正。

## 使用影响

使用表 13.1 由笛卡儿分量求 $V_\vartheta$（或反向）时，应以式 (13.21) 为准；该行的柱面直换列（$V_\rho\cos\vartheta - V_z\sin\vartheta$）与球面列（$V_\vartheta$）不受影响。操作化流程见 [[向量分量坐标系变换流程]]。