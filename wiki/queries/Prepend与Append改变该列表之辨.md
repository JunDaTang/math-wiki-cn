---
type: query
title: "Prepend 与 Append「改变该列表」之辨"
created: 2026-10-02
updated: 2026-10-02
tags: [Mathematica, Prepend, Append, 语义校勘]
related: [列表运算命令, 10-数学手册原书第10版--7-2024-列表--9o5vl4]
sources: ["数学手册(原书第10版)/20.2.4 列表.md"]
---

# Prepend 与 Append「改变该列表」之辨

## 疑点

表 20.4 将 `Prepend[l, a]`、`Append[l, a]` 分别释为「将 a 添加到前面／末尾**改变该列表**」。而按 Mathematica 实际语义，二者返回添加元素后的**新**列表，并不就地修改 l；就地修改须用 PrependTo／AppendTo。「改变该列表」的措辞有误导为就地修改之嫌。

## 可能解释

1. 原书（德文）表述意为「得到改变了的列表」，中译转写措辞引发就地修改的误读；
2. 原书确有就地修改之意，则与 Mathematica 语义不符；
3. 转写脱字（如「改变后的该列表」）或脱文。

## 裁定路径

实测：`l = {1, 2}; Append[l, 3]` 之后 l 的值（按实际语义应仍为 {1, 2}）；再核对原书措辞。结论回填 [[列表运算命令]]。