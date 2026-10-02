---
type: query
title: 式 2.231c 的「tan xPOx」是否漏排角符号（应为 tan∠POx）？
created: 2026-09-29
updated: 2026-09-29
tags: [转写疑点, 环索线, 参数方程]
related: [环索线, 三阶代数曲线]
sources: ["数学手册(原书第10版)/2.11 三阶(三次)曲线.md"]
---

# 式 2.231c 的「tan xPOx」是否漏排角符号（应为 tan∠POx）？

## 疑点

[[concepts/环索线]] 的参数方程 (2.231c) 在源 markdown 中写作

$$
t = \tan\,\mathrm{x}POx
$$

而同节平行的两处参数方程——笛卡儿叶形线 (2.227b) 与蔓叶线 (2.228b)——均写作 $t = \tan\angle POx$。

## 内部证据

- 在 (2.231c) 的参数式下，$\dfrac{y}{x} = t$，即 $t$ 恰为射线 $OP$ 与 $x$ 轴夹角的正切，与 $\angle POx$ 的语义一致。
- (2.231c) 的适用范围 $-\infty < t < \infty$ 与角度型参数一致。

## 待决问题

- `xPOx` 是否为 `∠POx` 在转写过程中丢失角符号后的残留？
- 应径直修正源 markdown，还是保留 [sic] 并加注？
- 可对勘原版书确认原始排版（见 REVIEW 建议）。

## 关联

- [[findings/环索线的三重表示与几何定义]]
- [[sources/10-数学手册原书第10版--10-211-三阶三次曲线--nch2ec]]