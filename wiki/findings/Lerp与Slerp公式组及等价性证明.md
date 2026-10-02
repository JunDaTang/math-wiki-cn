---
type: finding
title: Lerp 与 Slerp 公式组及等价性证明（式 4.143–4.149）
created: 2026-09-30
updated: 2026-09-30
tags: [四元数, 插值, Slerp, Lerp]
related: [Lerp, Slerp, 四元数, 测地线]
sources: ["数学手册(原书第10版)/4.4.3 四元数的应用.md"]
source: "[[10-数学手册原书第10版--10-443-四元数的应用--1robxiu]]"
confidence: high
replicated: true
---

# Lerp 与 Slerp 公式组及等价性证明（式 4.143–4.149）

**发现**：《数学手册（原书第10版）》4.4.3.1 给出的 Lerp（式 4.143）、Slerp 三重等价表达式（式 4.144）及其特殊情形（4.145、4.146）与等价性推导（4.147–4.149）经独立复核全部成立；其中式 (4.144)/(4.149) 的末项 p^{1−t}q^t 是非交换代数中的记号缩并，严格形式为 p(p̄q)^t。

## 公式组（照录）

```latex
Lerp(p, q, t) = p(1 - t) + q t                                             (4.143)

Slerp(p, q, t) = p(\bar{p} q)^t = p^{1-t} q^t
               = p · sin((1-t)φ)/sinφ + q · sin(tφ)/sinφ,   0 < φ < π       (4.144)

Slerp(1, q, t) = cos(tφ) + n̲_q sin(tφ)    (p = 1, q = cosφ + n̲_q sinφ)    (4.145)

q_k := Slerp(p, q, k/n) = (1/sinφ)(sin(φ - kψ) p + sin(kψ) q),
       ψ = φ/n,   k = 0, 1, …, n                                           (4.146)

Q₀ = Sc Q = Sc(p̄q) = ⟨p, q⟩ = cos φ                                       (4.147)

Q(t) = sin((1-t)φ)/sinφ + Q · sin(tφ)/sinφ
     = cos(tφ) + n⃗_Q sin(tφ) = e^{t n⃗_Q φ} = e^{t log Q} = Q^t            (4.148)

q(t) = p Q(t) = p · sin((1-t)φ)/sinφ + q · sin(tφ)/sinφ
     = p Q^t = p(p⁻¹q)^t = p^{1-t} q^t                                     (4.149)
```

## 复核结论

- (4.145)、(4.146)：由 (4.144) 直接代入成立；(4.146) 说明 ψ = φ/n 时 q_k 把大圆弧 n 等分（等距网格）。
- (4.148)：化简链 sin((1−t)φ) + cosφ·sin(tφ) = sinφ·cos(tφ) 正确；指数形式 e^{t n⃗_Q φ} = e^{t log Q} = Q^t 成立（n⃗_Q 为 Q 的单位向量部分）。
- (4.149)：与 (4.144) 一致（Slerp 的三角函数形式与 p(p̄q)^t 相同）。

## 警示：非交换记号 p^{1−t}q^t（分析者构造并复核的反例）

p^{1−t}q^t 与 p(p̄q)^t 仅当 p、q 交换时相等。取 p = i, q = j, t = ½：

- p(p̄q)^t：p̄q = (−i)j = −k，(−k)^{1/2} = (1−k)/√2，故 p(p̄q)^{1/2} = i(1−k)/√2 = (i+j)/√2（用 ik = −j）；这与三角函数形式 Slerp(i, j, ½) = i·sin(π/4) + j·sin(π/4) = (i+j)/√2 一致。
- p^{1−t}q^t = i^{1/2}j^{1/2} = (1+i)(1+j)/2 = (1+i+j+k)/2。

两者是不同的单位四元数，故等号一般不成立。推导本身正确，末项是记号缩并；是否原书如此见 [[queries/式4-144末项非交换记号是否原书如此]]。

## 主张归属

「插值点非等距（角速度不均匀）」属于 Lerp＋归一化；「最短连接条件 ⟨p,q⟩ > 0」属于 Slerp。两者不可互换（见 [[concepts/Lerp]]、[[concepts/Slerp]]、[[comparisons/Lerp与Slerp比较]]）。