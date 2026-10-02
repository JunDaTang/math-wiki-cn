---
type: query
title: "GaussianIntegers 例脱方括号之辨"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 疑辨, 因式分解, 转写讹误]
related: [高斯整数上的因式分解, 因式分解与多项式运算算例复算, 20-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---

# GaussianIntegers 例脱方括号之辨

## 疑点

20.3.1.2 高斯整数因式分解例转写为：

```
In[1] := Factor[x² - 2x + 5] → Out[1] = 5 - 2x + x²,
In[2] := FactorGaussianIntegers -> True
Out[2] = (-1 - 2I + x)(-1 + 2I + x)
```

In[2] 行脱 Factor 的方括号与被处理表达式；正文「那么这可以通过选择 Gaussianintegers 而得到」表述亦不完整（选项名大小写亦讹）。

## 重构假设

In[2] 疑为：

```
In[2] := Factor[x² - 2x + 5, GaussianIntegers -> True]
```

复算验证该输出成立（判别式 4−20 = −16，根 1±2i），见 [[findings/因式分解与多项式运算算例复算]]。

## 关联

[[concepts/高斯整数上的因式分解]]、[[queries/20-3全节系统性转写讹误清单]]。