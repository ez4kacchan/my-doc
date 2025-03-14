---
author: Đào Vũ Hưng
pubDatetime: 2025-03-06T07:46:02Z
title: Phan loai van ban trong NLP
featured: false
draft: false
tags:
  - natural-language-processing
description: Dao Vu Hung
---
## Table of contents
## 1. Phan loai  
Phan loai van ban bao gom viec **gan nhan** cho cac doan van ban. Vi du nhu: **sentiment analysis**, tuc la chung ta gan cho cac doan van ban cac **trang thai cam xuc**. Trang thai cam xuc co the la tieu cuc, tich cuc va trung lap. Ngoai ra con co **spam detection**, tuc la chung ta danh gia xem doan van ban ay co phai la thu rac hay la **khong.
## 2. Sentiment Analysis

**Ung dung** cua sentiment analysis co the thay o viec phan tich cac phan hoi cua nguoi dung.

Vay sentiment analysis hoat dong nhu the nao. Co 2 phuong phap giup chung ta phan tich. Cach thu nhat cung la cach pho thong nhat, day la su dung **lexicon**. Tuc la su dung cac **tu dien** sentiment. Thi cac tu dien nay chua cac **thang diem** ung voi moi tu . De ma tu do chung ta co the xac dinh duoc sentiment cua mot doan van ban dua tren thang diem tong **tinh toan** duoc. Ngoai ra, cach thu hai la chung ta su dung **deep learning**.

Khi di theo huong lexicon, ton tai mot vai **kho khan** nhu sau. Thu nhat, sentiment phu thuoc rat nhieu vao **chu the**. Cai thu hai la **hoan canh** viet hay hoan canh cua van ban cung anh huong rat lon den su tich cuc hay tieu cuc cua van ban. Chinh vi nhu the, neu chi phu thuoc vao lexicon thoi thi cung kho danh gia duoc mot cac chinh xac nhat co the.
### 2.1. Cach tiep can
Sentiment analysis yeu cau xem xet cac tu ngu la **doc lap** va **khong** co **thu tu** (bag of word). Tu do ta co the chia cau thanh cac tu va su dung **naives bayes** de tinh xac suat.

Gia su mot du lieu training, duoc chia thanh 3 nhan positive, negative, va neutral . Nhu vay ta co the tinh xac suat cua cac tu ngu duoc chia vao nhan nao. Tu do giup tinh toan xac suat cua mot cau thuoc nhan nao khi test.
#### 2.1.1. MLC va Naive Bayers Classifier
Sự  khác biệt giữa 2 classifier nằm ở chỗ xác suất được cài đặt sẵn. Thế thì ở Naïve Bayes, chúng ta có thông tin về xác suất rơi vào các nhãn của câu nay dựa vào các câu ở phía trước. Còn ở MLC, không có thông tin như vậy. Chúng ta phải tính xác suất của mỗi câu một cách độc lập mà không có thông tin gì về câu ở phía trước. Như vậy, Naïve Bayes classifier sẽ có một chút bias dựa vào thông tin được cung cấp
#### 2.1.2. Naive Bayers Classifier va Logistic Regression Classifier
Sự khác biệt thể hiện ở **tính chất** của mỗi thuật toán. Naive Bayes classifier là **generative model** còn logistic regression là **discriminative model**. Vậy hai mô hình này có gì khác nhau?

Cụ thể hơn, generative model có **thông tin** về xác suất của từng dạng được cài đặt từ trước. Đây chính là prior probability. Còn discriminative thì không có thông tin này. Nó giống như việc nhận dạng giữa con mèo và con chó. Naive Bayes được **biết** các thông tin về một con mèo thì như thế nào, con chó thì như thế nào. Còn discriminative thì phải tự đi tìm sự khác biệt, sự khác biệt ấy có thể là con chó được đeo kính còn con mèo thì không.