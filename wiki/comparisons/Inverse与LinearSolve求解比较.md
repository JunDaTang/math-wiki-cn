---
type: comparison
title: "Inverse 与 LinearSolve 求解比较"
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, 线性方程组, 比较]
related: [线性方程组求解命令, 线性方程组三例与NullSpace复算, 算例B克拉默方程组逆矩阵求解复算]
sources: ["数学手册(原书第10版)/20.3 Mathematica的重要应用.md"]
---

# Inverse 与 LinearSolve 求解比较

本比较依据《数学手册（原书第10版）》20.3.3（本页 frontmatter `sources` 所列源文件），对 Mathematica 求解线性方程组 P.X == B 的两条路径作对照。

## 对照表

| 维度 | X = Inverse[P].B | LinearSolve[P, B] |
|---|---|---|
| 适用情形 | 特殊情形 n = m 且 det P ≠ 0（唯一解） | 一般情形：与 NullSpace 配合可处理所有可能的情形（先确定是否存在解，存在则算出） |
| 副产品 | 显式得到逆矩阵 Inverse[P] | 无逆矩阵副产品，直接得解向量 |
| 性能（书中断言） | 较慢；可在合理时间内处理最多约 5000 个左右未知数的此类方程组（「依赖于计算机系统」） | 「将更快地得到一个等价的解」 |
| 失败行为 | 书中未展开（奇异矩阵情形） | 不相容时触发 LinearSolve::nosol 并将输入作为输出显示（例 B 复算成立，见 [[findings/线性方程组三例与NullSpace复算]]） |

## 语义要点

- Inverse 路径对应逆矩阵理论解 X = P⁻¹B，仅当方阵非奇异时可用；LinearSolve 覆盖超定（例 C：秩 3 的 4×3 系统仍有解 {10/7, −1/7, −2/7}）与不相容（例 B）情形。
- RowReduce 用于判定方程组左边（系数矩阵）的独立性（秩）；NullSpace 给出齐次解空间的一组基（例 A）。
- Thread[P.X == B] 将矩阵等式逐分量展开为方程列表（式 20.32），是构造方程组的输入手段而非求解命令。
- 20.2.5 节中另有以 Inverse[P].B 求解克拉默方程组的同类算例（[[findings/算例B克拉默方程组逆矩阵求解复算]]，其依据为 20.2.5 源文件），可与本节例 C 互证 Inverse 路径的适用面。

## 时代敏感注记

「约 5000 个左右未知数」的规模断言属本书成书时代、且「依赖于计算机系统」，仅属于 Mathematica 的 Inverse/LinearSolve 求解语境，不应外推至现代版本，也不得移植至 Matlab/Maple 等其他系统的页面。

## 关联

[[concepts/线性方程组求解命令]]、[[findings/线性方程组三例与NullSpace复算]]、[[concepts/消息系统（Mathematica）]]（nosol 实例）。