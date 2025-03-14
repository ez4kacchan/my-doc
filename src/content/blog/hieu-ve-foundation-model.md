---
author: Đào Vũ Hưng
pubDatetime: 2025-03-13T10:37:17Z
title: Hieu ve Foundation Model
featured: false
draft: false
tags:
  - ai-engineering
description: Dao Vu Hung
---
## Table of contents
## 1. Training Data 
Khi nói về việc *huấn luyện AI*, có một nguyên tắc cốt lõi mà chúng ta cần hiểu rõ: *chất lượng* của *mô hình* *phụ thuộc* **trực tiếp** vào chất lượng *dữ liệu* mà nó được đào tạo. Hãy tưởng tượng một mô hình *dịch thuật* – nếu dữ liệu huấn luyện của nó hoàn toàn *không chứa* *tiếng Việt*, thì dù có **mạnh mẽ** đến đâu, mô hình cũng không thể dịch từ tiếng Anh sang tiếng Việt. Đây chính là lý do vì sao việc chọn lọc và xây dựng dữ liệu đầu vào đóng vai trò **then chốt** trong quá trình phát triển AI.

Như vậy, để mô hình có thể giải quyết các bài toán thuộc về **chuyên sâu** của các lĩnh vực, thì đòi hỏi chúng ta phải **chắt lọc** dữ liệu một cách hợp lý.
## 2. Modeling
Đối với các model nhỏ, việc thường làm là lựa chọn các hyperparameter khác nhau và xem hyperparameter nào cho kết quả tốt nhất. Tuy nhiên, đối với các model lớn thì việc thay đổi hyperparameter rất tốn tài nguyên
## 3. Post-Training
Post-training một model đã được pre-training giúp cho model output đáng tin hơn và phù hợp với con người. Một cách hiểu đơn giản thì pre-training giúp model học được những kiến thức cơ bản, còn post-training giúp model có thể ứng dụng những kiến thức đã học.

Như vậy, model ở bước post-training thông thường được đi qua các bước sau: unsupervised learning, supervised fine-tuning, và cuối cùng là reinforcement learning from human feedback (RLHF).