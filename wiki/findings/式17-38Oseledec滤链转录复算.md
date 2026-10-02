---
type: finding
title: 式 17.38 Oseledec 滤链转录复算
created: 2026-10-01
updated: 2026-10-01
tags: [转录复算, Oseledec定理, 李雅普诺夫指数]
related: [Oseledec定理, 李雅普诺夫指数, 遍历不变测度, 17-2-3全节系统性转写讹误清单]
sources: ["数学手册(原书第10版)/17.2.3 李雅普诺夫指数.md"]
source: "[[10-数学手册原书第10版--12-1723-李雅普诺夫指数--g5uoaj]]"
confidence: high
replicated: null
---

# 式 17.38 Oseledec 滤链转录复算

## 转录（源文逐字）

对 $\mu$-几乎处处 $x$，存在 $\mathbb{R}^n$ 的一列子空间

$$
\mathbb{R}^{n} = E_{s_1}^{x} \supset E_{s_2}^{x} \supset \dots \supset E_{s_{r+1}}^{x} = \{0\},\tag{17.38}
$$

满足 $\frac{1}{t}\ln\|D\varphi^t(x)v\|$ 关于 $v \in E_{s_j}^{x} \backslash E_{s_{j+1}}^{x}$ 一致地收敛于 $\{\lambda_1, \cdots, \lambda_n\}$ 中某元素 $\lambda_{s_j}$。

## 结构核验（编者推演，直接证据为源文公式本身）

1. **滤链良序**：$E_{s_1}^x = \mathbb{R}^n$、$E_{s_{r+1}}^x = \{0\}$，中间严格递降；相异指数值个数 $r \leqslant n$（谱 $\{\lambda_1, \cdots, \lambda_n\}$ 按重数计 $n$ 个，相异值至多 $n$ 个）。
2. **层差口径自洽**：层差 $E_{s_j}^x \backslash E_{s_{j+1}}^x$ 上的方向共享同一指数 $\lambda_{s_j}$；由 $\lambda_1 \geqslant \cdots \geqslant \lambda_n$ 的排序，滤链越深对应指数越小（最外层 $E_{s_1} \backslash E_{s_2}$ 承载最大指数 $\lambda_1$，最深非零层承载最小指数）。〔此排序对应为编者依定义推得。〕
3. **一致收敛**：源文强调对 $v$ 的一致收敛，这是滤链表述强于「逐方向极限存在」之处。

## 转写问题

- 「关千 $v$」→「关于 $v$」、「收敛千」→「收敛于」（「千」为「于」之形近误植，全节多处）；
- 谱集合 $\{\lambda_1, \cdots, \lambda_n\}\}$ 尾部多一全角右花括号；
- 上文指数定义处「对µ μ-∧ 乎处处 x」乱码，疑为「对 μ-几乎处处 x」。

均录入 [[queries/17-2-3全节系统性转写讹误清单]]。

## 证据评估

直接证据：源文式 (17.38) 及其上下文。定理本身为标准结果（乘性遍历定理），本复算仅核验转录文本的内部自洽性，未做数值复现（replicated: null）。