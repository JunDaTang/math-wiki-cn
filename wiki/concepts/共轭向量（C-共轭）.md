---
type: concept
title: "共轭向量（C-共轭）"
created: 2026-10-01
updated: 2026-10-01
tags: [无约束优化, 线性代数, 共轭梯度法]
related: [共轭梯度法, 凸优化, 黑塞矩阵]
sources: ["数学手册(原书第10版)/18.2.5 无约束问题的解法.md"]
---
# 共轭向量（C-共轭）

相对对称正定矩阵 C，两个向量 d¹, d² 称作（C-）共轭向量，是指

$$
\boldsymbol{d}^{1\mathrm{T}} \boldsymbol{C}\, \boldsymbol{d}^{2} = 0. \tag{18.81}
$$

即 d¹ 与 Cd² 在通常内积下正交；C = I 时退化为普通正交（此特例说明为维基补充，非源原文）。

## 意义（源断言）

若 d¹, d², …, dⁿ 相对 C 两两共轭，则凸二次问题 $q(\boldsymbol{x})=\boldsymbol{x}^{\mathrm{T}}\boldsymbol{C}\boldsymbol{x}+\boldsymbol{p}^{\mathrm{T}}\boldsymbol{x}$（x∈ℝⁿ）可以经 n 步求解：从 x¹ 出发构建 x^{k+1}=x^k+α_k d^k，α_k 取最优步长。这是 [[concepts/共轭梯度法]] 的理论基础。

## 转写说明

源文档此段讹误密集：「相对千对称正定矩阵 是共谓向量」——「千」为「于」之讹、两处脱矩阵符号 C、「共谓」为「共轭」之讹；「d¹,…,dⁿ 矿相对千矩阵 是两两共辄的」中「矿」为乱码。见 [[queries/18-2-5全节系统性转写讹误清单]]。

## 相关

[[concepts/共轭梯度法]]、[[concepts/凸优化]]、[[concepts/黑塞矩阵]]（C ≈ ½H(x*) 的对应，Hess(xᵀCx+pᵀx)=2C）。