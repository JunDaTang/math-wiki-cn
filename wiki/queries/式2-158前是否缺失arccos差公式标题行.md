---
type: query
title: 式 2.158 前是否缺失「arccos x − arccos y =」标题行？
tags: [转写勘误, 式2-158, 反余弦函数, 和差公式]
related: [10-数学手册原书第10版--11-28-测圆或反三角函数--1yi9enf, arcsin与arccos的和差公式, 反余弦函数, 式2-146条件π减1是否应为负1, 式2-155与2-156编号及条件行错乱如何复原]
created: 2026-09-29
updated: 2026-09-29
sources: ["数学手册(原书第10版)/2.8 测圆或反三角函数.md"]
---

# 式 2.158 前是否缺失「arccos x − arccos y =」标题行？

## 现象

手册 2.8.6 节中，式 2.157（arccos 的和）之后直接出现两个**无主语**的分支：

$$= - \arccos \left(x y + \sqrt{1 - x^{2}} \sqrt{1 - y^{2}}\right) \quad (x \geqslant y) \tag{2.158a}$$

$$= \arccos \left(x y + \sqrt{1 - x^{2}} \sqrt{1 - y^{2}}\right) \quad (x < y) \tag{2.158b}$$

差公式的等式左端在转写文本中丢失。

## 论证

由主值域可推断缺失的左端应为 $\arccos x-\arccos y$：设 $\alpha=\arccos x$、$\beta=\arccos y$，则 $\cos(\alpha-\beta)=xy+\sqrt{1-x^{2}}\sqrt{1-y^{2}}$；因 arccos 递减，$x\geqslant y$ 时 $\alpha-\beta\leqslant0$，故取 $-\arccos(\cdots)$ 分支（2.158a），$x<y$ 时取正分支（2.158b）。该复原在边界点核验通过，且与 2.8 节其他差公式的版式（先给左端再给分支）一致。

## 待办

对照原书核实式 2.158 前是否确有「$\arccos x-\arccos y=$」一行；在此之前 [[arcsin与arccos的和差公式]] 中按复原后的完整等式登记并已注明。

## 关联

与 [[式2-146条件π减1是否应为负1]]、[[式2-155与2-156编号及条件行错乱如何复原]] 同属 2.8 节转写疑误群。