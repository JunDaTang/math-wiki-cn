---
type: query
title: 单摆异宿轨 sin 疑为 sinh 之辨
tags: [转写讹误, 梅尔尼科夫方法, 单摆, 异宿轨]
related: [梅尔尼科夫方法, 式17-90至17-92梅尔尼科夫方法与单摆算例复算]
created: 2026-10-01
updated: 2026-10-01
sources: ["数学手册(原书第10版)/17.3.2 过渡到混沌.md"]
---

# 单摆异宿轨 sin 疑为 sinh 之辨

## 疑点

源文（17.3.2.3 之 3）单摆算例的异宿轨写作 φ^±(t) = (±2 arctan(sin t), ±2/cosh t)。

## 证据

1. **相容性**：d/dt[2 arctan(sinh t)] = 2 cosh t/(1+sinh²t) = 2/cosh t，恰与第二分量 ±2/cosh t（即 ẋ）相容；而 d/dt[2 arctan(sin t)] = 2cos t/(1+sin²t) 与第二分量矛盾。
2. **能量核验**：x=±2 arctan(sinh t)、y=±2 sech t 时 H=y²/2−cos x=1，恰为分界线水平（鞍点 (±π,0) 处 H=1）。
3. **交叉印证**：以 sinh 校正后复算 M(t₀)=∓2π sin(ωt₀)/cosh(πω/2) 与源文一致（用 ∫cos(ωt)sech t dt = π/cosh(πω/2) 与奇性相消）。

## 结论倾向

"sin t"为"sinh t"之转写之讹。复算记录见 [[findings/式17-90至17-92梅尔尼科夫方法与单摆算例复算]]；本页可作为已基本闭合之辨（数学证据充分），存档待原书最终确认。