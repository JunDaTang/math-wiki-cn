---
type: query
title: 例 D 被积函数指数符号之辨
created: 2026-10-01
updated: 2026-10-01
tags: [阻尼振荡, 洛伦兹曲线, 勘误, 数学手册]
related: [findings/15-3-1-4特殊函数变换四例转录复算, concepts/洛伦兹曲线与布赖特-维格纳曲线, methodology/复辅助函数求实信号频谱流程, queries/15-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/15.3 傅里叶变换.md"]
---
# 例 D 被积函数指数符号之辨

## 原文（转录）

```text
𝓕{f*(t)} = ∫₀^∞ e^{−iωt} e^{(−α+iω₀)t} dt = ∫₀^∞ e^{(−α+(ω−ω₀)i)t} dt
          = [ e^{−αt} e^{i(ω−ω₀)t} / (−α+i(ω₀−ω)) ] |₀^∞
          = 1/(α−i(ω₀−ω)) = (α+i(ω₀−ω))/(α²+(ω−ω₀)²)
```

## 疑点

第一行被积式指数写作 $(\omega-\omega_0)\mathrm{i}$，第二行分子指数为 $\mathrm{i}(\omega-\omega_0)$ 而分母为 $-\alpha+\mathrm{i}(\omega_0-\omega)$——分子分母的频率差符号相反，内部不一致。

## 证据

由核 $\mathrm{e}^{-\mathrm{i}\omega t}\cdot\mathrm{e}^{(-\alpha+\mathrm{i}\omega_0)t}=\mathrm{e}^{-\alpha t}\mathrm{e}^{\mathrm{i}(\omega_0-\omega)t}$，正确的被积指数为 $(-\alpha+\mathrm{i}(\omega_0-\omega))t$，反导数分母 $-\alpha+\mathrm{i}(\omega_0-\omega)$，与第二行分母一致而与第一行指数矛盾。后续结果 $\frac{\alpha+\mathrm{i}(\omega_0-\omega)}{\alpha^2+(\omega-\omega_0)^2}$ 与最终洛伦兹式 $\mathcal{F}\{f\}=\frac{\alpha}{\alpha^2+(\omega-\omega_0)^2}$ 均正确。

## 判定建议

第一行指数应改为 $(\omega_0-\omega)$（或统一分子指数为 $\mathrm{i}(\omega_0-\omega)t)$），属中间步符号讹误、结论不受影响。另见 [[findings/15-3-1-4特殊函数变换四例转录复算]] 中关于 $\mathcal{F}\{f\}=\operatorname{Re}\mathcal{F}\{f^*\}$ 严格性的附注。参见 [[concepts/洛伦兹曲线与布赖特-维格纳曲线]]。