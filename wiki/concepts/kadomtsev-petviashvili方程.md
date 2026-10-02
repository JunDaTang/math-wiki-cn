---
type: concept
title: Kadomtsev-Petviashvili 方程 (KP)
tags: [偏微分方程, 非线性偏微分方程, 孤子, lump解, 多空间变量]
related: [kdv方程, 非线性发展方程, 广田双线性方法]
created: 2026-10-01
updated: 2026-10-01
sources: ["数学手册(原书第10版)/9.2.5 非线性偏微分方程 孤子、周期模式和混沌.md"]
---

# Kadomtsev-Petviashvili 方程 (KP)

**Kadomtsev-Petviashvili 方程**（KP；源文拼法「Kadomzev-Pedviashwili」为转写乱拼，标准拼法为 Kadomtsev-Petviashvili）是具有较多自变量（例如两个空间变量）的孤子方程的例子（9.2.5.5.6）：

```latex
(u_t + 6 u u_x + u_{xxx})_x = u_{yy}        (9.179a，按转写)
```

它有孤子解（lump 解）

```latex
u(x,y,t) = 2 ∂²/∂x² ln[ 1/k² + |x + i k y − 3k² t|² ]     (9.179b)
```

## 转写疑点：右端疑漏因子 3

复算表明：(9.179b) 的对数宗量 F = 1/k² + (x − 3k²t)² + k²y² 恰好满足双线性方程 (D_xD_t + D_x⁴ − 3D_y²)F·F = 0（D 为广田双线性算子），即 (9.179b) 是

```latex
(u_t + 6 u u_x + u_{xxx})_x = 3 u_{yy}
```

（KPI 型）的精确 lump 解；对按转写的「…_x = u_{yy}」版本代入则得到不恒为零的残差。lump 的速度 3k² 与常数项 1/k² 均只在含因子 3 的版本中自洽。详见 [[queries/式9-179a右端是否漏因子3]] 与 [[findings/式9-172至9-179附加七方程复算]]；双线性核验方法见 [[methodology/广田双线性方法]]。