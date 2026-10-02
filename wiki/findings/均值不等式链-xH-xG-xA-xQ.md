---
type: finding
title: "两正数的均值不等式链 a < x_H < x_G < x_A < x_Q < b"
created: 2026-09-29
updated: 2026-09-29
tags: [均值, 不等式]
related: [算术平均值, 几何平均值, 调和平均值, 二次均值, 四种均值的大小关系]
sources: ["数学手册(原书第10版)/1.2 有限级数.md"]
source: "[[10-数学手册原书第10版--7-12-有限级数--2sdpdk]]"
confidence: high
replicated: null
---

# 两正数的均值不等式链 a < x_H < x_G < x_A < x_Q < b

手册 1.2.5.5 指出，对两个正数 $a, b$，取 $x_{\mathrm{A}} = \frac{a+b}{2}$、$x_{\mathrm{G}} = \sqrt{ab}$、$x_{\mathrm{H}} = \frac{2ab}{a+b}$、$x_{\mathrm{Q}} = \sqrt{\frac{a^2+b^2}{2}}$，则：

- 若 $a < b$：$a < x_{\mathrm{H}} < x_{\mathrm{G}} < x_{\mathrm{A}} < x_{\mathrm{Q}} < b$（式 1.69a）；
- 若 $a = b$：$a = x_{\mathrm{A}} = x_{\mathrm{G}} = x_{\mathrm{H}} = x_{\mathrm{Q}} = b$（式 1.69b）。

## 证据与验证状态

- 证据类型：直接陈述。手册以编号公式给出，体例上不给证明。
- 本源内无推导；该结果是标准均值不等式（AM–GM–HM–RMS）的两数情形，正确性可独立验证。
- 本页入库时的数值抽查（直接代入，非本源内容）：$a=1, b=4$ 时 $x_{\mathrm{H}} = 1.6 < x_{\mathrm{G}} = 2 < x_{\mathrm{A}} = 2.5 < x_{\mathrm{Q}} = \sqrt{8.5} \approx 2.915$，次序符合 (1.69a)。
- 适用范围：手册仅对**两个正数**陈述；n 个数的一般形式未在本节给出。

## 关联

四种均值的定义与特征对照见 [[comparisons/四种均值的大小关系]]；各均值概念页：[[concepts/算术平均值]]、[[concepts/几何平均值]]、[[concepts/调和平均值]]、[[concepts/二次均值]]。
