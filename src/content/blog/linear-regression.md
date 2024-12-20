---
author: Đào Vũ Hưng
pubDatetime: 2024-12-18T03:01:54Z
title: Linear Regression
featured: false
draft: false
tags:
  - mathematics
description: Vu Hung
---
## Table of contents
## 1. Khái niệm liên quan
### 1.1. Linear 
Linear hay tuyến tính để chỉ những function được biểu diễn là **đường thẳng** trên **đồ thị**
## 2. Khái niệm chính
### 2.1. Dạng cơ bản
$$
X \bar{\theta} \approx \bar{y}
$$
Với:
$$
\mathbf{X} \text{: data matrix or features} \quad \bar{\boldsymbol{\theta}} \text{: parameter vector}
$$

Xét $X \in R^{m \times n}, \quad \bar{\theta} \in R^{n \times l}, \quad \bar{y} \in R^{m \times l}$
- Nếu $m = n$:
$$
X \bar{\theta} = \bar{y}
\leftrightarrow \bar{\theta} = X^{T}\bar{y}
$$

- Nếu $m < n$: thiếu **data** so với số lượng **feature**
$$
\begin{align}
X^T X \bar{\theta} &= (X^TX)^{-1}X^T \bar{y} \\
&= X^{+} \bar{y} \quad \text{với} \quad (X^TX)^{-1}X^T = X^{+}
\end{align}
$$
### 2.2. Kiểm tra độ chính xác?
#### 2.2.1. Error
Khái niệm: error = actual - prediction

Kiểm tra dấu:
- **Error = 0**: biểu diễn **đúng** độ lệch của mô hình
- **Error > 0**: biểu diễn **đúng** độ lệch của mô hình
- **Error < 0**: biểu diễn **sai** độ lệch của mô hình vì hai giá trị error **ngược dấu** nhau

Do đó **cần** một mô hình khác
#### 2.2.2. MSE
Mean Square Error tức **trung bình** của bình phương error. Khi bình phương thì **không** còn **lạc loài** trường hợp ngược dấu. Từ đó **giúp** cho quá trình **evaluation**

Để giúp ích cho việc tìm ra giá trị weight sát nhất. Ta để MSE nhỏ nhất, tức đạo hàm của nó sẽ bằng 0. Xét: 
$$
J(\bar{\theta}) = \frac{1}{n} \sum_{t=1}^{n} \frac{1}{2} \left[ y^{(t)} - \bar{\theta} \cdot \bar{x}^{(t)} \right]^2
$$

Thực hiện đạo hàm phần $\frac{\partial}{\partial \theta_{i}}J(\bar{\theta})$ , suppose $g() = \bar{\theta}\bar{x}^{(t)}$
$$
\begin{align} \\
\frac{\partial}{\partial \theta_i} J(\bar{\theta}) &= \frac{\partial J}{\partial g(\theta_{i})} \frac{\partial g}{\partial \theta_{i}} \\
&= \frac{1}{n} \sum_{t=1}^n \left[ y^{(t)} - \left( x_1^{(t)} \theta_1 + x_2^{(t)} \theta_2 + \cdots + x_d^{(t)} \theta_d \right) \right] \left( -x_i^{(t)} \right) \\
&= \frac{1}{n} \sum_{t=1}^n \left[ y^{(t)} - \left( \bar{x}^{(t)} \right)^T \bar{\theta} \right] \left( -x_i^{(t)} \right)
\end{align}
$$

Khi đó:
$$
\frac{1}{n}\sum_{t=1}^n (x_{i}^{(t)} \left(\bar{x}^{(t)} \right) ^T \bar{\theta}) = \frac{1}{n} \sum_{t=1}^n x_{i}^{(t)}y^{(t)}
$$
Rút gọn:
$$
\sum_{t=1}^n (x_{i}^{(t)} \left(\bar{x}^{(t)} \right) ^T \bar{\theta}) = \sum_{t=1}^n x_{i}^{(t)}y^{(t)}
$$
Ta có $\left( \bar{x}^{(t)} \right)^T \in R^d$ , để ý $x_i^{(t)}$ có thể viết lại dưới dạng $\bar{x}^{(t)}$:
$$
\sum_{t=1}^n \bar{x}^{(t)} \left(\bar{x}^{(t)}\right)^T \bar{\theta}= \sum_{t=1}^n \bar{x}^{(t)}y^{(t)}
$$
Ma trận $X^T = x^{(t)} \in R^{d\times n}, \quad X = \left(\bar{x}^{(t)}\right)^T \in R^{n\times d}$ 
Giống với:
$$
X^TX \bar{\theta} = X^T \bar{y}^{(t)}
$$
