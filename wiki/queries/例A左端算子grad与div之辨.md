---
type: query
title: 例 A 左端算子 grad 与 div 之辨
created: 2026-10-01
updated: 2026-10-01
tags: [勘误, 考据, 向量分析, 数学手册]
related: [梯度算子的运算法则, 梯度算子, 13-2-6全节系统性转写讹误清单, 式13-67至13-71c梯度算子与运算法则转录复算]
sources: ["数学手册(原书第10版)/13.2.6 梯度算子和拉普拉斯算子.md"]
---

# 例 A 左端算子 grad 与 div 之辨

## 问题

13.2.6.2 例 A 的最左端算子究竟应是 grad 还是 div？译者注「原文将此式最左端的 grad 误为 div」所作的「更正」是否本身即为误改？

## 现状（转写文本）

$$\operatorname{grad}(U\vec V) = \nabla(U\vec V) = \nabla(\overset{\downarrow}{U}\vec V) + \nabla(U\overset{\downarrow}{\vec V}) = \vec V\cdot\nabla U + U\,\nabla\cdot\vec V = \vec V\cdot\operatorname{grad}U + U\operatorname{div}\vec V.$$

脚注（OCR 有搅乱，作「叩……译者注■」）：「原文将此式最左端的 grad 误为 div。译者注」

## 类型检验（支持 div）

右端 $\vec V\cdot\operatorname{grad}U + U\operatorname{div}\vec V$ 为**标量**，故左端必须是 $\operatorname{div}(U\vec V)$——标准乘积法则

$$\operatorname{div}(U\vec V) = \vec V\cdot\operatorname{grad}U + U\operatorname{div}\vec V$$

恰好成立。反之，若左端为 $\operatorname{grad}(U\vec V)$（标量×向量的并向量型梯度），其结果应为张量/并矢，与标量右端类型不符。转写中间步骤 $\vec V\cdot\nabla U + U\,\nabla\cdot\vec V$ 中出现的显式点乘，亦与 div 读法一致。

## 两种可能

1. **译者误改**：若译者确实把原书的 div「更正」为 grad，则该更正本身疑为误改——原书（div）反而是对的，与标准乘积法则一致。
2. **OCR 搅乱**：转写或脚注文字被搅乱（脚注已确认有 OCR 噪声「叩……■」），实际印文或与转写不同。

## 状态与待办

- [ ] 核对中文纸质书例 A：左端印作 grad 还是 div？脚注原文如何？
- [ ] 必要时核对德文原书（Bronstein 系手册）对应条目。
- 关联：[[queries/13-2-6全节系统性转写讹误清单]] 第 8 项；复算记录 [[findings/式13-67至13-71c梯度算子与运算法则转录复算]]。