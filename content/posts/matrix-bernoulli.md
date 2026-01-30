+++ 
date = 2026-01-30T11:33:40+08:00
title = "矩阵形式的伯努利不等式"
description = ""
slug = ""
authors = []
tags = []
categories = ["线性代数"]
externalLink = ""
series = []
+++

前情提要：见[原帖](https://zhuanlan.zhihu.com/p/1998822127588107924)。其文末附了一个矩阵形式的伯努利不等式，于是在此尝试给出证明。

---

{{<theorem 1>}}设$A_1,\ldots, A_n$为一列实对称半正定矩阵，证明\[\det(I+\sum_{i=1}^nA_i)\le\prod_{i=1}^n\det(I+A_i)\]{{</theorem>}}

由数学归纳法只需证明$n=2$的情形， 亦即对实对称半正定矩阵$A,B$证明\[\det(I+A+B)\le\det(I+A)\det(I+B)\]
不妨将$A$正交对角化，例如$A=P\operatorname{diag}(\lambda_1,\ldots,\lambda_m)P^{-1}$，于是只需证明\[\det(I+\operatorname{diag}(\lambda_1,\ldots,\lambda_m)+B')\le\det(I+B')\prod_{i=1}^{n}(1+\lambda_i)\]对任意实对称半正定矩阵$B'$成立。

首先设除了$\lambda_1$外其余$\lambda_i=0$，则只需证明\[\det(\lambda_1e_1e_1^T+B'')\le\det(B'')(1+\lambda_1)\]其中$e_1=(1,0,\ldots,0)^T$而$B''=I+B$是正定实对称矩阵且特征值都不小于1。但是行列式按行展开有\[\det(\lambda_1e_1e_1^T+B'')=\lambda_1\det(B''_{1,1})+\det(B'')\]
其中$B''_{1,1}$是由$B''$删去第一行第一列得到的矩阵。这样只需证明$\det(B''_{1,1})\le\det(B'')$。而又注意到$\det(B''_{1,1})/\det(B'')$恰好是$(B'')^{-1}$的第一行第一列元素，从而约化为证明
{{<theorem 2>}}设$B$是实对称正定矩阵且特征值不大于1，则其第一行第一列元素不大于1。{{</theorem>}}
这是因为$e_1^TBe_1\le1$。

一般情形下逐步加上各$\lambda_i$即可。

---

正在寻找更美观的解答。