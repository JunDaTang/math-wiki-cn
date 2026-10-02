---
type: concept
title: "Mathematica 数的四种基本类型"
tags: [Mathematica, 计算机代数, 数的类型, 精确算术, 浮点数]
related: [mathematica, Head函数与类型查询, Mathematica谓词检验算子, Mathematica特殊常数, Mathematica中数的表示与转换]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# Mathematica 数的四种基本类型

Mathematica 用「头」（head）标识四种数的类型：Integer（精确整数，任意长）、Rational（形如 Integer/Integer 的互素分数）、Real（浮点数，任意给定精度）与 Complex（形如 number + number*I 的复数）。整数与有理数属精确表示，实数属可任意加长的浮点近似表示——「精确 vs 近似」是这套类型系统的主轴。来源：《数学手册（原书第10版）》20.2.2.1（[[sources/10-数学手册原书第10版--21-2022-mathematica中数的类型--gq11qw]]）。

## 类型总览（表 20.1 转录）

| 数的类型 | 头 | 特征 | 输入 |
|---|---|---|---|
| 整数 | Integer | 精确整数，任意长 | nnnnn |
| 有理数 | Rational | 形式为 Integer/Integer 的互素的分数 | pppp/qqqq |
| 实数 | Real | 浮点数，任意给定精度 | nnnn.mmmm |
| 复数 | Complex | 形式为 number + number*I 的复数 | （源稿此列为空，见 [[queries/表20-1脱表字与complex输入列空缺之辨]]） |

## 类型判定的两条规则

**尾部小数点规则**：整数若写作带尾部小数点的形式（如 51.、2.），即被 Mathematica 看成一个浮点数，即 Real 类型的数。源稿此句讹作「如果一个整数 nnn 写作 mm 的形式」（见 [[queries/整数写作nnn点之mm讹误之辨]]）；「尾部小数点」读法由同节算例直接佐证：`Head[51.] = Real`、`IntegerQ[2.] = False`。

**复数分量规则**：复数的实部和虚部可以属于任何数的类型，整个数的类型归属由「最宽」的分量决定：`5.731 + 0 I` 被看成 Real 类型，而 `5.731 + 0. I` 为 Complex 类型，因为 `0.` 被看成接近于 0 的一个浮点数（近似零被保留在结果中）。源稿对此为叙述性论断、未印出 Head 检验算例，复算状态见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]]。

## 类型查询入口

数的类型用命令 `Head[x]` 确定（[[concepts/Head函数与类型查询]]）：`Head[51]` → `Integer`、`Head[51.]` → `Real`。布尔化的类型检查由以 Q 结尾的谓词算子承担（[[concepts/Mathematica谓词检验算子]]）。

## 意义与关联

- 精确类型（Integer、Rational）承载无舍入误差的精确算术，是 [[concepts/公式操作]] 的数据基础；Real 的「任意给定精度」使数值计算可按需控制有效位数，对应 [[concepts/数值计算（计算机代数应用领域）]]。类型学比较见 [[comparisons/Mathematica精确数与浮点数类型学比较]]。
- Real 的任意精度与 19.8.2 节机器定长浮点（[[concepts/规范化浮点数表示]]）的层次辨析见 [[comparisons/机器浮点与任意精度浮点比较]]。
- 精确数与浮点数之间的双向转换（N、Rationalize）见 [[concepts/Mathematica中数的表示与转换]]。

## 边界

本页规则仅对 Mathematica 成立；Matlab、Maple 的数类型机制见 [[sources/10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm]]，不应跨系统外推。