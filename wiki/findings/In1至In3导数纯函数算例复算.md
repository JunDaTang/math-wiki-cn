---
type: finding
title: "In[1]–In[3] 导数纯函数算例复算"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, Derivative, 纯函数, 转录, 复算]
related: [Mathematica函数运算与纯函数, Derivative微分算子]
source: "[[10-数学手册原书第10版--9-2028-函数运算--arihlh]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# In[1]–In[3] 导数纯函数算例复算

## 转录（verbatim）

```
In[1] := f[x_] := Sin[x] Cos[x]
In[2] := f′      →  Out[2] = Cos[#1]^2 - Sin[#1]^2 &
In[3] := %[x]    →  Out[3] = cos[x]^2 - sin[x]^2
```

（源文于 In[1] 行尾衍一「由」字，实为下句「由 In[2] := f′ 得 Out[2]」之首，转录时归位。）

## 复算

1. 解析求导：d/dx(Sin x · Cos x) = Cos x·Cos x + Sin x·(−Sin x) = Cos²x − Sin²x（即 cos 2x）——与 Out[2] 的函数体 `Cos[#1]^2 - Sin[#1]^2` 一致 ✓
2. Out[2] 为纯函数（`#1` 槽位 + `&` 终结符）；`%[x]` 将其施于 x，应得 `Cos[x]^2 - Sin[x]^2`，与 Out[3] 语义一致 ✓

复算通过，属直接证据（源文载完整会话）；复算为解析推演。

## 讹误注记

源文 Out[3] 写作小写 `cos[x]^2 - sin[x]^2`，与 Out[2] 的大写 `Cos/Sin` 不一致。Mathematica 内置函数首字母大写，小写 `cos` 不会被求值为余弦函数，故 Out[3] 应为 `Cos[x]^2 - Sin[x]^2`；此大小写之讹系转写所致抑或原书排版，待纸本核对（[[queries/20-2-8全节系统性转写讹误清单]] 第 9 条）。