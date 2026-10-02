---
type: concept
title: 消息系统（Mathematica）
tags: [Mathematica, 消息系统, Message, Off, On, Quiet, Messages, 警告, 错误]
related: [mathematica, 信息查询（Mathematica）, Mathematica输入输出行记法, 符号属性（Mathematica）, 算例A与B消息触发复算]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# 消息系统（Mathematica）

消息系统是 Mathematica 在计算期间产生并显示提示信息的统一机制：消息的呈现一律采取 symbol::tag 的形式（符号名、双冒号、标记），这一统一形式为事后指称某条消息提供了可能；消息既由系统在计算中激活并出于不同理由使用，也可以由用户自建。

## 消息的开关与重现

| 命令 | 语义 |
|---|---|
| Off[s::tag] | 关掉一条消息 |
| On[s::tag] | 换成 On，该消息将再次出现 |
| Quiet | 关掉所有的消息 |
| Messages[symbol] | 重新调用与名称为 symbol 的符号相关联的所有消息 |

## 两个触发算例

（复算见 [[findings/算例A与B消息触发复算]]；行记法见 [[concepts/Mathematica输入输出行记法]]。）

```txt
■ A: In[1] := f[x_] := 1/x; In[2] := f[0]
Power::infy: Infinite expression 1/0 encountered.
Out[2] = ComplexInfinity
```

```txt
■ B: In[1] := Log[3, 16, 25]
Log::argt: Log called with 3 arguments; 1 or 2 arguments are expected.
Out[1] = Log[3, 16, 25]
```

例 A 表明：警告发出后计算本身仍可执行（1/0 得 ComplexInfinity）；例 B 表明：参数数目不符时计算无法执行，Mathematica 对该表达式不能做任何事情，原样返回。二者构成警告型与错误型消息的后果对照，见 [[comparisons/警告消息与错误消息后果比较]]。

## 转写注记

本节转写将消息关闭命令讹作数学排版乱码「$0\mathbf{f}\mathbf{f}[s|:tag]$」，据下文「换成 On 该消息将再次出现」高置信度还原为 Off[s::tag]，见 [[queries/消息关闭命令乱码疑为Off之辨]]；两处「在例 中」脱例号、「包含 个自变量」脱「3」等其余讹误见 [[queries/20-2-10全节系统性转写讹误清单]]。