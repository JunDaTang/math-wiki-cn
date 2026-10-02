---
type: concept
title: 符号属性（Mathematica）
tags: [Mathematica, Attributes, Orderless, Protected, Locked, Protect, Unprotect]
related: [mathematica, Set指派与清除, 语境与符号全名（Mathematica）, 信息查询（Mathematica）]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# 符号属性（Mathematica）

符号属性（Attributes）是 Mathematica 中可对符号指定的一类一般性质：符号除按其定义具有的性质外，还可以被指定若干附加的「属性」，用以约束或改变对该符号的定义与改写行为。本主题与 [[concepts/语境与符号全名（Mathematica）]] 同出 20.2.10.1 小节，共同构成对符号的一般管理机制。

## 本节列出的属性

| 属性 | 语义 |
|---|---|
| Orderless | 无序的、可交换的 |
| Protected | 不能更改的值 |
| Locked | 不能改变的属性 |

原书以「等等」收束——属性族不止此三种。

## 查询与设置

| 命令 | 语义 |
|---|---|
| Attributes[symbol] | 得到所考虑对象现有属性的有关信息 |
| Protect[symbol] | 保护符号：此后不能对该符号引入任何其他定义（即置 Protected） |
| Unprotect[symbol] | 除去上述保护属性 |

## 与相关机制的关系

- Protected 与 [[concepts/Set指派与清除]] 的指派机制相衔接：受保护符号拒绝新的定义指派，Protect/Unprotect 构成该限制的开关。（按 Mathematica 通行语义，内置符号通常处于 Protected 状态——此为独立可查证背景，本节未明言。）
- 语境决定符号的「归属」，属性决定符号的「行为约束」，二者并列构成符号级管理；对对象信息的查询手段见 [[concepts/信息查询（Mathematica）]]。

## 转写注记

「Attributes[!]」之「!」疑为符号名占位脱失（原书或作 Attributes[symbol] 之类）；「属千」「对千」等为千/于 系统性互讹。详见 [[queries/20-2-10全节系统性转写讹误清单]]。