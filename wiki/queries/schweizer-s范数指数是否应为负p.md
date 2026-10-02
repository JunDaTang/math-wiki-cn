---
type: query
title: "Schweizer s 范数指数是否应为负 p？"
tags: [t-范数, s-范数, Schweizer, 转写讹误]
related: [t-范数, s-范数, 表5-8十二对范数族与序链]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.9.2 模糊集的连接(聚合).md"]
---
# Schweizer s 范数指数是否应为负 p？

## 问题

表 5.8 Schweizer 行的 s 范数

s_s(x,y) = 1 − max{0, (1−x)^{−p} + (1−y)^p − 1}^{−1/p}

中第二项 (1−y) 的指数是否应为 **−p**？

## 证据

- 同行 t 范数 t_s(x,y) = max{0, x^{−p} + y^{−p} − 1}^{−1/p} 两项指数均为 −p，s_s 中仅第二项为 +p，不对称；
- 按通行对偶关系 s(x,y) = 1 − t(1−x, 1−y)（源文未显式给出），应有 s_s(x,y) = 1 − max{0, (1−x)^{−p} + (1−y)^{−p} − 1}^{−1/p}；
- 表 5.8 其余各族（s_b、s_a、s_ds、s_h、s_e、s_f、s_ya、s_w、s_do、s_du）经同一检验全部与对偶式一致，Schweizer 是唯一例外——支持「转写讹误」而非「不同约定」的解释。

## 影响范围

仅 Schweizer 的 s_s；t_s 与其他族不受影响。

## 核实途径

对照原书（德文版）表 5.8，或 Schweizer 族的通行定义；查证后在本页记录结论。