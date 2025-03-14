---
author: Đào Vũ Hưng
pubDatetime: 2025-03-10T06:12:01Z
title: Socket Programming
featured: false
draft: false
tags:
  - software-development
description: Dao Vu Hung
---
## Table of contents
## 1. Client va Server
**Cả** client và server đều phải tạo **endpoint** để có thể giao tiếp với nhau. Ở client, việc tạo endpoint yêu cầu phải **khai báo** địa chỉ **IP và port** của server để nó có thể **thiết lập** kết nối. Còn ở server, việc đó đơn giản hơn khi **chỉ** cần phải khởi tạo **port** cần được mở để **lắng nghe** thông tin từ client.

Kết nối giữa client và server được thiết lập bởi **2 socket**, một ở client và một ở server. Về cơ bản, bước đầu tiên là phải gán endpoint vào socket. Và tùy thuộc vào việc ở client hay server mà **gọi tới** hàm `listen` hay `connect` của socket.