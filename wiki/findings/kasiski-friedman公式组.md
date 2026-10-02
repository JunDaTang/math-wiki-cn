---
type: finding
title: "Kasiski–Friedmann 公式组（式 5.275a–c）"
tags: [密码分析, Vigenere密码, 重合指标, 公式]
related: [concepts/kasiski测试, concepts/friedmann测试与重合指标, entities/vigenere密码, methodology/kasiski-friedman破译流程]
source: "[[sources/10-数学手册原书第10版--6-55-保密学--g896dm]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Kasiski–Friedmann 公式组（式 5.275a–c）

本源 5.5.5.2 给出破译 [[entities/vigenere密码]] 的两测试与逐列定钥方法：

```
Kasiski 测试：重复密文串的间距必为密钥长度的倍数；
              密钥长度为诸距离 gcd 的某个因子（有偶然匹配致误之虞）

Friedmann 测试（n = 密文长度，IC = 重合指标）：
l = 0.027 n / ( (n−1)·IC − 0.038 n + 0.065 )                      (5.275a)
IC = Σ_{i=1}^{26} n_i(n_i − 1) / ( n(n−1) )                       (5.275b)
（n_i = 字母 a_i 在密文中出现的次数，i ∈ {0,1,…,25}）

逐列定钥（l 列，每列即一个移位密码）：列中最频繁字母对准 E 查 Vigenère 表，
行 R 与列 E 交于 V ⇒ 该列密钥字母为 R                                (5.275c)
```

## 复算（本 wiki 独立核验）

- **常数自洽**：0.065（英语典型 IC）− 0.038（随机文本 IC ≈ 1/26 = 0.0385）= **0.027** ✓，与式 (5.275a) 分子系数一致。
- **式 (5.275c) 例**：R = a₁₇，E = a₄，密文字母下标 = 17 + 4 = 21 = V ✓（行 R 列 E 交于 V）。
- 公式结构与通行 Friedman 公式一致。

## 原文小讹

式 (5.275b) 求和指标写作 i = 1..26，与字母下标集 {0,…,25} 不一致（应统一为同一指标域）。

## 适用限制（关于 Vigenère，勿外推）

密钥与明文等长（趋向一次一密）时诸法迄今未获成功；此时仅能判别所用的密码属单一字母、短周期多字母还是长周期多字母。操作流程见 [[methodology/kasiski-friedman破译流程]]。