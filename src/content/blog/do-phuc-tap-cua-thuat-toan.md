---
author: Đào Vũ Hưng
pubDatetime: 2025-02-26T04:23:45Z
title: Do phuc tap cua thuat toan
featured: false
draft: false
tags:
  - algorithm
description: Dao Vu Hung
---
## Table of contents
## 1. Mot vai khai niem
### 1.1. Dinh nghia
O notation duoc dung de **so sanh** va xep hang muc do tang truoc cua cac ham. Su tang truong duoc xem xet o day la **thoi gian** va **dung luong** yeu cau. Tom lai O notation mieu ta su tang truong cua yeu cau ve thoi gian va dung luong khi ma **tep du lieu** dau vao **tang**.

Ve co ban, co 2 cach chinh de tinh toan do phuc tap. Thu nhat la tinh thoi gian thuc thi thuc te cua thuat toan. Thu hai la phan tich ve mat toan cua thuat toan.
### 1.2. Toc do tang truong
Goi cop la thoi gian thuc hien mot basic operation va Cn la so lan operation do xuat hien. Thoi gian thuc hien tong = cop.Cn

O cac ham Cn, su khac biet giua hai thuat toan chi ro ret khi n cang lon.
### 1.3. Dau vao
Tuy nhien, lieu O chi phu thuoc dau vao la so luong mau du lieu hay khong? Cau tra loi la khong. Ngoai phu thuoc vao so luong mau du lieu, do phuc tap con phu thuoc vao mot so yeu to khac voi cung mot luong mau du lieu xac dinh.

Khi do, hinh thanh khai niem ve worst-case, average-case va best-case. 

Worst-case la khi thuat toan duoc cung cap mot tap du lieu xac dinh ma tai do thoi gian xu ly la lau nhat.

Best-case la khi thuat toan duoc cung cap mot tap du lieu xac dinh ma tai do thoi gian xu ly la ngan nhat.

Tuy nhien, khi doi dien voi tap du lieu no random, thi ca worst-case va best-case khong mieu ta duoc. Do do co average-case.
## 2. Do phuc tap cua thuat toan de quy
Tìm kiếm độ phức tạp của các thuật toán đệ quy cũng giống như đối với hàm khong đệ quy vậy. Việc chúng ta cần làm là xác định số lần xuất hiện của các phép toán cơ bản.

Tuy nhiên, khong the xác định được một hàm tính số lần xuất hiện của phép toán cơ bản một cách tường minh

Cụ thể, ta có các bước như sau:  
**Bước 1:** Xác định kích thước của dữ liệu và đầu vào.  
**Bước 2:** Xác định các phép toán cơ bản có trong hàm.  
**Bước 3:** Xác định xem các phép toán ấy có bị ảnh hưởng bởi các yếu tố khác hay không. Từ đó, phân chia thành các trường hợp tốt nhất, trung bình, xấu nhất.  
**Bước 4:** Tìm hệ thức truy hồi với một điểm bắt đầu hợp lý để tính được số lần xuất hiện của các phép toán cơ bản.  
**Bước 5:** Thực hiện giải hệ thức ấy.
## 3. Ap dung