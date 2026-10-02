---
type: entity
title: 普勒梅利-Sochozki公式
created: 2026-10-01
updated: 2026-10-01
tags: [数学手册, 复分析, 柯西型积分, 边值公式, 命名公式]
related: [柯西型积分, 柯西核奇异积分方程, 希尔伯特边值问题, 希尔伯特边值问题求解流程]
sources: ["数学手册(原书第10版)/11.5 奇异积分方程.md"]
---

# 普勒梅利-Sochozki公式

普勒梅利-Sochozki 公式是刻画柯西型积分边界值跃变的命名公式：设 $\varPhi(z)=\frac{1}{2\pi i}\int_\Gamma\frac{\varphi(y)}{y-z}\,\mathrm dy$ 为闭曲线组 $\Gamma$ 上以 $\varphi$ 为密度的柯西型积分，$\mathcal H\varphi$ 为对应的柯西主值奇异积分算子，则 $\varPhi$ 从内部区域 $S^+$、外部区域 $S^-$ 趋于边界点 $x\in\Gamma$ 时的边值满足

$$\varPhi^+(x)=\frac12\varphi(x)+(\mathcal H\varphi)(x),\qquad \varPhi^-(x)=-\frac12\varphi(x)+(\mathcal H\varphi)(x).\tag{11.76c}$$

即密度 $\varphi$ 恰好是两侧边值之差（跃变），而主值积分是两侧边值的平均。手册 11.5.2.3 以「普勒梅利 (Plemelj)–Sochozki 公式」之名给出该结果。

## 名称与译写

原书将冠名人 Plemelj 译作「普勒梅利」，Sochozki 保留拉丁转写；本 wiki 沿用原书拼写「普勒梅利-Sochozki公式」，别名「索霍茨基公式」。（可独立查证的背景，非本节内容：该公式在文献中通称 Sokhotski–Plemelj 公式或索霍茨基–普勒梅利公式。）

## 在本来源中的作用

- **11.5.2.3**：作为柯西型积分性质的核心结论给出，与「沿曲线行进时 $S^+$ 总在 $\Gamma$ 左边」的定向约定一致（复算确认符号无误）。
- **11.5.2.4**：借助它把柯西核特征方程 (11.74b) 化归为 [[concepts/希尔伯特边值问题]]——由 (11.76c) 相加减得 $\varphi=\varPhi^+-\varPhi^-$、$2\mathcal H\varphi=\varPhi^++\varPhi^-$ (11.77a)。
- **11.5.2.6**：再次用它计算 $R(z)$ 的边值 $R^\pm$ (11.85c)，最终导出特征方程的显式解 (11.86)。

## 复算核验

公式本身为标准结果，与 $\Gamma$ 定向（$S^+$ 在左）约定一致；将 (11.85c) 的 $R^\pm$ 代入 $\varphi=X^+R^+-X^-R^-$ 逐项化简，与 (11.86) 完全一致。详见 [[findings/式11-75a至11-76c存在性条件与柯西型积分转录复算]]、[[findings/式11-84a至11-87特征积分方程解与常系数算例复算]]。

## 依据

来源：[[sources/10-数学手册原书第10版--10-115-奇异积分方程--l25w62]]（11.5.2.3、11.5.2.4、11.5.2.6）。