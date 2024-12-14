---
author: Đào Vũ Hưng
pubDatetime: 2024-12-13T07:33:00Z
title: TRIGGER trong SQL
featured: false
draft: false
tags:
  - sql
  - learn-and-understand
description: Vu Hung
---
## Table of contents
## 1. Kiến thức liên quan
## 2. Khái niệm chính
TRIGGER là một phần của **ràng buộc toàn vẹn**, cung cấp những **khả năng** mà **CONSTRAINT** không thể làm được.
### 2.1. Thao tác với TRIGGER
Một vài thao tác **chính** sử dụng trong **SQLSERVER**

| Chức năng | Cú pháp               |
| --------- | --------------------- |
| Tạo       | CREATE TRIGGER 'name' |
| Chỉnh sửa | ALTER TRIGGER 'name'  |
| Xóa       | DROP TRIGGER 'name'   |

### 2.2. Cú pháp tạo TRIGGER
```sql
CREATE TRIGGER TEN_TRIGGER 
on TEN_TABLE
<CHUCNANG>
AS
BEGIN
	/*Function ở đây*/
END;
```