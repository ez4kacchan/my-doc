---
author: Đào Vũ Hưng
pubDatetime: 2025-03-08T10:17:49Z
title: Co ban ve Foundation Model
featured: false
draft: false
tags:
  - ai-engineering
description: Dao Vu Hung
---
## Table of contents
## 1. Language model
Có **2 loại** language model chính. Chúng được phân biệt với nhau dựa trên sự khác biệt về **thông tin** được **sử dụng** để dự đoán

Loai thu nhat la **masked** language model. Model nay duoc dung de du doan cac token **con thieu** trong mot sequence bang cach su dung thong tin ve context **truoc va sau** token bi thieu. Lay vi du: my favourite ___ is blue.

Trong van ban, model nay duoc su dung cho cac tac vu **khong sinh** nhu sentiment analysis va text classification. Va no cung rat huu dung voi cac van de yeu cau hieu **overall context** nhu code debugging khi thong tin ve  phan truoc va sau de sua loi. 

Loại thứ hai là **autoregressive** model. Model này **khác** với masked language model ở chỗ nó sử dụng các **token** ở **phía trước** để dự đoán token ở **phía sau**. Như vậy, các token được dự đoán thường nằm ở **cuối câu**, hay cuối một sequence. Trong các ứng dụng của autoregressive model, ứng dụng để **sinh văn bản** là nổi bật nhất. Cũng vì lý do đó mà autoregressive model phổ biến hơn masked language model.
### 1.1. Supervision va Self-Supervision
Supervision là phương pháp phổ thông để **cung cấp dữ liệu** cho model. Bằng cách **gán nhãn** các dữ liệu để model có thể xác định kết quả mong muốn đối với từng dữ liệu. Từ đó, thông qua việc train model để nó có thể xử lý trên tập **dữ liệu mới**.

Lấy ví dụ: bài toán spam detection. Chúng ta gán nhãn spam và not spam cho các đoạn text để model có thể trả lời

Tuy nhiên, việc gán nhãn cho từng dữ liệu như vậy yêu cầu rất nhiều sức lao động và chi phí.

Ngày nay, các model được train dựa trên **self-supervision**. Tức là model có thể **tự học** từ các sequence van ban thay vì phải label từng sequence. Như thế, công việc tạo ra dữ liệu để train trở nên dễ dàng hơn và **dễ scale** hơn khi mà các text sequence ngày nay có vô vàn trên internet.
## 2. Len ke hoach cho ung dung AI 
Bởi vì **rào cản** xây dựng ứng dụng AI khá là **thấp**, cho nên nhiều doanh nghiệp có thể tiếp cận được. Nếu quá trình xây dựng quá dễ dàng thì đối thủ cũng dễ dàng làm được.

Như vậy, có một dieu cần được xem xét khi xây dựng ứng dụng AI.Đó là nếu lớp layer chúng ta xây dựng trên foundation model quá đơn giản và khi foundation model cải tiến, nó có thể được cập nhật tính năng đó.

Lấy ví dụ: xây dựng tính năng PDF parsing trên ChatGPT có thể bi thay the bởi các phiên bản ChatGPT tiếp theo chỉ với 1 hay 2 engineer.

Trong ngành AI, tóm lại có **3** loại **lợi thế cạnh tranh**: **công nghệ, dữ liệu và cách phân phối**. Khi xây dựng ứng dụng trên foundation model, các công nghệ **cốt lõi** là **giống nhau** trên các nền tảng. Ngoài ra, **cách phân phối** ứng dụng đến người dùng thì các công ty lớn có một lợi thế.

Như vậy, chúng ta cần phải tập trung vào dữ liệu. Bởi mặc dù các doanh nghiệp thì chắc chắn họ có dữ liệu, còn chúng ta thì không. Nhưng nếu chúng ta **vào** thị trường **trước**, thì **dữ liệu** chúng ta thu thập được sẽ rất **có ích** để cải thiện model hoặc ít ra nhan duoc những insight cần thiết để cải thiện.
