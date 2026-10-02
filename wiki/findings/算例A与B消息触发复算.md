---
type: finding
title: 算例A与B消息触发复算
tags: [Mathematica, 复算, "Power::infy", "Log::argt", ComplexInfinity, 消息]
related: [消息系统（Mathematica）, 延迟赋值（SetDelayed与RuleDelayed）, 模式（Mathematica）, 警告消息与错误消息后果比较, mathematica]
created: 2026-10-02
updated: 2026-10-02
sources: ["数学手册(原书第10版)/20.2.10 关于句法、信息、消息的补充.md"]
source: "[[sources/10-数学手册原书第10版--17-20210-关于句法信息消息的补充--1xj9llw]]"
confidence: medium
replicated: true
---
# 算例A与B消息触发复算

本条目复算《数学手册》20.2.10 节为说明 [[concepts/消息系统（Mathematica）]] 而给出的两个算例。直接证据为该节逐字转录的输入与输出；「与现行版本一致」的判断属依据 Mathematica 通行语义的推断（独立可查证背景），尚非附有运行日志的实测。

## 例 A：警告型消息，计算仍可执行

```txt
In[1] := f[x_] := 1/x;
In[2] := f[0]

Power::infy: Infinite expression 1/0 encountered.

Out[2] = ComplexInfinity
```

复算要点：

- f[x_] := 1/x 经 [[concepts/延迟赋值（SetDelayed与RuleDelayed）]] 与 [[concepts/模式（Mathematica）]]（模式 x_）定义；
- 求值 f[0] 时，1/0 触发 Power::infy 消息；这是警告而非错误，计算本身可以执行，返回 ComplexInfinity；
- Power::infy 为 Mathematica 真实消息标记，1/0 → ComplexInfinity 与现行版本行为一致。

注意：本节说明句「当给一个表达式赋值时得到的值是 ∞」措辞不确——实际情形是求值 f[0] 得 ComplexInfinity，并非「赋值」；转写中「CX)」疑为「∞」之讹形。详见 [[queries/20-2-10全节系统性转写讹误清单]]。

## 例 B：错误型消息，计算无法执行

```txt
In[1] := Log[3, 16, 25]

Log::argt: Log called with 3 arguments; 1 or 2 arguments are expected.

Out[1] = Log[3, 16, 25]
```

复算要点：

- Log 按定义只接受 1 或 2 个自变量；3 个自变量的调用触发 Log::argt（转写句「包含 个自变量」脱数字「3」）；
- 该错误使计算无法执行，Mathematica 对该表达式不能做任何事情，原样返回 Log[3, 16, 25]；
- Log::argt 为 Mathematica 真实消息标记，行为与现行版本一致。

## 结论

两例构成刻意对照：同以 symbol::tag 形式呈现的消息，警告型（例 A）不阻断求值而错误型（例 B）阻断求值，见 [[comparisons/警告消息与错误消息后果比较]]。复算判定：与现行版本一致（replicated: true；confidence: medium——依据书面复算与通行语义核对，尚缺独立运行记录）。