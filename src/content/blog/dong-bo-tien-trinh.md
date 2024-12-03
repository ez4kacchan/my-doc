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

## 2. Vùng tranh chấp - Critical Section
Là vùng của các tiến trình, mà tại đó thực hiện việc truy cập các dữ liệu được **chia sẻ chung** và tại **1 thời điểm** chỉ có **1** tiến trình được truy cập.

Qúa trình **truy cập** critical section của tiến trình: 
- Yêu cầu đến entry section -> vào critical section -> thoát ra bởi exit section -> thực thi phần còn lại remainder section
![image](../../assets/images/2024-12-03_14-17-15.png)

