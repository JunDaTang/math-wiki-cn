---
type: finding
title: 整除定义与 DR1–DR12 法则组（式 5.214–5.226）
tags: [数论, 整除性, 法则组, 转写讹误]
related: [整除性, dr4与dr12结论脱落之复原, dr7与dr8的z量词域是否应为自然数]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.4.1 整除性.md"]
source: "[[10-数学手册原书第10版--7-541-整除性--1bgclvy]]"
confidence: high
replicated: null
---

# 整除定义与 DR1–DR12 法则组

## 内容（式 5.214–5.226，含转写复原标注）

定义（5.214）：$b$ 可被 $a$ 整除 ⟺ 存在 $q\in\mathbb{Z}$ 使 $qa=b$；记 $a\mid b$。$a$ 是因子，$q$ 是余因子，$b$ 是 $a$ 的倍数。

| 法则 | 内容 | 式号 | 转写状态 |
|---|---|---|---|
| DR1 | $\forall a\in\mathbb{Z}:\ 1\mid a,\ a\mid a,\ a\mid 0$ | 5.215 | 完整 |
| DR2 | $a\mid b \Rightarrow (-a)\mid b \wedge a\mid(-b)$ | 5.216 | 完整 |
| DR3 | $a\mid b \wedge b\mid a \Rightarrow a=b \vee a=-b$ | 5.217 | 完整 |
| DR4 | $a\mid 1 \Rightarrow$（脱落；按标准应复原为 $a=\pm 1$） | 5.218 | ⚠ |
| DR5 | $a\mid b \wedge b\neq 0 \Rightarrow \lvert a\rvert\leqslant\lvert b\rvert$ | 5.219 | 完整 |
| DR6 | $a\mid b \Rightarrow a\mid(zb)$（源文「alzb」） | 5.220 | ⚠ 复原 |
| DR7 | $a\mid b \Rightarrow a^z\mid b^z$（源文「azlbz」） | 5.221 | ⚠ 域存疑 |
| DR8 | $a^z\mid b^z \wedge b\neq 0 \Rightarrow a\mid b$（源文「DRS」「b-/-」） | 5.222 | ⚠ |
| DR9 | $a\mid b \wedge b\mid c \Rightarrow a\mid c$（结论脱落） | 5.223 | ⚠ 复原 |
| DR10 | $a\mid b \wedge c\mid d \Rightarrow ac\mid bd$（结论脱落） | 5.224 | ⚠ 复原 |
| DR11 | $a\mid b \wedge a\mid c \Rightarrow a\mid(z_1 b+z_2 c)$ | 5.225 | 完整 |
| DR12 | 整条脱落，仅存 $a\mid b$ | 5.226 | ⚠ 需原书复原 |

## 复核说明

- 法则组与标准初等数论一致（直接证据：DR1–DR3、DR5、DR11 原文完整且正确；推断：DR4/DR9/DR10 按标准结果复原）。
- DR7/DR8 转写作「对每个 $z\in\mathbb{Z}$」，但 DR8 取 $z=0$ 时由 $1\mid 1$ 将推出任意 $a\mid b$（假），域应为 $\mathbb{N}$ 或 $z\geqslant 1$，见 [[queries/dr7与dr8的z量词域是否应为自然数]]。
- 本 finding 为命题组转写，无数值算例可复算（replicated: null）；引用 DR4/DR9/DR10/DR12 原文前须校勘。

## 边界

法则组属 [[concepts/整除性]] 在 $\mathbb{Z}$ 上的内容；多项式环上的整除理论另见 [[concepts/带余除法与欧几里得算法]]（5.3.7），不可互相挪用。
