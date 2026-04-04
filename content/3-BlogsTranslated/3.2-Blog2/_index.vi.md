---
title: "Blog 2"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.2. </b> "
---

# Aigen đã cải tiến robot nông nghiệp bằng Amazon SageMaker AI như thế nào

Bài viết này mô tả cách công ty Aigen sử dụng AWS để cải tiến hệ thống machine learning cho robot nông nghiệp, nhằm hướng tới sản xuất nông nghiệp bền vững.

Aigen phát triển các robot tự động có khả năng nhận diện và loại bỏ cỏ dại bằng AI thay vì sử dụng hóa chất. Tuy nhiên, hệ thống ban đầu gặp nhiều hạn chế.

---

## Các vấn đề ban đầu

Aigen gặp phải nhiều khó khăn:

- Hạn chế về tài nguyên tính toán (on-premise)
- Chi phí cao cho việc gán nhãn dữ liệu
- Khó mở rộng hệ thống
- Kết nối mạng không ổn định ở nông thôn
  Làm giảm hiệu quả của hệ thống

---

## Giải pháp trên AWS

Aigen chuyển sang kiến trúc cloud-native sử dụng AWS.

### Thu thập dữ liệu

- Robot gửi dữ liệu qua AWS IoT Core
- Lưu trữ trên Amazon S3

Dữ liệu gồm:

- Hình ảnh
- Thông tin cảm biến
- Metadata

---

### Xử lý và gán nhãn dữ liệu

- Sử dụng AI để tự động gán nhãn
- Kết hợp con người kiểm tra (human-in-the-loop)
- Áp dụng active learning

Giảm đáng kể công sức thủ công

---

### Huấn luyện mô hình

- Sử dụng Amazon SageMaker
- Train trên GPU mạnh
- Hỗ trợ training phân tán

Tăng tốc độ và hiệu suất

---

## Kiến trúc mô hình

Hệ thống gồm nhiều loại model:

- **Foundation models** → xử lý tổng quát
- **Expert models** → chuyên biệt
- **Student models** → tối ưu hóa
- **Edge models** → chạy trên robot

Cân bằng giữa độ chính xác và hiệu năng

---

## Pipeline học liên tục

Quy trình hoạt động:

1. Thu thập dữ liệu
2. Xử lý và gán nhãn
3. Train model
4. Deploy lên robot
5. Thu thập dữ liệu mới

Liên tục cải thiện model

---

## Kết quả đạt được

- Giảm chi phí gán nhãn hơn **20 lần**
- Tăng tốc độ xử lý dữ liệu
- Tăng số lượng experiment đáng kể
- Cải thiện hiệu suất hệ thống

---

## Bài học rút ra

- Cloud giúp mở rộng dễ dàng
- Tự động hóa giảm chi phí
- AI + con người đảm bảo chất lượng
- Continuous learning giúp hệ thống ngày càng tốt hơn

---

## Kết luận

Bài viết cho thấy cách kết hợp các dịch vụ AWS như S3, IoT Core và SageMaker để xây dựng hệ thống AI quy mô lớn.

Đây là một ví dụ điển hình cho việc ứng dụng cloud và AI vào các bài toán thực tế như nông nghiệp thông minh.
