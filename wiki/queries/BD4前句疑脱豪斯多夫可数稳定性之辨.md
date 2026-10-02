---
type: query
title: BD4 前句疑脱豪斯多夫可数稳定性对照之辨
created: 2026-10-01
updated: 2026-10-01
tags: [讹误辨析, 盒维数, 豪斯多夫维数, 转录校勘, 脱文]
related: [concepts/盒维数（容量）, concepts/豪斯多夫测度与豪斯多夫维数, findings/式17-41至17-42豪斯多夫维数与盒维数转录复算, comparisons/豪斯多夫维数与盒维数比较, queries/17-2-4全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/17.2.4 维数.md"]
---
# BD4 前句疑脱豪斯多夫可数稳定性对照之辨

## 现状

源文 (BD4) 作：「如果 $A=\bigcup_nA_n$ 一般地对盒维数，等式 $d_B(A)=\sup_nd_B(A_n)$ 不成立」。前半句「如果 $A=\bigcup_nA_n$」悬空无谓语，疑其后的对照从句整段脱文。

## 疑点

按体例，(BD4) 应与 (HD4) 对照成文，原句疑为：「如果 $A=\bigcup_nA_n$，**则 $d_H(A)=\sup_nd_H(A_n)$（HD4），** 一般地对盒维数，等式 $d_B(A)=\sup_nd_B(A_n)$ 不成立」。脱去的正是点明两维数差异的关键对照（豪斯多夫维数可数稳定、盒维数不可数稳定）。

## 佐证

- (HD4) 的表述完整：「$A=\bigcup_{i=1}^\infty A_i\Rightarrow d_H(A)=\sup_id_H(A_i)$」；
- 本节随后用 $\mathbb{Q}\cap[0,1]$（$d_B=1>0=\sup$ 单点维数）隐含展示了盒维数不可数稳定，恰是该对照的实例。

## 待办

- 查印本 (BD4) 原句；
- 确认后回填 [[concepts/盒维数（容量）]] 与 [[comparisons/豪斯多夫维数与盒维数比较]]。