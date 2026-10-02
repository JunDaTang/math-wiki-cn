---
type: query
title: 式 17.13c 中 rank 疑为 tr 之辨
tags: [勘误, 刘维尔公式, 朗斯基行列式]
related: [基解矩阵与朗斯基行列式, 刘维尔, 式17-13a至17-13d线性方程组与常数变易法转录复算, 17-1-2全节系统性转写讹误清单]
created: 2026-10-01
updated: 2026-10-01
sources: ["数学手册(原书第10版)/17.1.2 常微分方程的定性理论.md"]
---
# 式 17.13c 中 rank 疑为 tr 之辨

## 现象

式 (17.13c) 转录为 $\dot W(t)=\operatorname{rank}A(t)\,W(t)$，其中 $W=\det\varPhi$ 为朗斯基行列式。

## 论证（疑为 tr）

1. **数学正确性**：刘维尔公式的标准形式是 $\dot W=\operatorname{tr}A(t)\cdot W$。对 $\varPhi=(\varphi_1,\dots,\varphi_n)$，$\dot W=\sum_i\det(\dots,\dot\varphi_i,\dots)=\operatorname{tr}A\cdot W$。若按 rank 理解，rank 取整值且一般不随 $t$ 连续，无法给出 $W$ 的连续增长律，公式错误。
2. **内部印证**：同节式 (17.17) 使用 $\exp(\int_0^T\operatorname{Tr}Df\,\mathrm{d}t)$ 表述乘子乘积，与迹口径一致；两式应同源。
3. **转写来源**：本手册转写自德文原书（表 17.1 残留 "oder"），德文迹记号为 "Sp"（Spur），"rank" 疑为其转写讹误。

## 待办

对照原书确认；确认前，wiki 中引用式 (17.13c) 一律按 $\operatorname{tr}$ 口径并注明。这是本节最重要的数学性疑误。