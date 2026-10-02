---
type: methodology
title: Kasiski–Friedmann 破译流程
tags: [密码分析, Vigenere密码, 操作流程]
related: [concepts/kasiski测试, concepts/friedmann测试与重合指标, entities/vigenere密码, findings/kasiski-friedman公式组, methodology/vigenere查表加解密流程, concepts/频率分析]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Kasiski–Friedmann 破译流程

依据本源 5.5.5.2，对 [[entities/vigenere密码]] 密文的唯密文攻击。**为什么可行**：密钥周期性应用使相同明文串在密钥对齐位置加密成相同密文串，且每个密钥位置等价于一个独立的移位密码（[[concepts/线性代换密码]]）——前者暴露周期，后者允许逐列用频率对准（[[concepts/频率分析]]）。

## 流程

1. **Kasiski 测试（定候选周期）**：在密文中找出重复出现的密文串，记录相邻出现位置的距离；诸距离的 gcd 给出密钥长度的某个因子（真实密钥长度至多是其倍数；警惕偶然匹配）。
2. **Friedmann 测试（定周期数量级）**：统计各字母频数 n_i，计算重合指标 IC = Σ n_i(n_i−1) / (n(n−1))；代入
   `l = 0.027 n / ( (n−1)·IC − 0.038 n + 0.065 )`（式 5.275a）得密钥长度估计。
3. **分列**：按密钥长度 l 将密文按位置 mod l 分成 l 列；每列分量由同一密钥字母经移位密码产生。
4. **逐列定钥**：取每列中出现最频繁的字母，假定它对应明文最频字母 E，在 Vigenère 表中查「行 = 候选密钥字母、列 = E」交叉处是否为该最频字母（式 5.275c：行 R 列 E 交于 V ⇒ 密钥字母 R），得各列密钥字母，拼出密钥。
5. **验证**：以所得密钥按 [[methodology/vigenere查表加解密流程]] 解密全文，检查明文可读性与频率结构。

## 适用限制

密钥与明文等长（趋向一次一密，[[concepts/一次一密]]）时本流程失效；此时仅能判别密码属单一字母、短周期多字母或长周期多字母。公式与常数的复算记录见 [[findings/kasiski-friedman公式组]]。