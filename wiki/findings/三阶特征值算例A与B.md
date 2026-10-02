---
type: finding
title: 三阶特征值算例 A 与 B（已复算）
tags: [线性代数, 特征值, 算例]
related: [特征值与特征向量, 特征值与特征向量计数三情形, 特征多项式与特征方程]
source: "[[10-数学手册原书第10版--10-46-矩阵特征值问题--f9s58z]]"
confidence: high
replicated: true
created: 2026-09-30
updated: 2026-09-30
sources: ["数学手册(原书第10版)/4.6 矩阵特征值问题.md"]
---

# 三阶特征值算例 A 与 B（已复算）

**发现**：4.6.2.1 给出两个三阶特征值算例；本次导入已独立复算，全部吻合。

**算例 A**：

$$A=\begin{pmatrix}2&-3&1\\3&1&3\\-5&2&-4\end{pmatrix},\qquad \det(A-\lambda I)=-\lambda^3-\lambda^2+2\lambda=0,$$

特征值 $\lambda_1=0,\ \lambda_2=1,\ \lambda_3=-2$（互异，故三个线性无关特征向量）：

$$\underline{x}_1=C_1\begin{pmatrix}10\\3\\-11\end{pmatrix},\quad \underline{x}_2=C_2\begin{pmatrix}-1\\0\\1\end{pmatrix},\quad \underline{x}_3=C_3\begin{pmatrix}4\\3\\-7\end{pmatrix}\quad(C_i\neq0).$$

源文并给出求解各齐次方程组的选主元过程（如 $\lambda_1=0$ 时：$x_1$ 任意，$x_2=\tfrac{3}{10}x_1$，$x_3=-2x_1+3x_2=-\tfrac{11}{10}x_1$，取 $x_1=10$）。

**算例 B**：

$$B=\begin{pmatrix}3&0&-1\\1&4&1\\-1&0&3\end{pmatrix},\qquad \det(B-\lambda I)=-\lambda^3+10\lambda^2-32\lambda+32=-(\lambda-4)^2(\lambda-2)=0,$$

特征值 $\lambda_1=2,\ \lambda_2=\lambda_3=4$。$\lambda_1=2$ 对应 $\underline{x}_1=C_1(1,-1,1)^{\mathrm{T}}$；二重特征值 4 仍有两个线性无关特征向量

$$\underline{x}_2=C_2\begin{pmatrix}0\\1\\0\end{pmatrix},\quad \underline{x}_3=C_3\begin{pmatrix}-1\\0\\1\end{pmatrix}$$

（分别取 $x_2=1,x_3=0$ 与 $x_2=0,x_3=1$）——**无亏损、可对角化**的示例。

**复算核验**：两例的特征多项式、特征值与全部特征向量均经代入 $A\underline{x}=\lambda\underline{x}$ 独立复核通过。

**转写讹误**：算例 B 中「$x_3,x_3$ 任意」应为「$x_2,x_3$ 任意」（$\lambda=4$ 时 $x_1=-x_3$，自由变量为 $x_2,x_3$），见 [[queries/例B的x3x3任意是否应为x2x3任意]]。