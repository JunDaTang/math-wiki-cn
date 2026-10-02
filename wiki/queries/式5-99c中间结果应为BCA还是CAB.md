---
type: query
title: "式 (5.99c) 中间三角形应为 △BCA 还是 △CAB？"
created: 2026-09-30
updated: 2026-09-30
tags: [转写讹误, 群表示, 勘误]
related: [d-3二面角群, d3群表与二维表示算例, 5-3-4全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/5.3.4 群表示.md"]
---

# 式 (5.99c) 中间三角形应为 △BCA 还是 △CAB？

**问题**：转写本 (5.99c) 为「S_A S_B(△ABC) = S_A(△CBA) = △CAB = R₁(△ABC)」，并由此得出 S_A·S_B = R₁。中间结果「△CAB」是否应为「△BCA」？

**证据**（本 wiki 逐步复算）：

1. S_B: A→C, B→B, C→A（式 5.99a），故 S_B(△ABC) = △CBA ✓（与转写一致）。
2. S_A: A→A, B→C, C→B，故 S_A(△CBA) = **△BCA**。
3. R₁: A→B, B→C, C→A，故 R₁(△ABC) = **△BCA** ✓。
4. 群表 (5.99d) 给 S_A·S_B = R₁（该表全部 36 项已独立核验，见 [[findings/d3群表与二维表示算例]]）。

若保留「△CAB」：R₂: A→C, B→A, C→B 给出 △CAB = R₂(△ABC)，与群表 S_A·S_B = R₁ 冲突。

**倾向复原**：△BCA（使第 2 步与结论同时自洽）。待原书影印本确认。