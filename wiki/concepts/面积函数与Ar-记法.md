---
type: concept
title: "面积函数与 Ar- 记法"
created: 2026-10-02
updated: 2026-10-02
tags: [反双曲函数, 面积函数, Ar-记法, 幂级数, 渐近展开, 译名]
related: [对数函数级数展开, 反三角函数级数展开, Arcosh负六次方项系数不自洽复算, Arcosh第三项分母疑脱6之辨]
sources: ["数学手册(原书第10版)/21.5 重要级数展开.md"]
---

# 面积函数与 Ar- 记法

「面积函数」是本手册对反双曲函数（德文 *Areafunktion*）的译名，以 Ar- 前缀记作 $\Arsinh$、$\Arcosh$、$\Artanh$、$\Arcoth$。本页依据 [[sources/10-数学手册原书第10版--10-215-重要级数展开--1gmcxgd]] 的面积函数块整理；该记法亦出现于对数函数块的两行商对数式（[[concepts/对数函数级数展开]]）。

## 四函数的级数

$$\Arsinh x=x-\frac{1}{2\cdot3}x^3+\frac{1\cdot3}{2\cdot4\cdot5}x^5-\frac{1\cdot3\cdot5}{2\cdot4\cdot6\cdot7}x^7+\cdots+(-1)^n\frac{1\cdot3\cdots(2n-1)}{2\cdot4\cdots(2n)(2n+1)}x^{2n+1}\pm\cdots,\quad \lvert x\rvert<1$$

$$\Arcosh x=\pm\left[\ln(2x)-\frac{1}{2\cdot2x^2}-\frac{1\cdot3}{2\cdot4\cdot4x^4}-\frac{1\cdot3\cdot5}{2\cdot4\cdot6x^6}-\cdots\right],\quad x>1$$

$$\Artanh x=x+\frac{x^3}{3}+\frac{x^5}{5}+\frac{x^7}{7}+\cdots+\frac{x^{2n+1}}{2n+1}+\cdots,\quad \lvert x\rvert<1$$

$$\Arcoth x=\frac{1}{x}+\frac{1}{3x^3}+\frac{1}{5x^5}+\frac{1}{7x^7}+\cdots+\frac{1}{(2n+1)x^{2n+1}}+\cdots,\quad \lvert x\rvert>1$$

## 要点

- $\Arsinh$ 与 $\arcsin$ 的双阶乘通项仅差 $(-1)^n$ 交错，二者互为复算印证（[[concepts/反三角函数级数展开]]）。
- $\Artanh$、$\Arcoth$ 分别与 $\ln\frac{1+x}{1-x}=2\,\mathrm{Artanh}\,x$、$\ln\frac{x+1}{x-1}=2\,\mathrm{Arcoth}\,x$ 两行逐项相同，收敛域亦一致。
- $\Arcosh$ 行是围绕 $x\to\infty$ 的 $x^{-2}$ 幂展开（首项 $\ln(2x)$，$x>1$ 时收敛于 $\Arcosh x-\ln(2x)$）；前置 $\pm$ 表示因 $\cosh$ 为偶函数所致的双分支（$\pm\Arcosh x$ 均满足 $\cosh u=x$）。其 $x^{-6}$ 项系数与复算不自洽，疑分母脱「·6」（[[findings/Arcosh负六次方项系数不自洽复算]]、[[queries/Arcosh第三项分母疑脱6之辨]]）。
- **记法与译名知识点**：德文原书用 *Areafunktion* 与 Ar- 前缀（Arsinh/Arcosh/Artanh/Arcoth），与英文文献常见的 asinh/arcosh（或 arsinh/arcosh、$\sinh^{-1}$ 等）记法不同，跨源引用时须注意区分。