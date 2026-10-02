---
type: query
title: 公式 53 arctan 宗量倒置之辨
created: 2026-10-02
updated: 2026-10-02
tags: [待刊本核对, 转写讹误, 拉普拉斯变换, 反三角族]
related: [公式53arctan宗量倒置与β脱方复算, 21-13拉普拉斯变换全表复算, 21-13全节系统性转写讹误清单, 拉普拉斯变换表]
sources: ["数学手册(原书第10版)/21.13 拉普拉斯变换.md"]
---

# 公式 53 arctan 宗量倒置之辨

**待辨问题**：21.13 节式 53 的 $F(p)=\arctan\frac{p^{2}-\alpha p+\beta}{\alpha\beta}$ 是否应为 $\arctan\frac{\alpha\beta}{p^{2}-\alpha p+\beta^{2}}$（宗量倒置且 $\beta$ 补平方）？此误是数字化转写还是原书排印？

**证据**（见 [[findings/公式53arctan宗量倒置与β脱方复算]]）：

- 除法规则复算：$\mathcal{L}\{\frac{e^{\alpha t}-1}{t}\sin\beta t\}=\arctan\frac{\alpha\beta}{p^{2}-\alpha p+\beta^{2}}$。
- 大 p 渐近：原表宗量 $\to\infty$，$F(p)\to\frac{\pi}{2}\neq0$，违反连续因果函数变换的衰减性；倒置后宗量 $\to0$，正常。

**判定所需**：原书第 10 版刊本 21.13 节式 53 页面。注意本错误为「倒置 + 脱方」复合，若刊本仅见其一，则另一处属转写层讹误。

**关联**：[[queries/21-13全节系统性转写讹误清单]]。