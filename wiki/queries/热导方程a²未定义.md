---
type: query
title: 热导方程 a² 未定义
created: 2026-10-01
updated: 2026-10-01
tags: [定义缺口, 热传导方程, 热导方程, a²]
related: [热传导方程, 热导方程例中cλ疑为cρ]
sources: ["数学手册(原书第10版)/13.3 向量场中的积分.md"]
---

# 热导方程 a² 未定义

## 疑点

13.3.3 例 C 末尾：均匀物体（$c,\varrho,\lambda$ 均为常数）时热导方程化为 $\partial T/\partial t=a^{2}\triangle T$，但 $a^{2}$ 在本节未给出定义。

## 分析

由推导链的常数情形 $c\varrho\,\partial T/\partial t=\lambda\triangle T$ 可知 $a^{2}=\lambda/(c\varrho)$（即热扩散率/导温系数的平方），此为推断而非原文明示；可能原书在他处（脚注或相应章节）给出定义而转写丢失，也可能手册体例默认读者已知。注意：此推断依赖 [[热导方程例中cλ疑为cρ]] 中 $c\varrho$（而非 $c\lambda$）的更正成立。

## 待办

- 原书扫描页确认 $a^{2}$ 的定义是否在别处给出；
- 后续偏微分方程章节入库时回填。