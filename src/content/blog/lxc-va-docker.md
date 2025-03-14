---
author: Đào Vũ Hưng
pubDatetime: 2025-03-12T09:33:31Z
title: LXC va Docker
featured: false
draft: false
tags:
  - container
description: Dao Vu Hung
---
## Table of contents
## 1. Su khac biet 
Sự **giống nhau** giữa LXC và Docker là mục đích **tạo** ra các **container** với môi trường riêng biệt dựa trên khả năng của Linux kernel. Tuy nhiên, **hướng đi** và **ứng dụng** của mỗi cái lại vô cùng **khác nhau**.

Có một điều khác biệt rõ ràng là LXC được xây dựng trên **mức độ OS**, tức là trên hệ điều hành hiện tại, tạo ra các container là các hệ điều hành khác. Còn về Docker, thì nó được xây dựng trên **mức độ ứng dụng** với mục đích là tạo ra các môi trường độc lập giữa các ứng dụng