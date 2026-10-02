---
type: finding
title: "Vigenère 算例 ONCEUPONATIME（密钥 HUT → VHVL OIVHTACFL）"
tags: [密码学, Vigenere密码, 算例复算]
related: [entities/vigenere密码, methodology/vigenere查表加解密流程, concepts/频率分析]
source: "[[sources/10-数学手册原书第10版--6-55-保密学--g896dm]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Vigenère 算例 ONCEUPONATIME（密钥 HUT → VHVL OIVHTACFL）

本源 5.5.4.3 的算例：密钥 HUT，明文 ONCEUPONATIME，密钥周期重复至明文长度：

| | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 明文 | O | N | C | E | U | P | O | N | A | T | I | M | E |
| 密钥 | H | U | T | H | U | T | H | U | T | H | U | T | H |
| 密文 | V | H | V | L | O | I | V | H | T | A | C | F | L |

形式化：明文字母 a_i 配同位置密钥字母 a_j，密文为 a_{i+j}（下标模 26）。

## 复算（本 wiki 逐字母独立核验，13/13 吻合）

| 位置 | 明文 (i) | 密钥 (j) | i+j | mod 26 | 密文 |
|---|---|---|---|---|---|
| 1 | O = 14 | H = 7 | 21 | 21 | V |
| 2 | N = 13 | U = 20 | 33 | 7 | H |
| 3 | C = 2 | T = 19 | 21 | 21 | V |
| 4 | E = 4 | H = 7 | 11 | 11 | L |
| 5 | U = 20 | U = 20 | 40 | 14 | O |
| 6 | P = 15 | T = 19 | 34 | 8 | I |
| 7 | O = 14 | H = 7 | 21 | 21 | V |
| 8 | N = 13 | U = 20 | 33 | 7 | H |
| 9 | A = 0 | T = 19 | 19 | 19 | T |
| 10 | T = 19 | H = 7 | 26 | 0 | A |
| 11 | I = 8 | U = 20 | 28 | 2 | C |
| 12 | M = 12 | T = 19 | 31 | 5 | F |
| 13 | E = 4 | H = 7 | 11 | 11 | L |

含 mod 26 回绕的位置（2、5、6、8、10、11、12）均吻合。原文解说中「密钥的第 15 个位置由字母 H 取定」应为「第 1 个位置」之讹（明文首字母 O = a₁₄ 配密钥首字母 H = a₇ 得 a₂₁ = V）。