---
type: entity
title: "Vigenère 密码"
tags: [密码学, 多字母代换, 古典密码]
related: [entities/hill密码, concepts/线性代换密码, concepts/频率分析, concepts/kasiski测试, concepts/friedmann测试与重合指标, concepts/一次一密, findings/vigenere算例onceuponatime, methodology/vigenere查表加解密流程]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Vigenère 密码

Vigenère 密码是一种基于密钥周期性应用的多字母代换密码：明文每个字母的密文由位于相同位置的密钥字母确定，密钥较短时重复直至与明文等长；形式化地，明文字母 a_i 配同位置密钥字母 a_j 时，密文字母为 a_{i+j}（下标模 n）。本源 5.5.4.3 给出其定义、Vigenère 表与算例，5.5.5.2 以其为 Kasiski–Friedmann 破译的对象，5.5.6 的一次一密则是其密钥取到与明文等长之随机串的极限情形。注意本源正文两处将「Vigenère」误转写为「Vigen如」「Vigen加」。

## Vigenère 表

行标为密钥字母、列标为明文字母，交叉处即密文字母（每个行表示其最左边关键字母的密码）：

| | A | B | C | D | E | F | … |
|---|---|---|---|---|---|---|---|
| **A** | A | B | C | D | E | F | … |
| **B** | B | C | D | E | F | G | … |
| **C** | C | D | E | F | G | H | … |
| **D** | D | E | F | G | H | I | … |
| **E** | E | F | G | H | I | J | … |
| **F** | F | G | H | I | J | K | … |
| ⋮ | ⋮ | ⋮ | ⋮ | ⋮ | ⋮ | ⋮ | ⋱ |

卡罗尔 (L. Carroll) 创立了 Vigenère 密码的一个变体，应用上表加密和解密。

## 算例（密钥 HUT，13 个字母全部复算吻合）

| | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 明文 | O | N | C | E | U | P | O | N | A | T | I | M | E |
| 密钥 | H | U | T | H | U | T | H | U | T | H | U | T | H |
| 密文 | V | H | V | L | O | I | V | H | T | A | C | F | L |

例如 O = a₁₄ 与 H = a₇ 得 a₂₁ = V；T = a₁₉ 与 H = a₇ 得 a₂₆ = a₀ = A（mod 26 回绕）。原文「密钥的第 15 个位置由字母 H 取定」应为「第 1 个位置」之讹。详见 [[findings/vigenere算例onceuponatime]]。

## 密码分析

由于密钥周期性应用，相同明文串被密钥同一部分加密会产生相同密文串：这是 [[concepts/kasiski测试]] 与 [[concepts/friedmann测试与重合指标]] 的攻击基础，操作流程见 [[methodology/kasiski-friedman破译流程]]；密钥与明文等长时（趋向 [[concepts/一次一密]]）上述方法失效。查表加解密的操作流程见 [[methodology/vigenere查表加解密流程]]；与其他古典密码的对照见 [[comparisons/单一字母与多字母代换密码比较]]。