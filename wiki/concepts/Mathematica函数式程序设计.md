---
type: concept
title: Mathematica 函数式程序设计
tags: [mathematica, 函数式程序设计, nest, nestwhile, apply, map, mapthread, distribute, total]
related: [concepts/纯函数（Mathematica）, concepts/Table-Range-Array列表生成命令, concepts/Mathematica标准函数, concepts/Do与While循环, concepts/Module与局部变元, entities/mathematica, findings/例B-函数式sumq与Total复算, comparisons/过程式与函数式sumq实现比较, queries/Total版十位结果逐位相同之辨]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
---
# Mathematica 函数式程序设计

函数式程序设计指以 `Nest`、`NestWhile`、`Apply`、`Map`、`MapThread`、`Distribute`「和另外一些运算」为骨干、经由函数作用于表达式与列表整体来构造程序的程序设计风格。《数学手册（原书第10版）》20.2.9 称 Mathematica 程序设计功能的「真正力量」首先在于使用函数方法。本来源仅列举这些运算之名（`Apply` 除外，见例 B），未逐一给出算例，故各运算的语义不据本页推断。

## 例 B：函数式改写 sumq

对于要求有十位精确数字的情形，可将例 A 的过程式 `sumq` 写成：

```
sumq[n_] := N[Apply[Plus, Table[Sqrt[i], {i, 1, n}]], 10]
```

`sumq[30]` 的结果为 112.0828452（复算验证见 [[findings/例B-函数式sumq与Total复算]]）。原文又称

```
Total[Sqrt[N[Range[n], 10]]]
```

给出相同的结果，而「不使用下标，不连续递增其值，也无须变元 sum 及其初始值」——即摆脱了 `Do` 式的下标递增（[[concepts/Do与While循环]]）与 `Module` 式的局部累加变元（[[concepts/Module与局部变元]]）。

## 要点与保留

- 原文「十位精确数字」与 `N[..., 10]` 的实际语义（10 位**有效数字**）措辞略含混，属翻译措辞问题而非计算错误；
- `Total` 版走逐项 10 位精度的数值路径，与 `N[精确和, 10]` 是否逐位相同需实测，原文「相同」之说偏强（[[queries/Total版十位结果逐位相同之辨]]）；
- 例 B 复用 [[concepts/Table-Range-Array列表生成命令]]（`Table`、`Range`）与 [[concepts/Mathematica标准函数]]（`Sqrt`、`N`、`Plus`）；
- 与 [[concepts/纯函数（Mathematica）]] 同属函数式主题：后者提供无名函数记法，本页诸运算则作用于表达式与列表。