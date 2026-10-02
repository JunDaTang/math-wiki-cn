---
type: finding
title: 标准形生成流程 C = UD（式 4.206–4.208）
tags: [线性代数, 二次型, 主轴变换]
related: [二次型, 主轴变换, 西尔维斯特惯性定理, 标准形与西尔维斯特惯性定理]
source: "[[10-数学手册原书第10版--10-46-矩阵特征值问题--f9s58z]]"
confidence: high
replicated: null
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/4.6 矩阵特征值问题.md"]
---

# 标准形生成流程 C = UD（式 4.206–4.208）

**发现**：4.6.2.3 第 3 条给出由主轴变换生成标准形的实用流程：**旋转 + 伸缩**，总变换 $C=UD$。

1. **旋转**：首先通过正交矩阵 $U$ 实施坐标系的旋转，$U$ 的各列是 $A$ 的特征向量（新坐标系的轴的方向是特征向量的方向），给出

$$Q=\widetilde{\underline{x}}^{\mathrm{T}}\boldsymbol{L}\widetilde{\underline{x}}=\sum_{i=1}^{r}\lambda_i\widetilde{x}_i^2,\tag{4.206}$$

$L$ 为对角元为特征值的对角矩阵。

2. **伸缩**：然后通过对角矩阵 $D$ 实施伸缩，其对角元是 $d_i=\sqrt{k_i/|\lambda_i|}$；整个变换由

$$\boldsymbol{C}=\boldsymbol{U}\boldsymbol{D}\tag{4.207}$$

给出，并且

$$Q=(\boldsymbol{U}\boldsymbol{D}\widetilde{\underline{x}})^{\mathrm{T}}\boldsymbol{A}(\boldsymbol{U}\boldsymbol{D}\widetilde{\underline{x}})=\widetilde{\underline{x}}^{\mathrm{T}}\boldsymbol{D}^{\mathrm{T}}\boldsymbol{L}\boldsymbol{D}\widetilde{\underline{x}}=\widetilde{\underline{x}}^{\mathrm{T}}\boldsymbol{K}\widetilde{\underline{x}}.\tag{4.208}$$

⚠ 转写讹误：源文 (4.208) 首项误作 $Q=\widetilde{\underline{x}}^{\mathrm{T}}A\widetilde{\underline{x}}$；按 $\underline{x}=UD\widetilde{\underline{x}}$（式 4.204、4.207），首项应为 $\underline{x}^{\mathrm{T}}A\underline{x}$，见 [[queries/式4-208首项是否应为xTAx]]。另注意记号 $D$ 一词两义：(4.198) 中为特征值对角阵，此处为伸缩对角阵（特征值对角阵改记 $L$）。

**应用**：二次型的主轴变换在二阶曲线和曲面的分类中起本质性作用（手册引 3.5.2.11、3.5.3.14，均未入库，见 [[queries/4-5与3-5未入库对特征值节的依赖缺口]]）。