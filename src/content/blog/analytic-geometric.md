---
author: Đào Vũ Hưng
pubDatetime: 2024-11-28T05:05:25Z
title: Analytic Geometric
featured: false
draft: false
tags:
  - mathematics
description: Vu Hung
---
## Table of contents
## 1. Các khái niệm liên quan
### 1.1. Vector space
$$
Example:  P(x) = a_0 + a_1x + \cdots + a_nx^n 
$$
Là **tổng** các vector, các vector có thể được **nhân** với scalar. 
- Kí hiệu phần tổng: 
$$
+ : V \times V \to V, \quad (u, v) \mapsto u + v
$$
- Kí hiệu phần nhân: 
$$
\cdot : \mathbb{F} \times V \to V, \quad (c, v) \mapsto c \cdot v
$$
Real vector space:

Complex vector space:
### 1.2. Inner Product 
Inner Product tức tích vô hướng, được **dùng bởi** các phép toán khác của Vector Space

Kí hiệu: 
$$
\langle \cdot, \cdot \rangle : V \times V \to \mathbb{F}
$$
Tính chất:
$$
\langle u + w, v \rangle = \langle u + v\rangle + \langle w + v\rangle 
$$
$$
 \langle cu, w\rangle= c \cdot \langle u,w \rangle
$$
Inner Product Space:
$$
(V, \langle \cdot,\cdot \rangle) 
$$
## 2. Các khái niệm chính
### 2.1. Norm 
Là **độ dài** trong không gian của vector
$$
\|\cdot\| : V \to \mathbb{R}
$$
Khi đó: vector u, v đều $\in V$  và scalar $c \in \mathbb{R}$ 

Tính chất:
1. Non-negatie: $$
\|\mathbf{v}\| \geq 0 \quad \text{and} \quad \|\mathbf{v}\| = 0 \iff \mathbf{v} = \mathbf{0}.
$$
2. Absolute Homogeneous $$
   \|c \cdot \mathbf{v}\| = |c| \cdot \|\mathbf{v}\|
$$
3. Triangle Inequality: $$
\|\mathbf{u} + \mathbf{v}\| \leq \|\mathbf{u}\| + \|\mathbf{v}\|.
$$

### 2.2. Length
Ở trong Inner Product Space, Norm được tính theo công thức:
$$
\|\mathbf{v}\| = \sqrt{\langle \mathbf{v}, \mathbf{v} \rangle}
$$
**Không** phải **tất cả** Norm được tính như trên. Thường áp dụng cho **Euclidean Norm** 
### 2.3. Distance
Sử dụng norm: $$
  d(\mathbf{x}, \mathbf{y}) = \|\mathbf{x} - \mathbf{y}\|
$$
Nếu inner product sử dụng **dot product** trên tập $\mathbb{R}^n$  thì được gọi là **Euclidian Distance**

Distance được gọi là **metric** khi: 
1. Positive Definite: $$
  d(\mathbf{x}, \mathbf{y}) \geq 0 \quad \text{for all } \mathbf{x}, \mathbf{y} \quad \text{and}\quad d(\mathbf{x}, \mathbf{y}) = 0 \iff \mathbf{x} = \mathbf{y}
$$
2. Symmetric: $$
   d(\mathbf{x}, \mathbf{y}) = d(\mathbf{y}, \mathbf{x})
$$
3. Triangle Inequality: $$
  d(\mathbf{x}, \mathbf{z}) \leq d(\mathbf{x}, \mathbf{y}) + d(\mathbf{y}, \mathbf{z})
$$
### 2.4. Feature Vectors và Feature Distance
Một ví dụ của Feature Vector là **RGB**: $[R,G,B]$
Nếu $x, y$ là hai Feature vectors của **hai entities** thì $\|\mathbf{x} - \mathbf{y}\|$ là **feature distance**
=> Nearest khi mà $\|\mathbf{x} - \mathbf{y}\|$ nhỏ nhất
=>$\mathbf{z}_{j}$ là nearest neighbor nếu: $$
     \|\mathbf{x} - \mathbf{z}_j\| \leq \|\mathbf{x} - \mathbf{z}_i\|, \quad \forall i = 1, 2, \dots, m.
$$
