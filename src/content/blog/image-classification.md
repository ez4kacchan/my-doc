---
author: Đào Vũ Hưng
pubDatetime: 2025-03-02T06:00:53Z
title: Image Classfication
featured: false
draft: false
tags:
  - computer-vision
description: Dao Vu Hung
---
## Table of contents
## 1. Cac huong di
### 1.1. Ham nhan dien hinh anh
Neu nhu xem viec nhan dien hinh anh giong nhu sap xep mot day so. Thi chung ta cung can **mot ham** va co cac thuat toan de nhan dien giong nhu thuat toan sap xep. Tuy nhien viec nhan dien hinh anh **khong** co cac **phuong phap cu the** nao de nhan dien khong nhu sap xep day so se co cac thuat toan nhu linear search binary search.

Vay thi lam sao de thiet ket mot ham de nhan dien hinh anh. Mot trong nhung cach la dung **hieu biet** cua **con nguoi**. Vi du nhu: khi nhan dien con meo, ta co the dung thuat toan **edge detection** va dua hieu biet cua chung ta, define lo tai con meo se co edge nhu the nao va nhan dien dua vao do.

Tuy nhien phuong phap tren gap mot vai van de nghiem trong. Neu nhu edge detection **khong** nhan dien duoc con meo mot cach **day du** thi sao. Nhu vay se thieu thong tin. The thi khi nhan dien lai khong tra ve ket qua chinh xac. Tom lai, ta co the thay phuong phap ay **khong** co su **manh me**.
### 1.2. May hoc
Phuong phap tren tro nen vo cung phuc tap khi chung ta thay doi muc tieu can nhan dien. Ngay nay, da co mot phuong phap manh me hon. Day chinh la **may hoc**, vay thi may hoc hoat dong nhu nao? Dau tien, chung ta can mot luong lon **du lieu** ve **muc tieu** can nhan dien. Tiep den se dung may hoc de xay dung **classifer**. Va chung ta se danh gia **hieu suat** cua classifier ay tren hinh anh moi.
#### 1.2.1. Nearest Neighbors
Ve mat toan, mot dieu quan trong ve thuat toan cua tim diem lan can nay la viec tinh toan **khoang cach** giua diem dang xet va cac diem xung quanh de chon ra cac **diem lan can**. Va tu cac diem lan can, co the phat trien them thanh viec lua ra dac trung chung giua cac nhom lan can.

Viec **lua chon** **so diem lan can** anh huong rat lon toi **cau truc** cua du lieu. Neu nhu so diem lan can **thap** co the bi cac **noise** lam anh huong , khi **tang** so diem lan can len thi cac cau truc tro nen ro ret va **smooth** hon.

Ngoai ra mot dieu quan trong nua ve nearest neighbors la ve **do do** khoang cach duoc su dung. Ket qua thu duoc se vo cung khac khi su L1 va L2.

Tuy nhien, cung phai nho rang cac thong so o tren khong thuoc ve qua trinh may hoc, tuc la **khong nam** trong **viec hoc** cua may. Day la nhung thong so duoc **cai dat san** de phan anh du lieu mot cach **hieu qua** nhat. Cac thong so ay con duoc goi la **hyperparameter**.
## 2. Thong so hyperparameter
Nhu vay, lam sao de chung ta kiem thong so hyper parameter phu hop nhat voi thuat toan de giai quyet bai toan cu the. Dieu duy nhat co the lam la chung ta thu nghiem tren tap du lieu va chon ra gia tri dem lai ket qua tot nhat.

Hien nay. ton tai 2 cach de xu ly tap du lieu. Cach thu nhat la chia tap du thanh **3 phan**: training, validation, va test. Cach thu hai la **cross-validation**. Ca hai phuong phap nay deu dam bao ve tinh tong quat cua thuat toan tren cac du lieu **chua** tung duoc **nhin thay**.
## 3. Tap du lieu
