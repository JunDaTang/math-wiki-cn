---
type: query
title: "In[3] 之「=」疑为「:=」之辨"
created: 2026-10-02
updated: 2026-10-02
tags: [数学手册, 校勘, mathematica, SetDelayed, 牛顿法]
related: [10-数学手册原书第10版--9-2028-函数运算--arihlh, 20-2-8全节系统性转写讹误清单, Set指派与清除, 延迟赋值（SetDelayed与RuleDelayed）]
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# In[3] 之「=」疑为「:=」之辨

## 现象

20.2.8 (6) 牛顿法算例的第三行输入，源文作：

```
In[3] =  g[x_] := x - f[x]/f′[x]
```

而同算例的 In[1]、In[2]、In[4]、In[5] 及本节其余所有会话行均作 `In[n] :=`。

## 两解

- **读作 `In[3] :=`（倾向此解）**：Mathematica 记录输入行的标准形式即 `In[n] := expr`；行内 `g[x_] := …` 本身用的是延迟赋值 SetDelayed（见 [[concepts/Set指派与清除]]、[[concepts/延迟赋值（SetDelayed与RuleDelayed）]]），与其前后各行完全平行。「=」当为「:=」脱冒号之讹。
- **按字面读 `In[3] =`**：则是对 `In[3]` 施行即时赋值 Set，与本节文意（定义牛顿迭代函数 g）不合，且未见 Mathematica 如此用法。

## 待决

需纸本核对原书该行；核对前，转录一律校作 `In[3] := g[x_] := x - f[x]/f′[x]` 并加注（见 [[findings/牛顿法NestList-FixedPoint求根算例复算]]、[[queries/20-2-8全节系统性转写讹误清单]]）。