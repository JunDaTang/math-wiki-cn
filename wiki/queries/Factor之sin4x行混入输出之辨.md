---
type: query
title: "Factor 之 Sin[4x] 行混入输出之辨"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 疑辨, 三角变换, 转写讹误]
related: [三角与复数变换命令, 20-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---

# Factor 之 Sin[4x] 行混入输出之辨

## 疑点

20.3.1.5 三角变换算例块中：

```
In[2] := Factor[sin[4x], Trig-> True] - 8Cos[x]³Sin[x] + 4Cos[x]Sin[x]
Out[2] = 0
```

存在三重问题：

1. 输入行混入了形似输出的表达式「−8Cos[x]³Sin[x] + 4Cos[x]Sin[x]」；
2. 函数名小写「sin」不合 Mathematica 内建函数首字母大写的约定；
3. 若输入确为 Factor[Sin[4x], Trig->True]，输出不应为 0。

## 重构假设

由恒等式 Sin[4x] = 8Cos[x]³Sin[x] − 4Cos[x]Sin[x]（推导：4 sinx cosx·cos2x = 2 sin2x cos2x = sin4x），输入疑为

```
Factor[Sin[4x] - 8Cos[x]^3 Sin[x] + 4Cos[x]Sin[x], Trig -> True]
```

此时被因子化的表达式恒为零，Out[2] = 0 方可解释。

## 待辨

- 对原书影印件核对该行原始形态：是排版将输入与其后表达式并置，还是原书即如此。

## 关联

同算例块的 TrigExpand[Sin[2x]Cos[2y]] 与 Factor[Cos[5x], Trig->True] 两例均复算吻合（后者 = Cos[x](1−2Cos[2x]+2Cos[4x])），唯此行存疑。见 [[concepts/三角与复数变换命令]]、[[queries/20-3全节系统性转写讹误清单]]。