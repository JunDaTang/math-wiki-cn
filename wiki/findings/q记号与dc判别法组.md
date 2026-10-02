---
type: finding
title: Q 记号组与 DC-1–DC-11 判别法表
tags: [数论, 整除性判别法, 十进制]
related: [整除性判别法, 式5-229g标号是否应为q3撇]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.4.1 整除性.md"]
source: "[[10-数学手册原书第10版--7-541-整除性--1bgclvy]]"
confidence: high
replicated: true
---

# Q 记号组与 DC-1–DC-11 判别法表

## Q 记号（式 5.229a–g）

$$n=(a_k a_{k-1}\dots a_2 a_1 a_0)_{10}=a_k 10^k+\dots+a_1 10+a_0\tag{5.229a}$$

$$Q_1(n)=a_0+a_1+\dots+a_k,\qquad Q_1'(n)=a_0-a_1+a_2-+\dots+(-1)^k a_k\tag{5.229b,c}$$

$$Q_2(n)=(a_1a_0)_{10}+(a_3a_2)_{10}+\dots,\qquad Q_2'(n)=(a_1a_0)_{10}-(a_3a_2)_{10}+\dots\tag{5.229d,e}$$

$$Q_3(n)=(a_2a_1a_0)_{10}+(a_5a_4a_3)_{10}+\dots,\qquad Q_3'(n)=(a_2a_1a_0)_{10}-(a_5a_4a_3)_{10}+\dots\tag{5.229f,g}$$

（源文 (5.229g) 左端标号误作 $Q_2'$，应为 $Q_3'$，见 [[queries/式5-229g标号是否应为q3撇]]；源文「数宇和」为「数字和」之讹。）

## DC 表（式 5.230a–k）

| 编号 | 判别法 | 式号 |
|---|---|---|
| DC-1 | $3\mid n \Leftrightarrow 3\mid Q_1(n)$ | 5.230a |
| DC-2 | $7\mid n \Leftrightarrow 7\mid Q_3'(n)$ | 5.230b |
| DC-3 | $9\mid n \Leftrightarrow 9\mid Q_1(n)$ | 5.230c |
| DC-4 | $11\mid n \Leftrightarrow 11\mid Q_1'(n)$ | 5.230d |
| DC-5 | $13\mid n \Leftrightarrow 13\mid Q_3'(n)$ | 5.230e |
| DC-6 | $37\mid n \Leftrightarrow 37\mid Q_3(n)$ | 5.230f |
| DC-7 | $101\mid n \Leftrightarrow 101\mid Q_2'(n)$ | 5.230g |
| DC-8 | $2\mid n \Leftrightarrow 2\mid a_0$ | 5.230h |
| DC-9 | $5\mid n \Leftrightarrow 5\mid a_0$ | 5.230i |
| DC-10 | $2^k\mid n \Leftrightarrow 2^k\mid(a_{k-1}\dots a_1 a_0)_{10}$ | 5.230j |
| DC-11 | $5^k\mid n \Leftrightarrow 5^k\mid(a_{k-1}\dots a_1 a_0)_{10}$ | 5.230k |

## 算例（本次独立复算，全部通过）

- $123456789$：$Q_1=45$，$Q_1'=5$，$Q_2=225$，$Q_2'=45$，$Q_3=1368$，$Q_3'=456$ ✓
- $9\mid 123456789$（$9\mid 45$）✓；$7\nmid 123456789$（$7\nmid 456$）✓
- $11\mid 91619$（$Q_1'=22$，源文「11122」为「11|22」之讹）✓
- $2^4\mid 99994096$（$2^4\mid 4096$）✓

## 原理（本 wiki 推断补充，非源文本）

判别法依据十进制的模同余：$10\equiv 1\ (\mathrm{mod}\ 3,9)$、$10\equiv-1\ (\mathrm{mod}\ 11)$、$10^2\equiv-1\ (\mathrm{mod}\ 101)$、$10^3\equiv-1\ (\mathrm{mod}\ 7,13)$、$10^3\equiv 1\ (\mathrm{mod}\ 37)$，以及 $10^k\equiv 0\ (\mathrm{mod}\ 2^k,5^k)$。此为机理说明，不属于源文本。
