---
type: finding
title: 式 15.46 与 √p 例反演积分转录复算
created: 2026-10-01
updated: 2026-10-01
tags: [转录复算, 反演公式, 围道积分, 分支割线]
related: [反演公式, 负实轴分支割线钥匙孔围道逆积分流程, 若尔当引理, 留数定理, 多值函数与主值, 圆周EF上留数为epsilon疑为半径为epsilon]
sources: ["数学手册(原书第10版)/15.2.2 到原始空间的逆变换.md"]
source: "[[10-数学手册原书第10版--14-1522-到原始空间的逆变换--lrl99z]]"
confidence: high
replicated: true
---

# 式 15.46 与 √p 例反演积分转录复算

## 反演公式转录

```latex
(15.46)  f(t) = lim_{yₙ→∞} (1/2πi)∫_{c−iyₙ}^{c+iyₙ} e^{tp}F(p)dp
```

源文：该式表示特定区域内解析函数的复积分，复函数积分理论可使用的积分方法（留数计算、依柯西积分定理的路径变化）此时都可以应用。

## √p 例转录

「·巾千 $\sqrt p$」（疑为「由于 $\sqrt p$」），$F(p)=\frac{p}{p^2+\omega^2}e^{-\sqrt p\,\alpha}$ 是双值函数，故选择图 15.20 的积分路径（负实轴钥匙孔围道，六段 $\widehat{AB},\overline{BE},\widehat{EF},\overline{FC},\widehat{CD},\overline{DA}$）：

$$\frac{1}{2\pi\mathrm{i}}\oint_{(K)}e^{tp}\frac{p}{p^2+\omega^2}e^{-\alpha\sqrt p}\,\mathrm{d}p=\int_{\widehat{AB}}\cdots+\int_{\widehat{CD}}\cdots+\int_{\widehat{EF}}\cdots+\int_{\overline{DA}}\cdots+\int_{\overline{BE}}\cdots+\int_{\overline{FC}}\cdots=\sum\operatorname{Res}e^{tp}F(p)=e^{-\alpha\sqrt{\omega/2}}\cos\left(\omega t-\alpha\sqrt{\omega/2}\right).$$

依[[concepts/若尔当引理]]（第 986 页 14.4.3），$y_n\to\infty$ 时 $\widehat{AB}$、$\widehat{CD}$ 上的积分消失；圆周 $\widehat{EF}$ 上的积分保持有界（源文作「留数为 $\varepsilon$」，疑为「半径为 $\varepsilon$」），且 $\varepsilon\to0$ 时积分路径长度趋向于 0，故该项也消失。两个水平线段（源文「万万和」疑为「$\overline{BE}$ 和」）分别按上沿 $p=re^{i\pi}$、下沿 $p=re^{-i\pi}$ 考虑：

```latex
∫_{−∞}^{0} F(p)e^{tp}dp = −∫₀^∞ e^{−tr}·r/(r²+ω²)·e^{−iα√r}dr
∫_{0}^{−∞} F(p)e^{tp}dp = +∫₀^∞ e^{−tr}·r/(r²+ω²)·e^{+iα√r}dr
```

最终：

$$f(t)=e^{-\alpha\sqrt{\omega/2}}\cos\left(\omega t-\alpha\sqrt{\tfrac{\omega}{2}}\right)-\frac{1}{\pi}\int_0^\infty e^{-tr}\,\frac{r\sin\alpha\sqrt r}{r^2+\omega^2}\,\mathrm{d}r.$$

## 复算

- **留数和**：$p=i\omega$ 处 $\operatorname{Res}=\frac{1}{2}e^{i\omega t}e^{-\alpha\sqrt{\omega/2}(1+i)}$，$p=-i\omega$ 处 $\operatorname{Res}=\frac{1}{2}e^{-i\omega t}e^{-\alpha\sqrt{\omega/2}(1-i)}$（用 $\sqrt{\pm i\omega}=\sqrt{\omega/2}(1\pm i)$ 与有理部分在两极点处的留数 $1/2$），两者之和 $=e^{-\alpha\sqrt{\omega/2}}\cos(\omega t-\alpha\sqrt{\omega/2})$。**通过**。
- **两沿积分**：上沿 $p=re^{i\pi}$ ⟹ $\sqrt p=i\sqrt r$、$\mathrm{d}p=-\mathrm{d}r$、$p/(p^2+\omega^2)=-r/(r^2+\omega^2)$，被积式 $=-e^{-tr}\frac{r}{r^2+\omega^2}e^{-i\alpha\sqrt r}\mathrm{d}r$，与源文第一式逐项相符；下沿 $p=re^{-i\pi}$ ⟹ $\sqrt p=-i\sqrt r$，得 $+e^{-tr}\frac{r}{r^2+\omega^2}e^{i\alpha\sqrt r}\mathrm{d}r$，与第二式相符。**通过**。
- **合成**：两沿相加 $=2i\int_0^\infty e^{-tr}\frac{r\sin\alpha\sqrt r}{r^2+\omega^2}\mathrm{d}r$；$(1/2\pi\mathrm{i})\times$ 该值 $=\frac{1}{\pi}\int_0^\infty\cdots$，从留数和中减去即得最终式。**自洽，通过**。
- **小圆消失论证**：被积函数在原点附近有界（$p/(p^2+\omega^2)\to0$），路径长 $2\pi\varepsilon\to0$ ⟹ 贡献 $\to0$——与「半径为 $\varepsilon$」的读法相容，与「留数为 $\varepsilon$」的原文相悖（见[[queries/圆周EF上留数为epsilon疑为半径为epsilon]]）。

## 直接证据与推断

- 直接证据：式 15.46、六段围道方程、留数和表达式、两沿积分、最终式均源文原载。
- 推断（复算）：留数逐项计算、两沿参数化细节、合成步骤为复算者补写。

## 意义

这是本 wiki 首个分支割线围道的完整算例（此前 14.4 的三种围道均不涉及[[concepts/多值函数与主值|多值函数]]），六段归零/归留数的论证已在[[methodology/负实轴分支割线钥匙孔围道逆积分流程]]中流程化。