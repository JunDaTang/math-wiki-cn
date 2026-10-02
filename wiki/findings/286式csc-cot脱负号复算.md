---
type: finding
title: 286 式 csc-cot 脱负号复算
created: 2026-10-02
updated: 2026-10-02
tags: [复算, 校勘, csc, 积分公式]
related: [21-7-3全表逐项求导复算, 三角函数不定积分表, csc与sec积分比较]
source: "[[10-数学手册原书第10版--11-2173-三角函数积分--jenyj9]]"
confidence: high
replicated: true
sources: ["数学手册(原书第10版)/21.7.3 三角函数积分.md"]
---
# 286 式 csc-cot 脱负号复算

条目 286（转写中编号脱落，由 285/287 邻接锚定）为 ∫dx/sin ax。转写原文：

```latex
\int \frac{dx}{\sin ax} = \int \csc ax\,dx = \frac{1}{a}\ln\tan\frac{ax}{2} = \frac{1}{a}\ln(\csc ax \cot ax)
```

## 复算

由半角恒等式 tan(u/2) = csc u − cot u（两端乘 sin u 即验：1 − cos u = tan(u/2)·sin u）：

```latex
\frac{1}{a}\ln\tan\frac{ax}{2} = \frac{1}{a}\ln(\csc ax - \cot ax) \neq \frac{1}{a}\ln(\csc ax \cot ax)
```

同一式内前两个等号成立而末等号不成立：d/dx[ln(csc x − cot x)] = csc x，而 d/dx[ln(csc x·cot x)] = d/dx[ln csc x + ln cot x] = −cot x − tan x = −1/(sin x cos x) ≠ csc x。故末项积性 csc·cot 应为差性 csc − cot，脱一减号。

## 镜像旁证

余弦侧对应条目 325 ∫dx/cos ax = (1/a)Artanh(sin ax) = (1/a)ln tan(ax/2+π/4) = (1/a)ln(sec ax + tan ax) 复算无误，其末项为和式 sec+tan，恰与 csc − cot 构成对偶（[[comparisons/csc与sec积分比较]]）——镜像结构的另一侧无恙，错位定位于 286 末项。

## 附注

该式末尾回指「参见324」疑为 325（[[queries/参见324疑为325之辨]]）。