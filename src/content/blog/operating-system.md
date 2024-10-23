---
author: Đào Vũ Hưng
pubDatetime: 2024-10-22T22:49:54+07:00
title: Hệ điều hành
featured: false
draft: false
tags:
  - academic
  - operating-system
description: Cùng tìm hiểu về operating system
---

# Approach

## 1.1.  Khái niệm chung về Operating System
 Hệ điều hành là phần chịu trách nhiệm chạy ứng dụng, thậm chí là nhiều ứng dụng của một lúc, cho phép ứng dụng chia sẻ bộ nhớ, tượng tác với các thiết bị. 
 
 Tóm lại là phần **trung gian** giữa phần cứng và người dùng. **Điều khiển** phần cứng và **cung cấp** dịch vụ cho người dùng.
 ![os](../../assets/images/os.png)
### 1.2. Cách hệ điều hành hoạt động
**Easy to use**: vì đó chỉ gồm 3 phần:
- Nhân(kernel): luôn hoạt động khi máy tính hoạt động
- Chương trình hệ thống: được đóng gói cùng với lại hệ thống nhưng không phải nhân
- Chương trình ứng dụng: tất cả các chương trình không có liên quan đến hệ thống

 ![event bus](../../assets/images/event_bus.png)
- Các thiết bị như mouse, keyboard được điều khiển như thế nào?
- Sytem bus hoạt động ra sao
#### 1.2.1. Đồng thời
- Có mốt vấn đề về hiệu điều hành đó là nó chạy từng câu lệnh. 
- Vậy thì làm sao để thiết bị I/O và CPU chạy đồng thời? Ngày nay thì đó là yêu cầu cần thiết
	- Đầu tiên, các thiết bị I/O được điều khiển bởi các **trình điều khiển thiết bị** (device drivers).
	- Khi có nhiều thiết bị I/O thì máy xử lý như thế nào, phải qua một cái bus để kết nối tới **memory** và cả **CPU**
	- Khi trình điều khiển thiết bị xử lý xong sẽ kết thúc thông qua thao tác **ngắt** (Interrupt)
##### 1.2.1.1. Trình điều khiển thiết bị 
- Có những numbers được hệ thống gán cho từng thiết bị như là những index trên hệ thống. Dựa vào những **index** đó mà hệ thống biết device drivers nào xử lý thiết bị nào.
- 70% dòng code của hệ điều hành liên quán tới trình điều khiển thiết bị.

##### 1.2.1.2. Ngắt 
- Ngắt là cơ chế khi mà các thiết bị muốn **thông báo** cho CPU rằng có data muốn truyền hay khi hoạt động đã hoàn thành.
- Hệ điều hành hoạt động theo hướng **ngắt**
- Ngắt làm cho CPU chuyển đến interrupt service routine thông qua interrupt vector (chứa địa chỉ)