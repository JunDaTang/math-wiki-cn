---
type: query
title: 式 2.253 第一行 Arcosh 形式的符号配对是否失配？
created: 2026-09-29
updated: 2026-09-29
tags: [曳物线, 面积余弦函数, 勘误, 查询]
related: [曳物线, 面积余弦函数, 10-数学手册原书第10版--10-215-各种其他曲线--pzek1r]
sources: ["数学手册(原书第10版)/2.15 各种其他曲线.md"]
---

# 式 2.253 第一行 Arcosh 形式的符号配对是否失配？

## 问题

式 (2.253) 第一行作 $x = a\,\mathrm{Arcosh}\frac{a}{y} \pm \sqrt{a^2-y^2}$。由于主支 $\mathrm{Arcosh}\frac{a}{y} = \ln\frac{a+\sqrt{a^2-y^2}}{y}$ 内部已含「+√」，第一行按字面的符号配对与第二行 ln 形式不一致。是否漏排了 Arcosh 前的 ±？

## 证据

- **第二行（自洽）**：「+ 在内、− 在外」给出右支 $x = a\ln\frac{a+\sqrt{a^2-y^2}}{y} - \sqrt{a^2-y^2}$；「− 在内、+ 在外」给出左支 $x = a\ln\frac{a-\sqrt{a^2-y^2}}{y} + \sqrt{a^2-y^2} = -a\,\mathrm{Arcosh}\frac{a}{y} + \sqrt{a^2-y^2}$。
- **第一行（按字面）**：$a\,\mathrm{Arcosh}\frac{a}{y} + \sqrt{a^2-y^2} = a\ln\frac{a+\sqrt{a^2-y^2}}{y} + \sqrt{a^2-y^2}$，与第二行任何一支都不相等。
- **数值反例**（$a=1$、$y=0.5$）：字面「+√」给出 $x \approx 2.183$，而曲线上该高度右支 $x \approx 0.451$、左支 $x \approx -0.451$——字面取值不在曲线上。
- **重建**：正确形式应为 $x = \pm\left(a\,\mathrm{Arcosh}\frac{a}{y} - \sqrt{a^2-y^2}\right)$。

## 待办

对照德文原书第 10 版或英文版确认第一行是否漏排 Arcosh 前的 ±（或外层符号应为与内层相反的 ∓）。

相关：[[concepts/曳物线]]、[[concepts/面积余弦函数]]、[[findings/曳物线的方程与几何量]]。