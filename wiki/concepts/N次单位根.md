---
type: concept
title: N 次单位根
created: 2026-10-01
updated: 2026-10-01
tags: [调和分析, 复数, 代数, 离散傅里叶变换]
related: [离散傅里叶变换, 快速傅里叶变换]
sources: ["数学手册(原书第10版)/19.6.4 调和分析.md"]
---
# N 次单位根

$N$ 次单位根是方程 $z^N=1$ 的解。《数学手册(原书第10版)》19.6.4.2 取

$$\omega_N=\mathrm{e}^{-2\pi\mathrm{i}/N}$$

为基本单位根，其逐次幂 $\omega_N^\nu\ (\nu=0,1,\dots,N-1)$ 给出全部 $N$ 个解。因 $\mathrm{e}^{-2\pi\mathrm{i}}=1$，成立循环性质：

$$\omega_N^N=1,\qquad \omega_N^{N+1}=\omega_N^1,\qquad \omega_N^{N+2}=\omega_N^2,\ \dots\tag{19.225}$$

## 在 FFT 中的作用

单位根的性质是[[快速傅里叶变换]]逐次二分归化的代数基础，[[离散傅里叶变换]]的折半全赖于此：

1. **周期性**：$\omega_N^{2l(n+\nu)}=\omega_N^{2ln}\omega_N^{2l\nu}=\omega_N^{2l\nu}$（因 $2ln=lN$ 且 $\omega_N^N=1$），用于把偶指标系数的求和折半 (19.226)；
2. **平方降阶**：$\omega_N^2=\omega_{N/2}$（源文记半长为 $n$、写作 $w_N^2=w_n$），使折半后的和式恰为长度 $N/2$ 的 DFT (19.228)、(19.231)；
3. **半周期反号**：$\omega_N^{N/2}=\mathrm{e}^{-\pi\mathrm{i}}=-1$（源文未显式写出，为奇指标归化 (19.229) 的复算要点）。

$N=8$ 算例中出现的特殊值：$\omega_8=0.707107(1-\mathrm{i})$，$\omega_8^2=-\mathrm{i}$，$\omega_8^3=-0.707107(1+\mathrm{i})$。

## 转录说明

源文「称之为 次单位根」脱字「N」；「指数 $w_N^\nu=z$ 满足方程 $z^N=1$」处 $\omega_N$ 与 $w_N$ 记号混用，本维基统一作 $\omega_N$（见[[19-6-4全节系统性转写讹误清单]]）。