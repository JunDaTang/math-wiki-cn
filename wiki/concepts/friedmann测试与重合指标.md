---
type: concept
title: "Friedmann 测试与重合指标（IC）"
tags: [密码学, 密码分析, 重合指标, Vigenere密码]
related: [concepts/kasiski测试, entities/vigenere密码, concepts/频率分析, findings/kasiski-friedman公式组, methodology/kasiski-friedman破译流程]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Friedmann 测试与重合指标（IC）

Friedmann 测试（通称 Friedman test；本源作 Friedmann，系德文拼法）与 [[concepts/kasiski测试]] 相结合可破译 [[entities/vigenere密码]]：Kasiski 测试只能给出密钥长度的倍数上界，Friedmann 测试则产生密钥长度的数量估计。

## 重合指标 IC

设 n 为某英文明文经 Vigenère 方法加密所得密文的长度，字母 a_i（i ∈ {0,…,25}）在密文中出现 n_i 次，则

```
IC = Σ_{i=1}^{26} n_i(n_i − 1) / ( n(n−1) )                       (5.275b)
```

（求和指标 i = 1..26 与字母下标集 {0,…,25} 不一致，系原文小讹。）

## 密钥长度公式

```
l = 0.027 n / ( (n−1)·IC − 0.038 n + 0.065 )                      (5.275a)
```

常数来源（已核自洽）：0.065 为英语典型 IC，0.038 为随机文本的 IC（≈ 1/26），0.027 = 0.065 − 0.038。

## 确定密钥字母

密钥长度定为 l 后，密文分裂为 l 列；因 Vigenère 密码借助移位密码产生每个列的分量，只需确定各列对 E 的等价移位：若某列中最频繁出现的字母为 V，则在 Vigenère 表中行标 R、列标 E 的交叉处找到 V（式 5.275c，已核 4 + 17 = 21 = V），即得该列的密钥字母 R。流程见 [[methodology/kasiski-friedman破译流程]]；限制条件（密钥与明文等长时失效）同 Kasiski 测试。