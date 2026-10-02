---
type: query
title: "「整数写作 mm 的形式」疑为「写作 nnn. 的形式」之辨"
tags: [勘误, Mathematica, 尾部小数点, Real 类型]
related: [20-2-2全节系统性转写讹误清单, Mathematica数的四种基本类型]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# 「整数写作 mm 的形式」疑为「写作 nnn. 的形式」之辨

问：20.2.2.1 节「如果一个整数 nnn 写作 mm 的形式则 Mathematica 将其看成一个浮点数，即 Real 类型的数」中，「mm」是否为「nnn.」（尾部小数点形式）之讹？

## 支持「nnn.」读法的证据

1. 论旨衔接：本句结论是「整数被看成 Real 类型的浮点数」，而 `mm` 不含小数点，无法触发该结论；带尾部小数点的 `nnn.` 恰使整数落入 Real 的输入模式。
2. 同节算例直接佐证：`Head[51.] = Real`、`IntegerQ[2.] = False`，均为「尾部小数点」规则的演示（复算见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]]）。
3. 表 20.1 中 Real 的输入形式为 `nnnn.mmmm`，小数点是 Real 输入的判别特征。

## 待办

- 对照原书 PDF 确认原字样（不排除其他形近讹变）。

## 影响

采信「nnn.」读法不影响任何数值结论；维持「mm」读法则该句不可解。相关知识见 [[concepts/Mathematica数的四种基本类型]]。