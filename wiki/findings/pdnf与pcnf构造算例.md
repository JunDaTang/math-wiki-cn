---
type: finding
title: PDNF 与 PCNF 构造算例（式 5.312–5.313，已复算）
source: "[[10-数学手册原书第10版--12-57-布尔代数和开关代数--1ua6pjv]]"
confidence: high
replicated: true
tags: [主正规形式, PDNF, PCNF, 算例, 语义等价]
related: [主正规形式, 布尔表达式, 由真值表构造pdnf与pcnf流程, pdnf与pcnf比较, 部分c两表达式是否脱落否定号]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.7 布尔代数和开关代数.md"]
---

# PDNF 与 PCNF 构造算例（式 5.312–5.313，已复算）

手册 5.7.6（部分 A/B）以一个三变量布尔函数演示 PDNF 与 PCNF 的构造。真值表（转写完整）：

| x | y | z | f(x,y,z) |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 |

**PDNF**（基本合取对应 $f=1$ 的赋值 001、101、110；变量值 1 取本身、值 0 取否定）：

$$(\bar x\sqcap\bar y\sqcap z)\sqcup(x\sqcap\bar y\sqcap z)\sqcup(x\sqcap y\sqcap\bar z).\tag{5.312}$$

**PCNF**（基本析取对应 $f=0$ 的赋值 000、010、011、100、111；变量值 1 取否定、值 0 取本身）：

$$(x\sqcup y\sqcup z)\sqcap(x\sqcup\bar y\sqcup z)\sqcap(x\sqcup\bar y\sqcup\bar z)\sqcap(\bar x\sqcup y\sqcup z)\sqcap(\bar x\sqcup\bar y\sqcup\bar z).\tag{5.313}$$

**复算结论（直接复算）**：$f=1$ 恰在赋值 001、101、110，$f=0$ 恰在 000、010、011、100、111；式 (5.312) 的三个基本合取与 (5.313) 的五个基本析取逐一对应上述赋值，两式与真值表完全吻合，转写无误。

## 部分 C：语义等价算例（含复原）

源（5.7.6「主正规形式」小节）称下列两表达式与上例函数语义等价（主正规形式相同）。**按转写文本两式均不等于 $f$，各脱落否定号**；高置信复原如下（复原后已在全部 8 个赋值点上逐点复算，与 PDNF 一致）：

1. $(\bar y\sqcap z)\sqcup(x\sqcap y\sqcap\bar z)$——转写为 $(y\sqcap z)\sqcup(\cdots)$，第一个合取的 $y$ 上脱杠；
2. $(x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup z)\sqcap(\bar y\sqcup\bar z)))\sqcap(\bar x\sqcup((y\sqcup z)\sqcap(\bar y\sqcup\bar z)))$——转写末项基本析取为 $(\bar y\sqcup z)$，应为 $(\bar y\sqcup\bar z)$；另两因子间的「$\cap$」为「$\sqcap$」之转写混用。

详见 [[queries/部分c两表达式是否脱落否定号]]。