---
type: comparison
title: csc 与 sec 积分比较
created: 2026-10-02
updated: 2026-10-02
tags: [积分表, 结构比较, csc, sec, 级数]
related: [三角函数不定积分表, 正弦与余弦积分小节平行结构比较, 伯努利与欧拉数级数积分比较, 286式csc-cot脱负号复算]
sources: ["数学手册(原书第10版)/21.7.3 三角函数积分.md"]
---
# csc 与 sec 积分比较

条目 286–292（csc 族）与 325–331（sec 族）逐条镜像。本比较基于 [[sources/10-数学手册原书第10版--11-2173-三角函数积分--jenyj9]]。

## 逐条对照

| 功能 | csc 侧 | sec 侧 | 镜像关系 |
|---|---|---|---|
| 一次倒数 | 286：(1/a)ln tan(ax/2) = (1/a)ln(csc ax − cot ax)〔订正〕 | 325：(1/a)Artanh(sin ax) = (1/a)ln tan(π/4+ax/2) = (1/a)ln(sec ax + tan ax) | 半角移位 + 差式↔和式 |
| 二次 | 287：−(1/a)cot ax | 326：(1/a)tan ax | 符号翻转 |
| 三次 | 288：−cos/(2a sin²) + (1/2a)ln tan(ax/2) | 327：sin/(2a cos²) + (1/2a)ln tan(π/4+ax/2) | 逐项对应 |
| n 次 | 289 递推 | 328 递推 | 递推同型 |
| x 因子 | 290：Bernoulli 数奇幂级数 | 329：Euler 数偶幂级数 | Bernoulli↔Euler 对偶 |
| x·二次 | 291：−(x/a)cot + (1/a²)ln sin | 330：(x/a)tan + (1/a²)ln cos | 逐项对应 |
| x·n 次 | 292 递推 | 331 递推 | 递推同型 |

## 290 与 329 的级数对照

```latex
% 290：奇次幂，Bernoulli 数
\int\frac{x\,dx}{\sin ax} = \frac{1}{a^{2}}\left(ax + \frac{(ax)^{3}}{18} + \frac{7(ax)^{5}}{1800} + \cdots + \frac{2(2^{2n-1}-1)B_{n}(ax)^{2n+1}}{(2n+1)!} + \cdots\right)
% 329：偶次幂，Euler 数
\int\frac{x\,dx}{\cos ax} = \frac{1}{a^{2}}\left(\frac{(ax)^{2}}{2} + \frac{(ax)^{4}}{8} + \frac{5(ax)^{6}}{144} + \cdots + \frac{E_{n}(ax)^{2n+2}}{(2n+2)(2n)!} + \cdots\right)
```

csc 展开只含奇次幂（sin 为奇函数）、sec 只含偶次幂（cos 为偶函数），通项分别由 Bernoulli 数（带 2(2^{2n−1}−1) 因子）与 Euler 数承载——两族系数均经全量核对无误（[[findings/三角积分伯努利欧拉级数系数复算]]、[[comparisons/伯努利与欧拉数级数积分比较]]）。

## 校勘交叉

286 的 ln(csc·cot) 讹误恰以 325 的正确和式 sec+tan 为镜像旁证：半角恒等式 tan(u/2) = csc u − cot u 与 tan(π/4+u/2) = sec u + tan u 对偶（[[findings/286式csc-cot脱负号复算]]）。