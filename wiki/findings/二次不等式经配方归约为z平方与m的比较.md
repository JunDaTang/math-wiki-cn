---
type: finding
title: "二次不等式经配方归约为 z 平方与 m 的比较（式 1.129–1.130）"
created: 2026-09-29
updated: 2026-09-29
tags: [不等式, 配方法, 求解程序, 数学手册]
related: [10-数学手册原书第10版--6-14-不等式--z8nyhr, 线性与二次不等式的求解, 不等式, 数区间]
sources: ["数学手册(原书第10版)/1.4 不等式.md"]
source: "10-数学手册原书第10版--6-14-不等式--z8nyhr"
confidence: high
replicated: true
---
# 二次不等式经配方归约为 z 平方与 m 的比较（式 1.129–1.130）

《数学手册(原书第10版)》1.4.3 把一般二次不等式的求解化归为最简形式 $z^2 \gtrless m$ 的四种情形：

1. 一般形式 $ax^2+bx+c > 0$ (1.129a) 或 $< 0$ (1.129b)，两边除以 $a$（$a<0$ 时变号），归为 $x^2+px+q < 0$ (1.129c) 或 $> 0$ (1.129d)；
2. 配方：$\left(x+\frac{p}{2}\right)^2 < \left(\frac{p}{2}\right)^2 - q$ (1.129e) 或 $>$ (1.129f)；
3. 代换 $z = x+\frac{p}{2}$、$m = \left(\frac{p}{2}\right)^2 - q$，得 $z^2 < m$ (1.130a) 或 $z^2 > m$ (1.130b)；
4. 按 (1.127)/(1.128) 求解：$z^2>m$ 时，$m\ge 0$ 给 $\lvert z\rvert>\sqrt{m}$、$m<0$ 恒成立；$z^2<m$ 时，$m>0$ 给 $\lvert z\rvert<\sqrt{m}$、$m\le 0$ 无解。

## 例题复核

- 线性例 (1.125b)：$5x+3<8x+1 \Rightarrow -3x<-2 \Rightarrow x>\frac{2}{3}$ ——正确
- 例 A：$-2x^2+14x-20>0 \Rightarrow x^2-7x+10<0 \Rightarrow \left(x-\frac{7}{2}\right)^2<\frac{9}{4} \Rightarrow 2<x<5$ ——正确
- 例 B：$x^2+6x+15>0 \Rightarrow (x+3)^2>-6$，恒成立 ——正确
- 例 C：$-2x^2+14x-20<0 \Rightarrow \left(x-\frac{7}{2}\right)^2>\frac{9}{4} \Rightarrow x>5$ 或 $x<2$ ——正确

四例经 wiki 逐项复核数值全部正确，与 1.3 商业数学存在数值排印错误（[[findings/式1.96示例7.76应为约7.86]]）形成对照。

## 评估

- **证据类型**：直接证据（手册原文程序与例题）；例题数值经独立复核一致。
- **置信度**：高。
- 概念页：[[concepts/线性与二次不等式的求解]]。