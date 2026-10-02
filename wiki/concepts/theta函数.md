---
type: concept
title: "θ函数"
created: 2026-10-01
updated: 2026-10-01
tags: [theta函数, 椭圆函数, 特殊函数, 复分析, 级数]
related: [雅可比函数, 椭圆积分, 椭圆函数]
sources: ["数学手册(原书第10版)/14.6 椭圆函数.md"]
---

# θ函数

θ函数（theta functions，源文记作 ϑ₁(z, q)–ϑ₄(z, q)）是以满足 |q| < 1 的参数 q（标准理论中称为 nome）与复变量 z 定义的四个三角级数函数，级数对每个复变量 z 都收敛；本手册用它们给出 [[雅可比函数]] sn、cn、dn 的显式商表示 (14.115)。注意：源文小节标题“μ函数”系 ϑ 的 OCR 误读，应为“θ函数”（源文正文括注英文 theta functions 可证）。

## 级数定义（(14.113a–d)）

```latex
\vartheta_1(z,q)=2q^{1/4}\sum_{n=0}^{\infty}(-1)^n q^{n(n+1)}\sin(2n+1)z
\vartheta_2(z,q)=2q^{1/4}\sum_{n=0}^{\infty}q^{n(n+1)}\cos(2n+1)z
\vartheta_3(z,q)=1+2\sum_{n=1}^{\infty}q^{n^2}\cos 2nz
\vartheta_4(z,q)=1+2\sum_{n=1}^{\infty}(-1)^n q^{n^2}\cos 2nz
```

当 |q| < 1（q 为复数）时，四个级数对每个复变量 z 收敛。

## 记号约定 (14.114) 及其关键性

源文约定 ϑₖ(z) := ϑₖ(πz, q)（k = 1, 2, 3, 4），即先把变量放大 π 倍再简写。该约定是核对 (14.115a) 正确性的关键：(14.115a) 前因子 2K·ϑ₄(0)/ϑ₁′(0) 中的 ϑ₁′(0) 是**缩放后变量**的导数（等于 π 乘以按原定义所求的导数）；忽略该约定会误判公式缺少因子 1/π。经 z→0 展开可验证 sn z ≈ z，确认 (14.115) 在此约定下自洽（方法见 [[退化极限与原点展开检验法]]）。

## 雅可比函数的 θ 表示（(14.115)）

```latex
\operatorname{sn}z=2K\,\frac{\vartheta_4(0)}{\vartheta_1'(0)}\,
\frac{\vartheta_1(z/2K)}{\vartheta_4(z/2K)}
\operatorname{cn}z=\frac{\vartheta_4(0)}{\vartheta_2(0)}\,
\frac{\vartheta_2(z/2K)}{\vartheta_4(z/2K)}
\operatorname{dn}z=\frac{\vartheta_4(0)}{\vartheta_3(0)}\,
\frac{\vartheta_3(z/2K)}{\vartheta_4(z/2K)}
q=\exp\!\left(-\pi\frac{K'}{K}\right),\qquad
k=\left(\frac{\vartheta_2(0)}{\vartheta_3(0)}\right)^{\!2}
```

其中 K、K′ 依 (14.109)（参见 [[椭圆积分]]）。参数 q = exp(−πK′/K) 与模数 k 经 (ϑ₂(0)/ϑ₃(0))² 相互联系，是雅可比理论与 θ 函数理论之间的桥梁。本节仅将 θ 函数用作计算雅可比函数的工具，未涉及其自身的拟周期性质。

转录复算见 [[式14-113至14-115theta函数表示转录复算]]。