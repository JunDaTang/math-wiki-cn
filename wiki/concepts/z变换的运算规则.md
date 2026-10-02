---
type: concept
title: "Z变换的运算规则"
created: 2026-10-01
updated: 2026-10-01
tags: [z变换, 移位定理, 差分, 卷积定理, 运算规则]
related: [z变换, 离散卷积, z变换的极限定理, 拉普拉斯变换的运算规则, z变换求解常系数线性差分方程流程]
sources: ["数学手册(原书第10版)/15.4 Z变换.md"]
---

# Z变换的运算规则

Z变换的运算规则刻画原序列上的运算对变换的影响及其反推（《数学手册》15.4.1.3）。设 $|z|>1/R$ 时 $F(z)=\mathcal{Z}\{f_n\}$，共七组法则（式 15.113–15.122）：

1. **平移（第一移位定理，向后平移）**：

$$\mathcal{Z}\{f_{n-k}\}=z^{-k}F(z)\quad(k=0,1,2,\dots),\qquad n-k<0\ \text{时约定}\ f_{n-k}=0\tag{15.113}$$

2. **平移（第二移位定理，向前平移）**：

$$\mathcal{Z}\{f_{n+k}\}=z^{k}\left[F(z)-\sum_{v=0}^{k-1}f_v\left(\frac1z\right)^{v}\right]\quad(k=1,2,\dots)\tag{15.114}$$

3. **求和**：当 $|z|>\max(1,1/R)$ 时，$\mathcal{Z}\{\sum_{v=0}^{n-1}f_v\}=\dfrac{F(z)}{z-1}$。（15.115）
4. **差分**：$\mathcal{Z}\{\Delta^{k}f_n\}=(z-1)^{k}F(z)-z\sum_{v=0}^{k-1}(z-1)^{k-v-1}\Delta^{v}f_0$（一般式，15.117；一阶行 $(z-1)F(z)-zf_0$）。**转写本二阶行末项作 $-zf_0$，疑脱 $\Delta$，应为 $-z\,\Delta f_0$**，见 [[queries/式15-117二阶差分末项zf0疑为zδf0]]。
5. **阻尼**：对任意复数 $\lambda\neq0$ 和 $|z|>|\lambda|/R$，$\mathcal{Z}\{\lambda^{n}f_n\}=F(z/\lambda)$。（15.118）
6. **卷积**：$f_n*g_n=\sum_{v=0}^{n}f_vg_{n-v}$，且 $\mathcal{Z}\{f_n*g_n\}=F(z)G(z)$（15.119/15.120，卷积定理，相当于两个幂级数的乘法法则），见 [[concepts/离散卷积]]。
7. **微分**：$\mathcal{Z}\{nf_n\}=-z\dfrac{\mathrm{d}F(z)}{\mathrm{d}z}$（15.121，重复运用可得 $F(z)$ 的高阶导数）；**积分**：假定 $f_0=0$ 时 $\mathcal{Z}\{f_n/n\}=\displaystyle\int_z^{\infty}\frac{F(\xi)}{\xi}\,\mathrm{d}\xi$。（15.122）

## 注意事项

- 「第一/第二移位定理」的向前/向后命名为本书约定，文献中命名或有互换，引用时须以公式本身为准。
- (15.122) 需假设 $f_0=0$（否则 $f_n/n$ 在 $n=0$ 处无定义）。

## 与连续侧的平行

与 [[concepts/拉普拉斯变换的运算规则]] 平行：差分 ↔ 微分（$(z-1)\leftrightarrow p$）、求和 ↔ 积分（$(z-1)^{-1}\leftrightarrow p^{-1}$）；解差分方程时第二移位定理所起的作用相当于解微分方程时的微分规则。系统对应表见 [[comparisons/z变换与拉普拉斯变换关系比较]]。全组法则的复算核验见 [[findings/式15-113至15-122-z变换计算法则转录复算]]。