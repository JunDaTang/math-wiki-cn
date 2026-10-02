---
type: concept
title: "Mathematica 中数的表示与转换"
tags: [Mathematica, N, Rationalize, BaseForm, 数制转换, 任意精度]
related: [mathematica, Mathematica数的四种基本类型, Mathematica特殊常数, 规范化浮点数表示, evalf与evalhf]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.2 Mathematica中数的类型.md"]
---
# Mathematica 中数的表示与转换

本页汇总《数学手册（原书第10版）》20.2.2.3（[[sources/10-数学手册原书第10版--21-2022-mathematica中数的类型--gq11qw]]）所载 Mathematica 中数的表示形式与相互转换机制：任意精度浮点化（N）、有理化（Rationalize）、数制转换（BaseForm 与 b^^ 记法）以及大数的科学形式。

## N[x, n]：任意精度浮点化

每个实数 x 可以表示成一个具有 n 位精确度的浮点数 `N[x, n]`：

```text
In[1] := N[E, 20]   →   Out[1] = 2.7182818284590452354    (20.6a)
```

Maple 中与之对应的是 evalf（[[concepts/evalf与evalhf]]）；是否另立跨系统比较页，待 20.2 节其余小节入库后再定（见 [[queries/20-2-2未入库回指缺口]]）。

## Rationalize[x, dx]：有理化

使用 `Rationalize[x, dx]`，具有精度 dx 的数 x 可以转换成一个有理数，即转换成两个整数作成的分数；Mathematica 用一个具有该准确度的有理数给出 x 可能的最佳逼近：

```text
In[2] := Rationalize[E, 10^-5]   →   Out[2] = 1071/394    (20.6b)
```

复算表明 1071/394 恰为分母最小且 |E − p/q| ≤ 10⁻⁵ 的有理逼近（误差 ≈ 7.72×10⁻⁶），与「最佳逼近」的叙述一致，见 [[findings/式20-5至20-7类型谓词与数制转换算例转录复算]]。

## BaseForm[x, b] 与 b^^ 记法：数制转换

`BaseForm[x, b]` 把以十进制给出的数 x 转换成相应的具有数基 b ≤ 36 的数制中的数；若 b > 10，则字母表中依次出现的字母 a, b, c, … 被进一步用于表示大于十的数位。反向的变换（b 进制转十进制）用 `b^^nnmmm` 记法执行（源稿讹作「b^^ Ammmm」，见 [[queries/20-2-2节行内数学变量脱失之辨]]）：

```text
In[1] := BaseForm[255, 16]       →   Out[1] = ff₁₆            (20.7a)
In[2] := BaseForm[N[E, 10], 8]   →   Out[2] = 2.557605213₈     (20.7b)
In[1] := 8^^735                  →   Out[1] = 477              (20.7c)
```

（源稿在 (20.7a)–(20.7b) 前标「A:」、(20.7c) 前标「■ B:」，为原书算例分组的排版残迹，非知识内容。）

## 科学形式与默认精度

数可以用任意精度来表示，这里默认的是硬件精度；对于大数则使用所谓的科学形式，即形如 `n.mmmm*10^±qq` 的形式。「默认硬件精度」一句是 Mathematica 任意精度软件浮点与 19.8.2 节机器定长浮点（[[concepts/规范化浮点数表示]]）的衔接点，辨析见 [[comparisons/机器浮点与任意精度浮点比较]]。

## 类型学位置

N 与 Rationalize 是精确表示（Integer/Rational，[[concepts/Mathematica数的四种基本类型]]）与浮点表示（Real）之间的双向桥梁；对特殊常数（[[concepts/Mathematica特殊常数]]）而言，N 是符号进入数值的唯一通路。