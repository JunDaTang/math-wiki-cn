---
type: concept
title: Wallis 积分公式
created: 2026-10-02
updated: 2026-10-02
tags: [定积分, 递推公式, 三角函数]
related: [Gamma函数（第二型欧拉积分）, Beta函数（第一型欧拉积分）, 二项式微分递推公式, 公式21-6为21-7a特化之复算, Wallis递推形式与Gamma-Beta闭式比较]
sources: ["数学手册(原书第10版)/21.8 定积分.md"]
---
# Wallis 积分公式

Wallis 积分公式给出 $\int_0^{\pi/2}\sin^n x\,dx$（等价地 $\int_0^{\pi/2}\cos^n x\,dx$）按 n 奇偶的两支连乘积闭式，源自递推 $I_n=\frac{n-1}{n}I_{n-2}$。

## 手册 21.6

$$\int_0^{\pi/2}\sin^n x\,dx=\begin{cases}\frac{2}{3}\cdot\frac{4}{5}\cdot\frac{6}{7}\cdots\frac{n-1}{n}, & n\text{ 为奇数},\\[4pt] \frac{\pi}{2}\cdot\frac{1}{2}\cdot\frac{3}{4}\cdot\frac{5}{6}\cdots\frac{n-1}{n}, & n\text{ 为偶数}.\end{cases}$$

## 与 Γ/B 闭式的关系

21.6 是 21.7a 取 β=−½、α=(n−1)/2 的特化：

$$\int_0^{\pi/2}\sin^n x\,dx=\frac{\Gamma(\frac{n+1}{2})\sqrt{\pi}}{2\,\Gamma(\frac{n+2}{2})},$$

n 奇、偶两支分别化为上式两行连乘积——复算证实，见 [[公式21-6为21-7a特化之复算]] 与 [[Wallis递推形式与Gamma-Beta闭式比较]]。这一特化把 Wallis 递推形式（离散、按奇偶分支）与 [[Gamma函数（第二型欧拉积分）]]/[[Beta函数（第一型欧拉积分）]] 闭式（连续参数）打通，其递推思想与 [[二项式微分递推公式]] 同源。

## 条件张力

21.7a 正文称「对任意 α, β 成立」，而收敛实需 α, β>−1（其下三个例子 α=−¼、−⅓ 等皆在收敛域内）；或原文本有「(非整数)」之类限定被脱——见 [[21-8全节系统性转写讹误清单]]。