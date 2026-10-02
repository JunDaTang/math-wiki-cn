---
type: finding
title: 公式 53 arctan 宗量倒置与 β 脱方复算
source: "[[10-数学手册原书第10版--11-2113-拉普拉斯变换--10ahihv]]"
confidence: high
replicated: true
created: 2026-10-02
updated: 2026-10-02
tags: [复算, 拉普拉斯变换, 转写讹误, 反三角族]
related: [21-13拉普拉斯变换全表复算, 拉普拉斯变换对复算法, 拉普拉斯变换表]
sources: ["数学手册(原书第10版)/21.13 拉普拉斯变换.md"]
---

# 公式 53 arctan 宗量倒置与 β 脱方复算

21.13 节式 53 原文为

$$F(p)=\arctan\frac{p^{2}-\alpha p+\beta}{\alpha\beta},\qquad f(t)=\frac{\mathrm{e}^{\alpha t}-1}{t}\sin\beta t,$$

复算判定：arctan 宗量倒置且 $\beta$ 疑脱平方，$F(p)$ 应为 $\arctan\dfrac{\alpha\beta}{p^{2}-\alpha p+\beta^{2}}$。

## 复算过程（除法规则）

由 $\mathcal{L}\{g(t)/t\}=\int_p^\infty G(s)\,ds$：

$$G(p)=\mathcal{L}\{(\mathrm{e}^{\alpha t}-1)\sin\beta t\}=\frac{\beta}{(p-\alpha)^{2}+\beta^{2}}-\frac{\beta}{p^{2}+\beta^{2}},$$

$$\int_p^\infty G(s)\,ds=\arctan\frac{\beta}{p-\alpha}-\arctan\frac{\beta}{p}
=\arctan\frac{\alpha\beta}{p^{2}-\alpha p+\beta^{2}},$$

末步用 arctan 差角公式 $\arctan u-\arctan v=\arctan\frac{u-v}{1+uv}$（$u=\frac{\beta}{p-\alpha},\ v=\frac{\beta}{p}$，化简得 $\frac{\alpha\beta}{p^{2}-\alpha p+\beta^{2}}$）。

## 大 p 渐近核查（第二重独立矛盾）

原表宗量 $\frac{p^{2}-\alpha p+\beta}{\alpha\beta}\to\infty$，故 $F(p)\to\frac{\pi}{2}\neq0$；而本条 $f(t)\sim\alpha\beta t\ (t\to0^+)$ 连续且 $f(0^+)=0$，其变换必须满足 $F(p)\to0\ (p\to\infty)$。倒置后的宗量 $\frac{\alpha\beta}{p^{2}-\alpha p+\beta^{2}}\to0$，渐近正常。

## 强度与边界

证据强度：强（直接复算 + 渐近判据双重一致）。原表文的错误可分解为「宗量分子分母倒置」与「$\beta$ 脱平方」两处滑笔的复合；是转写还是排印之误见 [[queries/公式53arctan宗量倒置之辨]]。本判定仅针对 21.13 节式 53。