---
type: methodology
title: Vigenère 查表加解密流程
tags: [密码学, Vigenere密码, 操作流程]
related: [entities/vigenere密码, findings/vigenere算例onceuponatime, methodology/kasiski-friedman破译流程]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Vigenère 查表加解密流程

依据本源 5.5.4.3（卡罗尔变体的 Vigenère 表实现）。**为什么用查表**：Vigenère 加密逐位做「明文下标 + 密钥下标 (mod 26)」的模加法，Vigenère 表把全部 26×26 种组合预先排成方阵（行 = 密钥字母、列 = 明文字母，交叉处即密文字母），使加解密成为纯查表操作，无需逐位计算。

## 加密流程

1. 取密钥（如 HUT），周期性重复直至与明文等长。
2. 对每个位置：以该位置密钥字母定行、明文字母定列，取交叉处字母为密文字母。
3. 依次读出密文。

## 解密流程

反向使用同一张表：以密钥字母定行，沿该行找到密文字母，其所在列的顶行字母即明文字母。

## 算例

明文 ONCEUPONATIME、密钥 HUT → 密文 VHVL OIVHTACFL（13 个字母逐位复算吻合，见 [[findings/vigenere算例onceuponatime]]）。形式化：明文 a_i 配密钥 a_j ⇒ 密文 a_{i+j}（mod 26）。

## 与破译的关系

本流程是合法通信方的操作；窃听方对同一密码的对应流程是 [[methodology/kasiski-friedman破译流程]]。