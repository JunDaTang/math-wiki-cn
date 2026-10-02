---
type: concept
title: 语境与符号全名（Mathematica）
tags: [Mathematica, 语境, Context, 符号全名, 命名空间, 程序包, 同名遮蔽]
related: [mathematica, Mathematica符号命名规则, Set指派与清除, Mathematica标准函数, 消息系统（Mathematica）]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
---
# 语境与符号全名（Mathematica）

语境（Context）是 Mathematica 的符号命名空间机制：任何一个符号的完整名称都由「语境 + 短名称」两部分构成，二者以反引号相连。语境携带符号所属程序部分（程序模块、程序包或用户会话）的名称；引入这一层的动机是：Mathematica 必须处理大量符号，其中有一些要用于请求进一步加载的程序模块，为避免模棱两可，符号名称须由两部分组成。

## 全名的构成

- 短名称：表达式的头与元素的名称（「头」之概念见 [[concepts/Part（部件提取与头）]]），其拼写规则见 [[concepts/Mathematica符号命名规则]]（20.2.1）。
- 语境：为命名一个符号，Mathematica 需确定该符号所属的程序部分，这一归属即由语境给出。
- 完整名称 = 语境 + 反引号 + 短名称，如 `` Global`f ``、`` System`Log ``。

## System` 与 Global`

Mathematica 启动时即有两个语境出现：

- `` System` ``：所有内置函数所属的语境，为 [[concepts/Mathematica标准函数]] 补上语境归属注脚；
- `` Global` ``：由用户定义的函数所属的语境。

当一个语境得以实现（相应程序部分被加载）后，其中的符号就能被其短名称所指称。

## 语境查询与程序包加载

| 命令 | 语义 |
|---|---|
| Contexts[] | 得到有关其他可用程序模块（语境）的信息 |
| `<<NamePackage` | 读入另一个 Mathematica 程序模块；相应语境被打开并引入先前的列表 |

## 同名遮蔽与消解

加载新模块之前若已以某名称引入一个符号，而新近打开的语境中相同名称伴随另一个定义出现，Mathematica 将对用户发出警告。消解有二途：

1. ``Remove[Global`name]``：擦去先前定义的名称（彻底移除，与 Clear 的强度差异见 [[comparisons/Remove与Clear比较]]）；
2. 对新近载入的符号改用其完整名称指称。

遮蔽警告经 [[concepts/消息系统（Mathematica）]] 呈现。

## 转写注记

- 本节转写将语境分隔反引号一律讹作撇号「'」（System'、Global'、Remove [Global'name]），且「启动时总是有两个语境出现 System' Global'」为简化表述——按 Mathematica 通行语义（独立可查证背景），会话当前语境 $Context 为 `` Global` ``，`` System` `` 位于语境搜索路径 $ContextPath 之中。见 [[queries/System与Global撇号疑为反引号之辨]]。
- `<<NamePackage` 之程序包名疑脱语境分隔反引号（或为 ``<<Name`Package``）。
- 其余讹误（「使用命Contexts[]」脱「令」、「对千巾」疑为「对于以」等）见 [[queries/20-2-10全节系统性转写讹误清单]]。