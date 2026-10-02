---
type: source
title: "数学手册（原书第10版）20.2.2 Mathematica 中数的类型"
tags: [计算机代数, Mathematica, 数的类型, 谓词, 数制转换, 数学手册]
related: [mathematica, Mathematica输入输出行记法, Mathematica数的四种基本类型, Head函数与类型查询, Mathematica谓词检验算子, Mathematica特殊常数, Mathematica中数的表示与转换, 式20-5至20-7类型谓词与数制转换算例转录复算, 10-数学手册原书第10版--6-201-引言--4divnh]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
authors: []
year: ""
venue: "数学手册（原书第10版）"
url: ""
---
# 数学手册（原书第10版）20.2.2 Mathematica 中数的类型

## 源文档定位

本页是《数学手册（原书第10版）》第 20 章（计算机代数）20.2 节「Mathematica」子节 20.2.2 的入库源页，全节分三小节：20.2.2.1 数的基本类型、20.2.2.2 特殊的数、20.2.2.3 数的表示与转换。上游源为 20.1 引言（[[sources/10-数学手册原书第10版--6-201-引言--4divnh]]）；本节与 19.8.4 交互程序系统和计算机代数系统的应用（[[sources/10-数学手册原书第10版--22-1984-交互程序系统和计算机代数系统的应用--k25qkm]]）中的 Mathematica 部分互为呼应。In[n]/Out[n] 记法沿用 [[concepts/Mathematica输入输出行记法]] 所载惯例。本节全部论断仅关于 [[entities/mathematica]]，不应外推至 Matlab 或 Maple。

## 20.2.2.1 数的基本类型

Mathematica 认识四种数的类型，各以「头」（head）标识。表 20.1 转录如下（表标题在转写稿中作「20.1」，疑脱「表」字；Complex 行「输入」列为空，两处均见 [[queries/表20-1脱表字与complex输入列空缺之辨]]）：

| 数的类型 | 头 | 特征 | 输入 |
|---|---|---|---|
| 整数 | Integer | 精确整数，任意长 | nnnnn |
| 有理数 | Rational | 形式为 Integer/Integer 的互素的分数 | pppp/qqqq |
| 实数 | Real | 浮点数，任意给定精度 | nnnn.mmmm |
| 复数 | Complex | 形式为 number + number*I 的复数 | （源稿此列为空） |

要点：

- 实数即浮点数，可以任意地长。整数若写作带尾部小数点的形式（源稿讹作「写作 mm 的形式」，据算例应为「写作 nnn. 的形式」，见 [[queries/整数写作nnn点之mm讹误之辨]]），则被 Mathematica 看成一个浮点数，即 Real 类型的数。
- 数的类型用命令 Head[x] 确定：`Head[51]` 得 `Integer`，`Head[51.]` 得 `Real`。详见 [[concepts/Head函数与类型查询]] 与 [[concepts/Mathematica数的四种基本类型]]。
- 复数的实部和虚部可以属于任何数的类型：`5.731 + 0 I` 被看成 Real 类型，而 `5.731 + 0. I` 为 Complex 类型，因为 `0.` 被看成接近于 0 的一个浮点数（源稿「接近千」为「接近于」之讹，且其后疑脱「0」，见 [[queries/20-2-2节行内数学变量脱失之辨]]）。
- 存在一些进一步的运算，它们给出有关数的信息：以 Q 结尾的谓词（判据）检验算子 NumberQ、IntegerQ、EvenQ、OddQ、PrimeQ，总在逻辑检验（包括类型检查）的意义上回答布尔常数 True 或 False；`NumberQ[π]` 输出 False 而 `NumericQ[π]` 得 True（源稿此处断裂讹作「Num.ericQ ［兀］」，见 [[queries/NumericQ断裂与兀为pi之讹]]）。详见 [[concepts/Mathematica谓词检验算子]]。

## 20.2.2.2 特殊的数

Mathematica 中常需一些能以任意精度调入的特殊数：以符号 Pi 表示的 π、以符号 E 表示的 e（源稿此处 E 脱失）、以常数 Degree 表示的从角度到弧度的变换因子 π/180°、表示符号 ∞ 的 Infinity（源稿文句粘连作「表示符号 ∞ Infinity」），以及虚单位 I。详见 [[concepts/Mathematica特殊常数]]。

## 20.2.2.3 数的表示与转换

数可以用不同形式表示，并相互转换（详见 [[concepts/Mathematica中数的表示与转换]]）：

1. `N[x, n]`：每个实数 x 可表示成具有 n 位精确度的浮点数；
2. `Rationalize[x, dx]`：具有精度 dx 的数 x 可转换成有理数（两个整数作成的分数），Mathematica 用一个具有该准确度的有理数给出 x 可能的最佳逼近；
3. `BaseForm[x, b]`：以十进制给出的数 x 被转换成相应的具有数基 b ≤ 36 的数制中的数；若 b > 10，则依次用字母 a, b, c, … 表示大于十的数位；
4. `b^^nnmmm`（源稿讹作「b^^ Ammmm」）：执行反向变换，即其他进制转十进制；
5. 数可以用任意精度表示（这里默认的是硬件精度）；对于大数则使用所谓科学形式，即形如 `n.mmmm*10^±qq` 的形式。

## 算例转录（式 20.5–20.7 及前置算例）

以下按源稿顺序转录全部 In/Out 算例（OCR 空格噪声已归一化，如「$I n [ 3 ]$」→「In[3]」；讹字按原文保留并另行登记；编号沿用原书）：

```text
In[1] := Head[51]                 Out[1] = Integer
In[2] := Head[51.]                Out[2] = Real
In[3] := NumberQ[51]              Out[3] = True                    (20.5a)
        （x = π 时 NumberQ[π] 输出 False；NumericQ[π] 得 True）
In[4] := IntegerQ[2.]             Out[4] = False
In[5] := PrimeQ[1075643]          Out[5] = True                    (20.5b)
In[6] := PrimeQ[1075641]          Out[6] = False                   (20.5c)
In[1] := N[E, 20]                 Out[1] = 2.7182818284590452354   (20.6a)
In[2] := Rationalize[E, 10^-5]    Out[2] = 1071/394                (20.6b)
A:
In[1] := BaseForm[255, 16]        Out[1] = ff₁₆                    (20.7a)
In[2] := BaseForm[N[E, 10], 8]    Out[2] = 2.557605213₈             (20.7b)
■ B:
In[1] := 8^^735                   Out[1] = 477                     (20.7c)
```

其中「A:」「■ B:」为原书算例分组的排版残迹，非知识内容。全部算例的逐条复算见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]]：除 PrimeQ[1075643] 的完整素性验证待机验外，其余全部复算一致。

## 转写讹误与可信度

本转写稿存在与 20.1、19.8.x 各节同类的系统性讹误（「千」代「于」、行内数学变量脱失、符号断裂、表格脱字）。全部讹误的逐条登记见 [[queries/20-2-2全节系统性转写讹误清单]]。要点：讹误均属排版/OCR 层面，数值结论经复算全部一致，源内容可作为可信知识采信；采信前宜按清单对照原书复核。

## 与既有 wiki 的关联

- [[entities/mathematica]]：本节为其类型系统与数处理命令提供新的实质性内容（待增补）。
- [[concepts/Mathematica输入输出行记法]]：本节 In[n]/Out[n] 算例为该页所载惯例的新实例（待增补）。
- [[concepts/公式操作]] / [[concepts/数值计算（计算机代数应用领域）]]：本节「精确表示 vs 浮点表示」是符号/数值二分在类型系统层面的具体化，类型学比较见 [[comparisons/Mathematica精确数与浮点数类型学比较]]。
- [[concepts/规范化浮点数表示]]、[[concepts/舍入与舍入误差]]：19.8.2 节机器定长浮点与本节任意精度 Real 的层次辨析见 [[comparisons/机器浮点与任意精度浮点比较]]；符号解的浮点代入风险另见 [[queries/符号解浮点代入的相消风险]]。
- [[concepts/evalf与evalhf]]：Maple 的 evalf 与本节 N[x, n] 构成跨系统对应，比较页候选见 [[queries/20-2-2未入库回指缺口]]。