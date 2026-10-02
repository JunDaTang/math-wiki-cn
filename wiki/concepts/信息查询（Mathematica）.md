---
type: concept
title: 信息查询（Mathematica）
tags: [Mathematica, 信息查询, 帮助系统, F1, SetDelayed]
related: [mathematica, Mathematica标准函数, 延迟赋值（SetDelayed与RuleDelayed）, 符号属性（Mathematica）, 消息系统（Mathematica）]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# 信息查询（Mathematica）

信息查询指 Mathematica 中获取「关于对象的基本性质的信息」的一族手段（20.2.10.2 小节）：以问号引导的查询语法、对特殊算子的查询，以及联机帮助键。

| 手段 | 语义 |
|---|---|
| ?symbol | 关于给定名称为 symbol 的对象的信息 |
| ??symbol | 关于该对象的详细信息 |
| ?模式* | 关于所有名称以某串打头的 Mathematica 对象的信息（通配列表；本转写此行整体脱失） |
| ?:= 等 | 获取特殊算子的信息——例如用 ?:= 得到关于 SetDelayed 算子的信息 |
| 光标 + F1 | 将光标置于单元中含所考虑对象符号处，接着按压 F1；原书称此为「最实用的一种做法」 |

?:= 一例直接关联 [[concepts/延迟赋值（SetDelayed与RuleDelayed）]]：SetDelayed 即延迟赋值算子 :=。可查询的对象既含 [[concepts/Mathematica标准函数]] 之内置函数，亦含用户自定义符号；按 Mathematica 通行语义（背景），查询结果中即含对象的 [[concepts/符号属性（Mathematica）]] 与关联 [[concepts/消息系统（Mathematica）]] 的消息一类信息。

## 转写注记

- 「？贮关千所有名称以 打头的 Mathematica 对象的信息」一行，通配查询模式整体脱失，「贮」为残留讹字，本页暂按 ?模式* 记写，原字样待回查；
- 「接着按压 Fl」之「Fl」疑为功能键「F1」。

详见 [[queries/20-2-10全节系统性转写讹误清单]]。