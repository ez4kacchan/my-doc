---
author: Đào Vũ Hưng
pubDatetime: 2024-12-03T04:22:07Z
title: Đồng bộ tiến trình
featured: false
draft: false
tags:
  - operating-system
description: Vu Hung
---
## Table of contents
## 1. Race condition
Trongbài toán **Producer & Consumer** biến **count** được **truy cập** bởi cả quá trình. Trong bài toán **Cấp PID**, nếu cả 2 process khác nhau đều **fork()** cùng 1 lúc thì **next_availiable_pid()** được **truy cập** bởi 2 processes.
-> cần một cơ chế để đảm bảo thự tứ trước sau -> **race condition**

## 2.