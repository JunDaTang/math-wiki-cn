---
type: methodology
title: RSA 加解密流程
tags: [RSA, 公钥密码, 操作流程, 模算术]
related: [entities/rsa方法, findings/rsa算法与算例, concepts/费马-欧拉定理, concepts/线性同余式, concepts/欧拉函数, methodology/费马-欧拉降幂求模流程, methodology/线性同余式转丢番图方程求解流程]
sources: ["数学手册(原书第10版)/5.5 保密学.md"]
created: 2026-09-30
updated: 2026-09-30
---

# RSA 加解密流程

依据本源 5.5.7.3。**为什么可行**：加密 R = N^r mod m 与解密 N = R^s mod m 互逆的保证是欧拉-费马定理（[[concepts/费马-欧拉定理]]）——由 rs ≡ 1 (mod φ(m)) 得 R^s = N^{1+kφ(m)} ≡ N·(N^{φ(m)})^k ≡ N (mod m)；私钥 s 的存在性则归结为 [[concepts/线性同余式]] 的可解性（gcd(r, φ(m)) = 1）。

## 密钥生成（接收者 B）

1. 选取两个大素数 p、q；算 m = pq 与 φ(m) = (p−1)(q−1)（[[concepts/欧拉函数]]）。
2. 取 r 使 gcd(r, φ(m)) = 1 且 1 < r < φ(m)。
3. 解线性同余式 rs ≡ 1 (mod φ(m)) 得 s（可用 [[methodology/线性同余式转丢番图方程求解流程]]）。
4. 公布 m 与 r（公开密钥）；p、q、φ(m)、s 保密（私人密钥）。

## 加密（发送者 A）

1. 将消息文本转换为数字串，分裂成若干相同长度的区组（每区组小于 100 个十进制数位，数值小于 m）。
2. 对每区组 N 计算 R ≡ N^r (mod m)（式 5.276a），发送 R。

## 解密（接收者 B）

1. 对每个收到的 R 计算 R^s (mod m)（式 5.276b），还原 N。
2. 数字串转回文本。

大指数模幂的实际计算用 [[methodology/费马-欧拉降幂求模流程]]（如 578⁶⁰⁵ mod 1073）。

## 算例（已全链复算）

p = 29, q = 37 ⇒ m = 1073、φ(m) = 1008；r = 5、s = 605；N = 8 ⇒ R = 8⁵ mod 1073 = 578；R^s = 578⁶⁰⁵ ≡ 8 (mod 1073)。注意原文模数印作 1037 为讹误（见 [[findings/rsa算法与算例]]、[[queries/rsa算例模数1037是否应为1073]]）。理论缺口：式 5.276b 引用 N^{φ(m)} ≡ 1 需 gcd(N, m) = 1（见 [[queries/rsa模幂需gcd条件缺失]]）。