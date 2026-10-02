---
type: entity
title: "Hill 密码（矩阵代换）"
tags: [密码学, 多字母代换, 矩阵, 模算术, 古典密码]
related: [entities/vigenere密码, entities/剩余类环zn, entities/互素剩余类群zmx, concepts/线性代换密码, findings/hill密码算例autumn-jihzmt, methodology/hill密码模26矩阵加密流程, queries/5-5未入库依赖缺口]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# Hill 密码（矩阵代换）

Hill 密码是本源 5.5.4.4 以「矩阵代换」为题给出的密码：把长为 m 的明文区组视为字母下标向量，左乘一个满足 gcd(det S, n) = 1 的整数方阵 S，各分量按模 n 算术约化，即得密文；解密用 S 模 n 的逆矩阵。条件 gcd(det S, n) = 1 正是 S 在 [[entities/剩余类环zn]] 上的矩阵环中可逆的判据（可逆元结构见 [[entities/互素剩余类群zmx]]）。

## 定义

```
密文 = ( S · ( a_{t(1)}, a_{t(2)}, …, a_{t(m)} )ᵀ )ᵀ ，分量按模 n 算术确定      (5.274)

S = (s_ij)，s_ij ∈ {0, 1, …, n−1}（原文作 {0,…,m−1}，疑为讹），
S 为非奇异 m 阶方阵（原文作「(m,n) 型」，疑为讹），且 gcd(det S, n) = 1
```

原文称其「表示一个单一字母矩阵代换」；但按 5.5.4.1 的分类（固定长度 m > 1 的字母串被代换为多字母代换），该归类表述与实际机制之间的关系存疑，宜存照。

## 算例（m = 3，模 26，AUTUMN → JIHZMT，全链已复算）

```
S = ⎛14  8  3⎞
    ⎜ 8  5  2⎟ ，  det S = 14·(5·1−2·2) − 8·(8·1−2·3) + 3·(8·2−5·3) = 14 − 16 + 3 = 1
    ⎝ 3  2  1⎠

字母编号 a₀ = A, …, a₂₅ = Z；明文 AUTUMN 分为 AUT = (0,20,19) 与 UMN = (20,12,13)：
S·(0,20,19)ᵀ  = (217,138,59)ᵀ  ≡ (9,8,7)ᵀ   = J I H  (mod 26)
S·(20,12,13)ᵀ = (415,246,97)ᵀ  ≡ (25,12,19)ᵀ = Z M T  (mod 26)
故 AUTUMN → JIHZMT
```

det S = 1 满足 gcd(det S, 26) = 1。详见 [[findings/hill密码算例autumn-jihzmt]]；加密操作流程见 [[methodology/hill密码模26矩阵加密流程]]。

## 依赖与交叉

Hill 密码依赖的矩阵运算工具在手册 4.x 章讲解，该部分尚未入库（见 [[queries/5-5未入库依赖缺口]]）。与线性代换密码、Vigenère 密码的对照见 [[comparisons/单一字母与多字母代换密码比较]]。