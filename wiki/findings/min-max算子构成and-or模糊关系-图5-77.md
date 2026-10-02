---
type: finding
title: "极小值/极大值算子构成 AND/OR 模糊关系（图 5.77）"
tags: [模糊推理, 模糊关系, min算子, max算子, AND, OR]
related: [findings/zadeh算子与and-or-not对应, concepts/柱面扩充, concepts/t-范数, concepts/s-范数, comparisons/同论域聚合与跨论域关系复合比较, methodology/柱面扩充与and-or复合构造流程, queries/5-9-4全节系统性转写讹误清单]
created: 2026-09-30
updated: 2026-09-30
source: "[[sources/10-数学手册原书第10版--12-594-模糊推理近似推理--2acbbg]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/5.9.4 模糊推理(近似推理).md"]
---
# 极小值/极大值算子构成 AND/OR 模糊关系（图 5.77）

**断言**（《数学手册(原书第10版)》5.9.4，第 594 页，逐字转录）：在柱面扩充（图 5.76）之后，

```
AND（和）: μ_R(p, T) = min{μ₁(p), μ₂(T)}
OR（或）:  μ_R(p, T) = max{μ₁(p), μ₂(T)}
```

即用**极小值算子**复合「中等压力 AND（和）高温」，用**极大值算子**复合「OR（或）」，图 5.77 给出图形结果。

## 证据与核验状态

- **交叉印证（replicated: true）**：min=AND、max=OR 的算子对应在 5.9.2 已独立陈述（式 5.350–5.351、表 5.9，见 [[findings/zadeh算子与and-or-not对应]]、[[concepts/t-范数]]、[[concepts/s-范数]]）；5.9.4 把它从同论域聚合推广到跨论域关系复合，两节相互印证。
- 公式自洽：μ_R 是 min/max 对柱面扩充后的两个隶属函数逐点作用。
- **图示内容未复算**：图 5.77 的像素内容无法核验。

## 转写疑点

正文先称「5.77(a) 给出形成模糊关系的图形结果」，随后 min-AND 与 max-OR 两处均标「图 5.77(b)」，而转录仅含两幅 5.77 图像——分图编号与文字描述不一致（真实分图应为 (a)/(b) 还是 (a)/(b)/(c)？），见 [[queries/5-9-4全节系统性转写讹误清单]]。另有 μ_R(p T) 逗号脱落、「｝」多余。