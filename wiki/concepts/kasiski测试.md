---
type: concept
title: Kasiski 测试
tags: [密码学, 密码分析, Vigenere密码]
related: [entities/vigenere密码, concepts/friedmann测试与重合指标, concepts/频率分析, findings/kasiski-friedman公式组, methodology/kasiski-friedman破译流程]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Kasiski 测试

Kasiski 测试是破译 [[entities/vigenere密码]] 的第一步（本源 5.5.5.2），利用其加密算法**周期性地应用密钥**的事实：如果相同的明文字母串被密钥的同一部分加密，那么将产生相同的密文字母串。

## 论断

- 密文中相同密文串的相隔距离（长度）必然是**密钥长度的倍数**。
- 在有几个重复出现的密文串的情形，密钥长度是所有距离的最大公因子的某个因子。
- 风险：偶然出现的匹配会导致错误结论。

因此 Kasiski 测试确定的密钥长度**至多是真实密钥长度的倍数**（给出倍数上界）；密钥长度的数量估计由 [[concepts/friedmann测试与重合指标]]（Friedmann 测试）给出。二者结合的操作流程见 [[methodology/kasiski-friedman破译流程]]，公式记录见 [[findings/kasiski-friedman公式组]]。

## 限制

当 Vigenère 密钥与明文一样长（趋向一次一密，[[concepts/一次一密]]）时，Kasiski 与 Friedmann 方法迄今都未获成功；此时仅能推断所用密码是单一字母的、短周期多字母的还是长周期多字母的。