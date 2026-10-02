---
type: query
title: "式 (4.63) 末项是否应为 AᵀBᵀ 而非 AᵀBᴴ？"
created: 2026-09-30
updated: 2026-09-30
tags: [线性代数, 行列式, 转写讹误, 存疑公式]
related: [行列式计算法则, 行列式计算法则八条, 4-2全节转写讹误清单]
sources: ["数学手册(原书第10版)/4.2 行列式.md"]
---

# 式 (4.63) 末项是否应为 AᵀBᵀ 而非 AᵀBᴴ？

## 问题

《数学手册(原书第10版)》式 (4.63)：

$$(\det\boldsymbol A)(\det\boldsymbol B)=\det(\boldsymbol{AB})=\det(\boldsymbol{AB}^{\mathrm T})=\det(\boldsymbol A^{\mathrm T}\boldsymbol B)=\det(\boldsymbol A^{\mathrm T}\boldsymbol B^{\mathrm H})$$

末项与链首的等式在一般情形下不成立：$\det(\boldsymbol A^{\mathrm T}\boldsymbol B^{\mathrm H})=\det\boldsymbol A\cdot(\det\boldsymbol B)^{*}$，仅当 $\det\boldsymbol B$ 为实数时才等于 $(\det\boldsymbol A)(\det\boldsymbol B)$。而同节 4.2.1 明言行列式可以是复数，故对一般复矩阵该等式为假。

## 两种假设

1. **转写讹误**：原书应为 $\det(\boldsymbol A^{\mathrm T}\boldsymbol B^{\mathrm T})$，上标 T 被误识为 H。辅助证据：(4.63) 后的说明文字枚举"行与列、行与行、列与行或列与列的标量积"，其中"列与行"对应的非共轭组合恰为 $\boldsymbol A^{\mathrm T}\boldsymbol B^{\mathrm T}$；若取 Bᴴ，该项实为"列与共轭行"，与"标量积"的平实措辞不甚吻合（此为辅助性、非决定性证据）。本源已确认存在系统性的上标/符号转写脱落（[[queries/4-2全节转写讹误清单]]）。
2. **原书如此**：则该式隐含实矩阵限定（此时 Bᴴ=Bᵀ，等式成立），但与 4.2.1"行列式可取复数"的表述存在内部张力。

## 当前倾向

假设 1 解释力更强：既消除数学矛盾，又与说明文字的四组合枚举相容。

## 待办

- 查对原书第 10 版纸本或可靠电子版的式 (4.63)。
- 若确认为 Bᴴ，需在 [[findings/行列式计算法则八条]] 与 [[concepts/行列式计算法则]] 补记"实矩阵限定"条件。