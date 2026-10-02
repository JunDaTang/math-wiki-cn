---
type: comparison
title: Remove与Clear比较
tags: [Mathematica, Remove, Clear, 符号管理, 同名遮蔽]
related: [Set指派与清除, 语境与符号全名（Mathematica）, mathematica]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# Remove与Clear比较

本比较综合两处来源：Remove 的语义来自本页所附来源（20.2.10，专用于消解同名遮蔽）；Clear 的语义来自 20.2.3 节的 [[concepts/Set指派与清除]]（见 [[sources/10-数学手册原书第10版--9-2023-重要算子--ztnien]]）。

| 维度 | ``Remove[Global`name]`` | Clear[name] |
|---|---|---|
| 出处 | 20.2.10 语境一节 | 20.2.3 重要算子一节 |
| 原书表述 | 「可以擦去先前定义的名称」——彻底移除符号 | 清除已指派的值与定义（详见该概念页） |
| 典型用途 | 消解加载程序包后的同名遮蔽 | 清除指派以便重新定义 |
| 配套机制 | [[concepts/语境与符号全名（Mathematica）]]（以全名指称新符号为替代消解方案） | [[concepts/Set指派与清除]] |

按 Mathematica 通行语义（独立可查证背景）：Clear 清除符号的值与定义但保留符号本身，Remove 则将符号从系统中彻底移除，使之如同从未定义过——原书两节未将二者并置比较，此强度差异为背景补充，供遮蔽消解场景下选择操作时参考。