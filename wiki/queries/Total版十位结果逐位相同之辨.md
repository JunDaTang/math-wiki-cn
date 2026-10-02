---
type: query
title: Total[Sqrt[N[Range[n],10]]] 与 N 版结果逐位相同之辨
tags: [mathematica, total, range, 有效数字, 舍入累积, 数值验证]
related: [concepts/Mathematica函数式程序设计, findings/例B-函数式sumq与Total复算, comparisons/过程式与函数式sumq实现比较, queries/20-2-9全节系统性转写讹误清单, sources/10-数学手册原书第10版--9-2029-程序设计--l13hq7]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.9 程序设计.md"]
---
# Total[Sqrt[N[Range[n],10]]] 与 N 版结果逐位相同之辨

**问题**：例 B 称 `Total[Sqrt[N[Range[n], 10]]]` 与 `N[Apply[Plus, Table[Sqrt[i], {i, 1, n}]], 10]`「给出相同的结果」（n = 30 时后者为 112.0828452，复算通过，见 [[findings/例B-函数式sumq与Total复算]]）。

**疑点**：两式的数值路径不同——

- `N[Apply[Plus, Table[...]], 10]`：先在精确数域求和（`Sqrt[i]` 为精确根式），再一次性取 10 位有效数字；
- `Total[Sqrt[N[Range[n], 10]]]`：先将各整数数值化为 10 位精度，逐项开方（每项各自舍入至 10 位），再求和——30 项的逐项舍入累积可能波及末位。

**拟断**：近似可信（逐项误差约 10⁻¹⁰ 量级，30 项累积约 10⁻⁹，恰在第 10 位有效数字附近），但原文「相同」之说偏强，需在 Mathematica 中实测 `Total[Sqrt[N[Range[30], 10]]]` 的逐位输出方能定谳。

**查证方向**：实测该式输出；查证 Wolfram Language 有效数位算术（significance arithmetic）中加法与开方的误差传播规则；若末位有出入，应在 [[concepts/Mathematica函数式程序设计]] 及例 B 相关页面标注原文表述偏强。