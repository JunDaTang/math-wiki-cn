---
type: finding
title: InverseFunction 与 InverseSeries 算例复算
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, InverseFunction, InverseSeries, 级数反演, 复算]
related: [InverseFunction与InverseSeries算例块归属之辨, 20-2-7未入库回指缺口]
sources: ["数学手册(原书第10版)/20.2.7 模式.md"]
source: "10-数学手册原书第10版--7-2027-模式--125ne2w"
confidence: high
replicated: true
---
# InverseFunction 与 InverseSeries 算例复算

对 20.2.7 节末算例块 ■ A–C 逐一复算。三例各自从 In[1] 起，为相互独立的会话算例；其与本节“模式”主题的归属问题另见 [[queries/InverseFunction与InverseSeries算例块归属之辨]]。复算方式为解析推演与标准语义核验，非实机执行。以下结论分别针对 InverseFunction 与 InverseSeries 本身，不外推至其他命令。

## 算例 A：InverseFunction[f][x] → f^{-1}[x]

`InverseFunction[f]` 表示函数 f 的符号逆函数；作用于 x 得 `f^{-1}[x]`（Mathematica 中显示为 `f^(-1)[x]`）。与原文 Out[1] 一致。

## 算例 B：InverseFunction[Exp] → Log

`InverseFunction[Exp]` 求值为 `Log`：Exp 的逆函数即 Log。与原文 Out[1] 一致。

## 算例 C：InverseSeries 级数反演公式推导验证

`Series[g[x], {x, 0, 2}]` 展开为

g(x) = g[0] + g'[0]·x + (g''[0]/2)·x² + O(x³)

记 g0 = g[0]、g1 = g'[0]、g2 = g''[0]，令 t = y − g0 = g1·x + (g2/2)·x²。级数反演解出

x = t/g1 − g2·t²/(2·g1³) + O(t³)

核验：代入 g1·(t/g1 − g2·t²/(2·g1³)) + (g2/2)·(t/g1)² = t − g2·t²/(2·g1²) + g2·t²/(2·g1²) + O(t³) = t + O(t³)，成立。将变量名换回 x（以 x 记逆函数的自变量），得

(x − g[0])/g'[0] − g''[0]·(x − g[0])²/(2·g'[0]³) + O[x − g[0]]³

与原文 Out[1] 完全一致，故算例 C 的反演公式在数学上成立。

## 限定与待验

- 复算为解析推导；实机 `InverseSeries` 对符号系数级数的**输出显示形式**（如 `g'[0]` 还是 `Derivative[1][g][0]`、余项 `O[x - g[0]]^3` 的书写）待实机核验。
- 本算例块在原文中与“模式”主题无文字衔接，或属未入库的 20.2.5/20.2.6；引用时应注明归属未定（见 [[queries/InverseFunction与InverseSeries算例块归属之辨]]、[[queries/20-2-7未入库回指缺口]]）。
