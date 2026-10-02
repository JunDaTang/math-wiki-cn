---
type: concept
title: Oseledec定理
created: 2026-10-01
updated: 2026-10-01
tags: [遍历论, 动力系统, 李雅普诺夫指数, 乘性遍历定理]
related: [李雅普诺夫指数, 矩阵奇异值, 遍历不变测度, Oseledec, 变分方程]
sources: ["数学手册(原书第10版)/17.2.3 李雅普诺夫指数.md"]
---

# Oseledec 定理

Oseledec 定理（又称乘性遍历定理）是遍历论的核心定理之一，以 [[entities/Oseledec]] 命名。就本源（17.2.3 第 2 小节）所载内容而言，它断言：设 $\{\varphi^t\}$ 为 $M \subset \mathbb{R}^n$ 上的光滑动力系统，$\varLambda$ 为吸引子，$\mu$ 为支撑在 $\varLambda$ 上的遍历不变概率测度，则对 $\mu$-几乎处处 $x$：

1. **指数谱存在**：存在一列数 $\lambda_1 \geqslant \cdots \geqslant \lambda_n$（即 [[concepts/李雅普诺夫指数]]），使 $\frac{1}{t}\ln\sigma_i(t,x) \to \lambda_i$，其中 $\sigma_i(t,x)$ 为 $D\varphi^t(x)$ 的第 $i$ 个奇异值（收敛口径的转写疑点见 [[queries/李雅普诺夫指数收敛方式L1与几乎处处之辨]]）；
2. **子空间滤链**（式 17.38）：

$$
\mathbb{R}^{n} = E_{s_1}^{x} \supset E_{s_2}^{x} \supset \dots \supset E_{s_{r+1}}^{x} = \{0\},\tag{17.38}
$$

且 $\frac{1}{t}\ln\|D\varphi^t(x)v\|$ 关于 $v \in E_{s_j}^{x} \backslash E_{s_{j+1}}^{x}$ **一致地**收敛于谱 $\{\lambda_1, \cdots, \lambda_n\}$ 中的某个元素 $\lambda_{s_j}$。

滤链的层差 $E_{s_j}^{x} \backslash E_{s_{j+1}}^{x}$ 给出方向指数的分层：同一层差上的方向具有相同的指数增长率，不同层差对应谱中相异的取值（相异值个数 $r \leqslant n$；此结构性解读为编者依定义推得）。转录复算见 [[findings/式17-38Oseledec滤链转录复算]]。

## 意义

- 定理把 [[concepts/李雅普诺夫指数]] 从启发式量提升为良定义对象；
- 是指数和公式 (17.39a)/(17.39b) 与熵关系（[[concepts/佩辛熵公式]]、[[concepts/测度熵与正指数和不等式]]）的共同前提；
- 一致收敛性是其强于「逐方向极限存在」之处（源文强调）。