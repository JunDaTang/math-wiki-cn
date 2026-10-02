---
type: concept
title: "DFP 方法"
created: 2026-10-01
updated: 2026-10-01
tags: [无约束优化, 拟牛顿法, DFP方法]
related: [戴维顿, 弗莱彻, 鲍威尔, 线搜索, 黑塞矩阵, 共轭梯度法, 牛顿法（无约束优化）]
sources: ["数学手册(原书第10版)/18.2.5 无约束问题的解法.md"]
---
# DFP 方法

DFP 方法（Davidon–Fletcher–Powell 方法，18.2.5.4；命名人见 [[entities/戴维顿]]、[[entities/弗莱彻]]、[[entities/鲍威尔]]）是逐步逼近逆黑塞矩阵的无约束优化迭代法：

$$
\boldsymbol{x}^{k+1} = \boldsymbol{x}^{k} - \alpha_k \boldsymbol{M}_k \nabla f(\boldsymbol{x}^{k}) \quad (k=1,2,\dots), \tag{18.84}
$$

其中 M_k 为对称正定矩阵，步长 α_k 沿方向 −M_k∇f(x^k) 由 [[concepts/线搜索]]（18.86）确定。

## 核心思想（源断言）

f 为二次函数时，方法的想法是逆黑塞矩阵由 M_k 逐步近似：从对称正定矩阵 M₁（例如 M₁=I）出发，M_k 由 M_{k−1} 加上一个秩修正矩阵（原文脱秩数，按更新式为两个秩一矩阵之和，疑为「秩 2」，见 [[queries/秩修正矩阵脱秩数之辨]]）确定：

$$
\boldsymbol{M}_k = \boldsymbol{M}_{k-1} + \frac{\boldsymbol{v}^{k} \boldsymbol{v}^{k\mathrm{T}}}{\boldsymbol{v}^{k\mathrm{T}} \boldsymbol{v}^{k}}
  - \frac{(\boldsymbol{M}_{k-1}\boldsymbol{w}^{k})(\boldsymbol{M}_{k-1}\boldsymbol{w}^{k})^{\mathrm{T}}}{\boldsymbol{w}^{k\mathrm{T}} \boldsymbol{M}_k \boldsymbol{w}^{k}}, \tag{18.85}
$$

其中 v^k = x^k−x^{k−1}（位移），w^k = ∇f(x^k)−∇f(x^{k−1})（梯度差），k=2,3,…。若 f 是二次函数，则 DFP 方法变成 [[concepts/共轭梯度法]]（相应初始 M₁=I）。

## 重要疑点：式 18.85 的分母

照印的 18.85 不满足拟牛顿（割线）方程 M_k w^k = v^k，且末分母含 M_k 自指（用被定义量定义自身），与「M_k 由 M_{k−1} 确定」的递归表述冲突。将首分母改为 v^{kT}w^k、末分母改为 w^{kT}M_{k−1}w^k（标准 DFP 形式）后割线方程成立。复算细节见 [[findings/式18-84至18-86DFP更新公式转录复算]]，疑点追踪见 [[queries/式18-85首分母vkTvk疑为vkTwk且末分母下标Mk疑为Mk-1之辨]]。

## 延伸概念（后人术语，非源用语）

源文档描述了「逆黑塞矩阵由 M_k 逐步近似」与「秩修正」的思想，但未使用「拟牛顿法」（quasi-Newton）/「变度量法」等名称；此类术语系后人对该思想家族的归纳，此处仅作指引，不应记为源文档主张。

## 流程与比较

[[methodology/DFP方法矩阵修正与线搜索流程]]、[[comparisons/四种无约束优化方法比较]]。