---
type: query
title: 例 A 原函数 e^{−|a|t} 与 e^{−a|t|} 之辨
created: 2026-10-01
updated: 2026-10-01
tags: [特殊函数变换, 双边指数, 勘误, 数学手册]
related: [findings/15-3-1-4特殊函数变换四例转录复算, concepts/傅里叶变换, queries/15-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/15.3 傅里叶变换.md"]
---
# 例 A 原函数 e^{−|a|t} 与 e^{−a|t|} 之辨

## 原文（转录）

```text
A: 欲探寻原函数 f(t) = e^{−|a|t}, Re a > 0  (A.1) 对应的像函数，…
    ∫_{−A}^{+A} e^{−iωt − a|t|} dt = …                  (A.2)
    F(ω) = 𝓕{e^{−a|t|}} = 2a/(a² + ω²).                (A.3)
```

## 疑点

(A.1) 写作 $\mathrm{e}^{-|a|t}$（对 $a$ 取模），而 (A.2) 被积式与 (A.3) 结果均按 $\mathrm{e}^{-a|t|}$（对 $t$ 取模）计算，前后不一致。

## 证据

- (A.2) 被积式为 $\mathrm{e}^{-\mathrm{i}\omega t-a|t|}$：指数中是 $a|t|$。
- (A.3) 结果 $2a/(a^2+\omega^2)$：分段积分 $\int_0^{\infty}\mathrm{e}^{-(a+\mathrm{i}\omega)t}\,\mathrm{d}t+\int_0^{\infty}\mathrm{e}^{-(a-\mathrm{i}\omega)t}\,\mathrm{d}t=\frac{1}{a+\mathrm{i}\omega}+\frac{1}{a-\mathrm{i}\omega}=\frac{2a}{a^2+\omega^2}$，仅当原函数为 $\mathrm{e}^{-a|t|}$ 时成立。
- 条件 $\operatorname{Re}a>0$ 也只对 $\mathrm{e}^{-a|t|}$ 有意义（保证 $t\to\pm\infty$ 双向衰减）。

## 判定建议

(A.1) 应为 $f(t)=\mathrm{e}^{-a|t|}$（$a$ 落在指数上、$|t|$ 为自变量取模），以 (A.2)/(A.3) 为准。参见 [[findings/15-3-1-4特殊函数变换四例转录复算]]。