---
type: query
title: 5.7.6 部分 C 的两表达式是否脱落否定号？
tags: [转写讹误, 布尔表达式, 语义等价, 主正规形式]
related: [布尔表达式, 主正规形式, pdnf与pcnf构造算例, 5-7全节系统性转写讹误清单]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.7 布尔代数和开关代数.md"]
---

# 5.7.6 部分 C 的两表达式是否脱落否定号？

**问题**：手册 5.7.6「主正规形式」小节（部分 C）称下列两表达式与部分 A/B 的函数 $f$ 语义等价（主正规形式相同）；但按转写文本两式均不等于 $f$。是否脱落否定号？

## 转写文本

1. $(y\sqcap z)\sqcup(x\sqcap y\sqcap\bar z)$
2. $(x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup z)\sqcap(\bar y\sqcup\bar z)))\cap(\bar x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup z)))$

## 反例（已复算）

$f$ 的真值表：$f=1$ 恰在 $(x,y,z)=(0,0,1),(1,0,1),(1,1,0)$。

- 表达式 1 在 $(0,0,1)$ 处：$y\sqcap z=0\sqcap 1=0$，$x\sqcap y\sqcap\bar z=0$，得 $0\neq 1$。
- 表达式 2 在 $(1,1,0)$ 处：第一个大因子 $=1$，第二个因子 $=\bar x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup z))=0\sqcup(1\sqcap 0)=0$，得 $0\neq 1$。

## 复原（高置信；复原后已逐点复算，与 PDNF 一致）

1. $(\bar y\sqcap z)\sqcup(x\sqcap y\sqcap\bar z)$——第一个合取的 $y$ 上脱杠；
2. $(x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup z)\sqcap(\bar y\sqcup\bar z)))\sqcap(\bar x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup\bar z)))$——末项基本析取应为 $(\bar y\sqcup\bar z)$ 而非 $(\bar y\sqcup z)$；另两因子间的「$\cap$」为「$\sqcap$」之转写混用。

复原后两式在全部 8 个赋值点上与 $f$ 一致，与源「语义等价」断言吻合（两者的主正规形式与 PDNF/PCNF 相同）。