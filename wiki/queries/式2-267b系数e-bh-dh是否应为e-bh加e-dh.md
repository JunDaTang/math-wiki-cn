---
type: query
title: "式 2.267b 的系数 e^(bh+dh) 是否应为 e^(bh)+e^(dh)？"
created: 2026-09-29
updated: 2026-09-29
tags: [经验公式, 转写讹误, 指数和, 数学手册]
related: [指数和, 指数和的两级修正, 修正]
sources: ["数学手册(原书第10版)/2.16 经验曲线的确定.md"]
---
# 式 2.267b 的系数 e^(bh+dh) 是否应为 e^(bh)+e^(dh)？

手册 2.16.2.11 给出的指数和一级修正为（按转写字面）

$$Y=\frac{y_2}{y}=(\mathrm{e}^{bh+dh})X-\mathrm{e}^{bh}\mathrm{e}^{dh},\qquad X=\frac{y_1}{y},$$

其中 x 成公差 h 的等差数列，$y, y_1, y_2$ 为已知函数的任意三个连续值。斜率系数 $\mathrm{e}^{bh+dh}$ 是否应为 $\mathrm{e}^{bh}+\mathrm{e}^{dh}$？

## 支持订正的证据（推导矛盾）

等差采样下，序列 $y_i=a\mathrm{e}^{bx_i}+c\mathrm{e}^{dx_i}$ 满足二阶线性递推（特征根 $\mathrm{e}^{bh},\mathrm{e}^{dh}$）：

$$y_2=(\mathrm{e}^{bh}+\mathrm{e}^{dh})\,y_1-\mathrm{e}^{bh}\mathrm{e}^{dh}\,y,$$

可用 $y=2^x+3^x$ 数值验证。两边除以 y 得

$$Y=(\mathrm{e}^{bh}+\mathrm{e}^{dh})X-\mathrm{e}^{bh}\mathrm{e}^{dh}.$$

若按转写字面取斜率 $\mathrm{e}^{bh+dh}$，该恒等式不成立。故疑为“$\mathrm{e}^{bh}+\mathrm{e}^{dh}$”的上标粘连转写讹误，与本 wiki 已记录的 [[queries/式2-206的icot-iz是否为i-cot-iz粘连]] 同类；亦不排除原版即误。

## 待办

- 对照原版（Bronstein/Semendjajew 德文版或英文版）相应公式确认系数。
- 若原版即误，应在来源页记录为原版讹误而非转写引入。

## 关联

- [[findings/指数和的两级修正]]（本式所在 finding，含二级修正 2.267c 的验证）
- [[concepts/指数和]]