---
type: comparison
title: J 族与 I 族拉普拉斯变换对平行比较
created: 2026-10-02
updated: 2026-10-02
tags: [拉普拉斯变换, 贝塞尔函数, 平行结构, 变换表]
related: [贝塞尔函数（柱面函数）, 拉普拉斯变换表, 拉普拉斯变换, 21-13拉普拉斯变换全表复算, 公式49根号内α2减β2疑为β2减α2复算]
sources: ["数学手册(原书第10版)/21.13 拉普拉斯变换.md"]
---

# J 族与 I 族拉普拉斯变换对平行比较

《数学手册（原书第10版）》21.13 节的贝塞尔族条目呈五组镜像：把 $p^{2}+\alpha^{2}$（$J$ 族）换为 $p^{2}-\alpha^{2}$（$I$ 族），原函数中的 $J$ 相应换为 $I$，其余结构不变。这一平行结构既是复算工具（一组核对后另一组按同构迁移），也是定位式 49 疑点的参照系。

| 组 | $J$ 族（$p^2+\alpha^2$） | $I$ 族（$p^2-\alpha^2$） | 结构 |
|---|---|---|---|
| 46/47 | $\frac{1}{\sqrt{p^{2}+\alpha^{2}}}\leftrightarrow J_{0}(\alpha t)$ | $\frac{1}{\sqrt{p^{2}-\alpha^{2}}}\leftrightarrow I_{0}(\alpha t)$ | 基本对 |
| 63/64 | $\frac{(\sqrt{p^{2}+\alpha^{2}}-p)^{\nu}}{\sqrt{p^{2}+\alpha^{2}}}\leftrightarrow\alpha^{\nu}J_{\nu}(\alpha t)$ | $\frac{(p-\sqrt{p^{2}-\alpha^{2}})^{\nu}}{\sqrt{p^{2}-\alpha^{2}}}\leftrightarrow\alpha^{\nu}I_{\nu}(\alpha t)$ | 任意阶（$Re\nu>-1$） |
| 66/67 | $\frac{e^{-\beta\sqrt{p^{2}+\alpha^{2}}}}{\sqrt{p^{2}+\alpha^{2}}}\leftrightarrow$ 分段 $J_{0}(\alpha\sqrt{t^{2}-\beta^{2}})$ | 同型 $\leftrightarrow$ 分段 $I_{0}(\alpha\sqrt{t^{2}-\beta^{2}})$ | 延迟 |
| 69/70 | $\frac{e^{-\beta\sqrt{p^{2}+\alpha^{2}}}}{p^{2}+\alpha^{2}}\left(\beta+\frac{1}{\sqrt{p^{2}+\alpha^{2}}}\right)\leftrightarrow\frac{\sqrt{t^{2}-\beta^{2}}}{\alpha}J_{1}(\alpha\sqrt{t^{2}-\beta^{2}})$ | 同型 $\leftrightarrow\frac{\sqrt{t^{2}-\beta^{2}}}{\alpha}I_{1}(\cdot)$ | 延迟一阶 |
| 71/72 | $e^{-\beta p}-e^{-\beta\sqrt{p^{2}+\alpha^{2}}}\leftrightarrow\frac{\beta\alpha}{\sqrt{t^{2}-\beta^{2}}}J_{1}(\alpha\sqrt{t^{2}-\beta^{2}})$ | $e^{-\beta\sqrt{p^{2}-\alpha^{2}}}-e^{-\beta p}\leftrightarrow\frac{\beta\alpha}{\sqrt{t^{2}-\beta^{2}}}I_{1}(\cdot)$ | 差型 |

## 观察要点

- **符号规律**：像函数中取 $+\alpha^{2}$ 对应 $J$，取 $-\alpha^{2}$ 对应 $I$。式 49 恰好违反此规律——分母配方后为 $(p+\alpha)^{2}+(\beta^{2}-\alpha^{2})$ 即「$+$」型，宗量却按「$-$」型写 $\sqrt{\alpha^{2}-\beta^{2}}$——这是判定其疑点的结构依据（[[findings/公式49根号内α2减β2疑为β2减α2复算]]）。
- **分子差序呼应**：式 63 分子为 $\sqrt{p^{2}+\alpha^{2}}-p$（「$+$」型时根式大于 $p$，差为正），式 64 分子为 $p-\sqrt{p^{2}-\alpha^{2}}$（「$-$」型时根式小于 $p$，差为正）——两组都保持「大减小」以维持正性，这正是式 41 差序倒置暴露的机制（[[findings/公式41根号内差序倒置复算]]）。
- **混合型**：式 48、68 的 $(p+\alpha)(p+\beta)$ 配方后归于 $I_{0}$（「$-$」型），不属 $J$/$I$ 严格镜像，但同受上述符号规律支配。
- **参见注的不对称**：式 47 注 $I_0$ 参见第 744 页 (3)，而式 64 注 $I_\nu$ 参见第 743 页 (2)，疑有一误（[[queries/公式64参见2疑为3之辨]]）。

## 复算状态

五组镜像对（46/47、63/64、66/67、69/70、71/72）与混合型式 48、68 复算全部通过，属 [[findings/21-13拉普拉斯变换全表复算]] 中 71 条相符的一部分；唯配方型式 49 复算不符。本比较亦为 [[concepts/贝塞尔函数（柱面函数）]] 提供拉普拉斯表示族的正面佐证——注意 21.11 的 $Y_0$ 数值表讹误（[[findings/Y0于x0-2值1-0181与复算不符]]）属数值表问题，性质不同，不可移用于此。