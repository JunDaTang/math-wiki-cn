---
type: finding
title: SPC 化简算例（式 5.314–5.315，已复算）
source: "[[10-数学手册原书第10版--12-57-布尔代数和开关代数--1ua6pjv]]"
confidence: high
replicated: true
tags: [开关代数, SPC, 化简, 算例]
related: [开关代数, spc布尔表达式化简流程, 布尔代数]
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/5.7 布尔代数和开关代数.md"]
---

# SPC 化简算例（式 5.314–5.315，已复算）

手册 5.7.7 的核心算例（图 5.23 的电路）：对 SPC 指派开关函数

$$S=(\bar a\sqcap b)\sqcup(a\sqcap b\sqcap\bar c)\sqcup(\bar a\sqcap(b\sqcup c)).\tag{5.314}$$

依据布尔代数的变换公式逐步化简：

```
S = (b⊓(ā⊔(a⊓c̄))) ⊔ (ā⊓(b⊔c))
  = (b⊓(ā⊔c̄)) ⊔ (ā⊓(b⊔c))
  = (ā⊓b) ⊔ (b⊓c̄) ⊔ (ā⊓c)
  = (ā⊓b⊓c) ⊔ (ā⊓b⊓c̄) ⊔ (b⊓c̄) ⊔ (a⊓b⊓c̄) ⊔ (ā⊓c) ⊔ (ā⊓b̄⊓c)
  = (ā⊓c) ⊔ (b⊓c̄)                    (5.315)
```

其中从 $(\bar a\sqcap b\sqcap c)\sqcup(\bar a\sqcap c)\sqcup(\bar a\sqcap\bar b\sqcap c)$ 合并得 $\bar a\sqcap c$，从 $(\bar a\sqcap b\sqcap\bar c)\sqcup(b\sqcap\bar c)\sqcup(a\sqcap b\sqcap\bar c)$ 合并得 $b\sqcap\bar c$。化简后的最终 SPC 显示在图 5.24 中。

## 复算结论（直接复算）

- 化简链每一步的等价性已核验（提公因子、分配律展开为基本合取的析取、吸收律合并）；
- 最终式 $S=(\bar a\sqcap c)\sqcup(b\sqcap\bar c)$ 与原式 (5.314) 在全部 8 个赋值点 $(a,b,c)\in B^3$ 上取值一致。

## 源的结语

这个例子表明通常通过变换得到最简布尔表达式并不那么容易；在文献中可以找到不同的化简方法（源未具名）。

## 附图（原图不可核验，仅存文件）

![图 5.23：待化简的 SPC](media/10-数学手册原书第10版--12-57-布尔代数和开关代数--1ua6pjv/004-eff2af511d40bcd7b9054728d0a2c758ed3d810e44bff0836b457e99f380af1c.jpg)

![图 5.24：化简后的 SPC](media/10-数学手册原书第10版--12-57-布尔代数和开关代数--1ua6pjv/005-0747007976320542e6aa6bae473bae74e660d658edca22a2c4b7e0268ca3e8e0.jpg)

> 转写注：式 (5.315) 的式号在转写中被误标为「(5)」；化简过程为源原文完整转写，已全链复算。