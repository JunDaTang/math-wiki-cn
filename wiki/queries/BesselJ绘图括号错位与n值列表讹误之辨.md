---
type: query
title: BesselJ 绘图括号错位与 n 值列表讹误之辨
tags: [校勘, 转写讹误, mathematica, besselj]
related: [20-4全节系统性转写讹误清单, 式20-44a-b贝塞尔函数绘图复算, 10-数学手册原书第10版--18-204-用mathematica绘图--f10hmv]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.4 用Mathematica绘图.md"]
---

# BesselJ 绘图括号错位与 n 值列表讹误之辨

## 现象一：In[1] 括号错位

式 20.44a 原样：`bj0 = Plot[{BesselJ[0, z], BesselJ[2, z], BesselJ[4, z]}], {z, 0, 10}, PlotLabel->TraditionalForm[{BesselJ[0, z], BesselJ[2, z], BesselJ[4, z]}]`——`BesselJ[4, z]}]` 处的 `]` 提前闭合了 Plot，使其后的 `{z, 0, 10}` 落在括号外，且末尾缺一个 `]`。

## 现象二：正文 n 值列表残缺

「将产生贝塞尔函数 J_n(z) 关于 n = 0, 2, 4 = l, 3, 的图形」——「= l, 3,」不通。

## 拟校改

- In[1] 应为 `bj0 = Plot[{BesselJ[0, z], BesselJ[2, z], BesselJ[4, z]}, {z, 0, 10}, PlotLabel->TraditionalForm[{BesselJ[0, z], BesselJ[2, z], BesselJ[4, z]}]]`（与 In[2] 的平行结构对勘可无歧义复原）。
- 正文应为「关于 n = 0, 2, 4 **和** n = **1**, 3, **5** 的图形」：l 为 1 之讹，且脱「和」与「5」（与 In[1]/In[2] 分别绘制偶数阶与奇数阶两组互证）。

## 状态

复原方案已写入 [[式20-44a-b贝塞尔函数绘图复算]] 并复算通过；待核对原书 PDF 定谳。总目：[[20-4全节系统性转写讹误清单]]。