---
type: comparison
title: Apply 与 Map 比较
created: 2026-10-02
updated: 2026-10-02
tags: [mathematica, Apply, Map, 头替换, 逐元映射, 比较]
related: [Apply与Map, Part（部件提取与头）, FullForm（完整形式）]
sources: ["数学手册(原书第10版)/20.2.8 函数运算.md"]
---
# Apply 与 Map 比较

依据《数学手册(原书第10版)》20.2.8 (7)(8) 的定义式与算例（均经复算，见 [[findings/式20-22至20-23与Apply-Map算例转录复算]]），Apply 与 Map 的分野如下：

| 维度 | Apply | Map |
|---|---|---|
| 定义式 | `Apply[f, {a,b,c,…}] → f[a,b,c,…]`（式 20.22） | `Map[f, {a,b,c,…}] → {f[a], f[b], f[c],…}`（式 20.23） |
| 作用机制 | 用 f **替换**目标表达式的头 | **保持**头，将 f 逐个施于每个元素 |
| f 的调用方式 | 一次调用，收全部元素为变元 | 每个元素各调用一次 f |
| 结构变化 | 头改变、元素集不变 | 头不变、元素被逐个替换 |
| 源文算例 | `Apply[Plus, {u,v,w}] → u+v+w`；`Apply[List, a+b+c] → {a,b,c}` | `Map[f, {u,v,w}] → {u²,v²,w²}`；`Map[f, Plus[a,b,c]] → a²+b²+c²` |
| 作用范围 | 两例分别以列表与和式为对象 | 源文明言「可应用于更一般的表达式」 |

## 互为镜像的一对算例

- `Apply[List, a+b+c] = {a,b,c}`：把 `Plus[a,b,c]` 的头换成 List——**和式变列表**；
- `Map[f, Plus[a,b,c]] = a²+b²+c²`：保持 Plus 的头，把 f 施于各变元——**和式仍是和式**。

两者恰好展示了表达式的两个自由度（头、元素）；配合 [[concepts/FullForm（完整形式）]]（`FullForm[Apply[List, Plus[a,b,c]]] = List[a,b,c]`）可把机制看得分明。

## 典型易混点

对同一列表 `{a, b, c}` 与同一 f：

```
Apply[f, {a, b, c}] = f[a, b, c]         （f 一次收三个变元）
Map[f,   {a, b, c}] = {f[a], f[b], f[c]}  （f 每次收一个变元）
```

前者要求 f 能接受 n 个变元，后者只要求 f 是一元函数。源文中 `Apply[Plus, {u,v,w}]` 之所以得 `u+v+w`，正因 Plus 恰是接受任意多个变元的求和函数。

## 证据边界

以上对照仅基于 20.2.8 所载定义式与五条算例；两命令的其余用法（如指定作用层级的变体）源文未涉，不在本比较的断言范围内。