---
type: query
title: 「可以用函数方式将例 写成」脱「A」之辨
tags: [转写校勘, 脱字, mathematica]
related: [queries/20-2-9全节系统性转写讹误清单, findings/例B-函数式sumq与Total复算, comparisons/过程式与函数式sumq实现比较, sources/10-数学手册原书第10版--9-2029-程序设计--l13hq7]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
---
# 「可以用函数方式将例 写成」脱「A」之辨

**问题**：例 B 题面作「对于要求有十位精确数字的情形，可以用函数方式将例 写成」，「例」后脱字。

**拟断**：脱「A」，即「将例 A 写成」。证据：例 B 之 `sumq[n_] := N[Apply[Plus, Table[Sqrt[i], {i, 1, n}]], 10]` 与例 A 之过程式 `sumq` 同名同任务（Σ_{i=1}^n √i），显系对例 A 的函数式改写；且本节在先者仅例 A 一例。