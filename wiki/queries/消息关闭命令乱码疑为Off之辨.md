---
type: query
title: "消息关闭命令乱码疑为 Off[s::tag] 之辨"
tags: [讹误, 乱码还原, Off, On, 消息系统, Mathematica]
related: [10-数学手册原书第10版--17-20210-关于句法信息消息的补充--1xj9llw, 消息系统（Mathematica）, 20-2-10全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# 消息关闭命令乱码疑为 Off[s::tag] 之辨

**状态：高置信度还原，待回查原书。** 本节转写文本中，消息开关一段作：

> 使用 $0 \mathbf{f} \mathbf{f} \left[ s \mid : tag \right]$ 用户可以关掉一条消息换成 On 该消息将再次出现．

「$0\mathbf{f}\mathbf{f}[s|:tag]$」为数学排版乱码。还原为 Off[s::tag] 的依据：

1. 下句「换成 On 该消息将再次出现」表明所缺命令与 On[s::tag] 成对，即 Off[s::tag]；
2. [[concepts/消息系统（Mathematica）]] 的 Off/On 语义与此完全吻合；
3. 乱码形态「0ff」与「Off」（O 讹作 0、逐字符数学斜体化）、「s|:tag」与「s::tag」（竖线为冒号之讹）字形相合。

结论：暂按 Off[s::tag] 记写于 [[concepts/消息系统（Mathematica）]]；回查原书确认后销号。总汇见 [[queries/20-2-10全节系统性转写讹误清单]]。