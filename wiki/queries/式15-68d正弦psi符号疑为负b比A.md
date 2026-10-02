---
type: query
title: 式 (15.68d) 正弦 psi 符号疑为 −b/A
created: 2026-10-01
updated: 2026-10-01
tags: [傅里叶积分, 振幅相位形式, 勘误, 数学手册]
related: [concepts/傅里叶积分, findings/式15-64至15-68傅里叶积分公式转录复算, concepts/频谱（振幅谱与相位谱）, queries/15-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/15.3 傅里叶变换.md"]
---
# 式 (15.68d) 正弦 psi 符号疑为 −b/A

## 原文（转录）

```text
(15.68a)  A(ω) = √(a²(ω) + b²(ω))
(15.68b)  φ(ω) = ψ(ω) + π/2
(15.68c)  cos ψ(ω) = a(ω)/A(ω)
(15.68d)  sin ψ(ω) = b(ω)/A(ω)
(15.68e)  cos φ(ω) = b(ω)/A(ω)
(15.68f)  sin φ(ω) = a(ω)/A(ω)
```

## 疑点

(15.68d) 与同组其余各式联立矛盾。

## 证据

由 (15.66) $f=\int_0^{\infty}A\cos[\omega t+\psi]\,\mathrm{d}\omega$ 展开并与 (15.65b) 的 $a\cos\omega t+b\sin\omega t$ 比较系数：$a=A\cos\psi$、$b=-A\sin\psi$，故

$$\sin\psi(\omega)=-\frac{b(\omega)}{A(\omega)}.$$

再核 (15.68e,f)：$\cos\varphi=\cos(\psi+\pi/2)=-\sin\psi=b/A$、$\sin\varphi=\sin(\psi+\pi/2)=\cos\psi=a/A$——即 (15.68e,f) 只有在 $\sin\psi=-b/A$ 时才成立，与 (15.68d) 的 $+b/A$ 矛盾。

## 判定建议

(15.68d) 应为 $\sin\psi(\omega)=-b(\omega)/A(\omega)$（丢负号）。属符号级疑误，直接影响振幅–相位形式 (15.66) 的使用；是否原书即误需对照原版。参见 [[findings/式15-64至15-68傅里叶积分公式转录复算]]、[[concepts/傅里叶积分]]。