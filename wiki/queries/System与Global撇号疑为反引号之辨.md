---
type: query
title: "System' 与 Global' 之撇号疑为反引号之辨"
tags: [讹误, 反引号, 撇号, System, Global, 语境, Mathematica]
related: [10-数学手册原书第10版--17-20210-关于句法信息消息的补充--1xj9llw, 语境与符号全名（Mathematica）, 20-2-10全节系统性转写讹误清单]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# System' 与 Global' 之撇号疑为反引号之辨

**状态：高置信度还原，待回查原书。** 本节转写将语境分隔符一律写作撇号「'」：System'、Global'、Remove [Global'name]。按 Mathematica 通行语义（独立可查证背景），完整符号名的语境与短名称以反引号「`」相连：`` System` ``、`` Global` ``、``Remove[Global`name]``——概念页 [[concepts/语境与符号全名（Mathematica）]] 已按反引号记写。

附带疑点：本节「Mathematica 启动时，总是有两个语境出现 System' Global'」为简化表述。严格而言（通行语义背景）：会话当前语境 $Context 为 `` Global` ``，`` System` `` 位于语境搜索路径 $ContextPath 之中；「启动即有两个语境」的说法把当前语境与搜索路径语境并列，未区分二者角色。

待办：回查原书确认原字样（反引号抑或撇号）及「两个语境」句的原表述；确认后销号并同步 [[queries/20-2-10全节系统性转写讹误清单]]。