---
author: Đào Vũ Hưng
pubDatetime: 2024-12-03T04:22:07Z
title: Vector Calculus
featured: false
draft: false
tags:
  - mathematics
description: Vu Hung
---
## Table of contents
## 1.  Các khái niệm liên quan
### 1.1. Smooth Function
Có tính chất **infinitely differentiable**. 
### 1.2. Complex Space
Kí hiệu: $\mathbb{C}$ 
## 2. Các khái niệm chính
### 2.1. Taylor Series
Mục đích: để có một function khác **giống** function đang tìm hiểu. 
ELI5: Biến một đường cong **xấu xí** thành một đường cong **dịu dàng**

Taylor Polynomial: bậc n của hàm $f:\mathbb{R} \to \mathbb{R}$ tại điểm $x_{0}$
$$
T_n(x):=\sum_{k=0}^n\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k
$$

Taylor Series: $f \in \mathbb{C}^{\infty}$
$$
T_\infty(x):=\sum_{k=0}^\infty\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k
$$
is **called** analytic if $f(x)=T_{\infty}(x)$