---
type: concept
title: D 与 Dt 微分命令
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 求导, 偏导数, 全微分]
related: [Derivative微分算子, 纯函数（Mathematica）, mathematica]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---
# D 与 Dt 微分命令

Mathematica 应用分析运算的求导命令（表 20.12），是 [[concepts/Derivative微分算子]] 的落地命令：在第 1341 页 20.2.8 导数概念作为函数算子被引入，其完整形式 Derivative[n₁, n₂, …]（式 20.34）是一个偏微分算子——自变量表明该函数关于目前变元要求多少次导；就此意义而言，Mathematica 试图将这一结果表示为一个纯函数。已知函数的求导可以用算子 D 以一种简化的方式来进行：D[f[x], x] 将确定函数 f 在自变量 x 处的导数。

## 表 20.12 求导运算

| 命令 | 释义 |
|---|---|
| D[f[x], {x, n}] | 得到函数 f(x) 关于 x 的 n 阶导数 |
| D[f, {x1, n1}, {x2, n2},···] | 多重导数,关于 xi (i = 1,2,···)的 ni 阶导数 |
| Dt[f] | 函数 f 的全微分 |
| Dt[f, x] | 函数 f 的全导数 df/dx |
| Dt[f, x1, x2,···] | 多元函数的全导数 |

## 语义要点与源例

- **任意阶与偏导数**：D[f[x], {x, n}]；多重导数 D[f, {x1,n1}, {x2,n2}, …]。
- **全微分与全导数**：Dt[f] 得全微分（例 C：Dt[x³+y³] = 3x²Dt[x] + 3y²Dt[y]）；Dt[f, x] 得全导数 df/dx（例 D：Dt[x³+y³, x] = 3x² + 3y²Dt[y,x]）——Mathematica 假定 y 是 x 的未知函数，它是未知的，因此该导数的第二部分以符号方式 Dt[y,x] 写出。源文认为更可取的书写形式为 D[x³ + y[x]³, x] 之类，明确显示独立变元（源印此句讹残，见 [[queries/20-3全节系统性转写讹误清单]]）。
- **符号函数保持一般形式**：如果 Mathematica 在计算导数时发现一个符号函数，则保持这个一般形式、用 f′ 表示其导数（例 E：D[x f[x]³, x] = f[x]³ + 3x f[x]² f′[x]）。
- **形式求导法则**：Mathematica 知道乘积和商的求导法则，也知道链式法则并能形式地应用（例 F：D[f[u[x]], x] = f′[u[x]] u′[x]；例 G：D[u[x]/v[x], x] = u′[x]/v[x] − u[x]v′[x]/v[x]²）。例 G 行号印作 In[17]/Out[z]，疑为 In[1]/Out[1]（见 [[queries/In17与Out-z疑为In1与Out1之辨]]）。
- 例 A、B（显式函数求导，含 (2x+1)^{3x} 之对数求导）见 [[findings/20-3-4微分与积分算例复算]]。

## 关联

[[concepts/Derivative微分算子]]（算子语义）、[[concepts/纯函数（Mathematica）]]（结果表示为纯函数）。