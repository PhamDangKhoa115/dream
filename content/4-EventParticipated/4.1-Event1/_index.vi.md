---
title: "Event 1"
date: 2026-04-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Sự kiện 1: Building Full-Stack Observability on AWS with Datadog

### Thông tin sự kiện

- **Tên sự kiện:** Building Full-Stack Observability on AWS with Datadog
- **Thời gian:** 14:00 - 17:00, ngày 27 tháng 2
- **Địa điểm:** Tầng 26, Bitexco Tower, 02 Hải Triều, Phường Sài Gòn, TP. Hồ Chí Minh
- **Vai trò:** Người tham gia

---

### Đọc giả

- **Ngoc Anh** – Accountant Executive
- **Hải Bằng** – Solution Engineer
- **Emilea Teo** – Solution Engineer

---

## Mô tả sự kiện

Sự kiện này giới thiệu khái niệm **Full-Stack Observability** và cách triển khai nó trên môi trường AWS bằng Datadog.

Buổi chia sẻ tập trung vào việc các ứng dụng hiện đại (đặc biệt là cloud-native và microservices) cần có khả năng quan sát toàn diện trên tất cả các tầng của hệ thống nhằm đảm bảo hiệu năng, độ ổn định và trải nghiệm người dùng.

---

## Full-Stack Observability là gì?

Full-stack observability là khả năng giám sát và phân tích toàn bộ hệ thống, bao gồm:

- Frontend (trải nghiệm người dùng, hiệu năng trình duyệt)
- Backend (API, service, logic nghiệp vụ)
- Infrastructure (server, container, tài nguyên cloud)

Nó được xây dựng dựa trên ba thành phần chính:

- **Metrics** → dữ liệu dạng số (CPU, RAM, độ trễ)
- **Logs** → nhật ký hệ thống
- **Traces** → luồng request giữa các service

---

## Tổng quan về Datadog

Datadog là một nền tảng observability trên cloud, cung cấp hệ thống giám sát hợp nhất cho các ứng dụng hiện đại.

Các khả năng chính bao gồm:

- Thu thập dữ liệu từ server, container, database và cloud
- Trực quan hóa hiệu năng hệ thống theo thời gian thực
- Liên kết logs, metrics và traces trong cùng một dashboard
- Hỗ trợ AWS, multi-cloud và hybrid cloud

---

## Các tính năng chính của Datadog

### Giám sát hợp nhất (Unified Monitoring)

- Kết hợp tất cả dữ liệu giám sát trong một dashboard
- Quan sát toàn bộ trạng thái hệ thống theo thời gian thực

---

### Truy vết phân tán (Distributed Tracing - APM)

- Theo dõi luồng request giữa các microservices
- Xác định các điểm nghẽn trong hệ thống

---

### Quản lý Logs

- Thu thập và phân tích logs từ nhiều nguồn
- Kết hợp logs với metrics và traces

---

### Giám sát hạ tầng (Infrastructure Monitoring)

- Theo dõi CPU, RAM, network
- Giám sát tài nguyên cloud

---

## Observability trên AWS

Sự kiện cũng trình bày cách Datadog tích hợp với AWS:

- Giám sát các dịch vụ như EC2, Lambda, RDS
- Theo dõi hệ thống serverless
- Hiển thị sơ đồ phụ thuộc giữa các service (Service Map)

Datadog có thể thu thập và liên kết dữ liệu từ nhiều dịch vụ AWS trong một nền tảng duy nhất.

---

## Dự án nhỏ

Do bị 1 số sự cố trong việc việc khởi động demo nên tôi không trải nghiệm được hết workshop

---

## Những điều rút ra

Thông qua sự kiện, tôi học được rằng:

- Observability là yếu tố quan trọng trong các hệ thống cloud hiện đại
- Việc giám sát cần bao phủ toàn bộ hệ thống, không chỉ một phần
- Datadog cung cấp nền tảng hợp nhất giúp theo dõi toàn diện
- Logs, metrics và traces cần được kết hợp để debug hiệu quả
- Giám sát thời gian thực giúp phát hiện và xử lý lỗi nhanh hơn

---

## Trải nghiệm cá nhân

Mặc dù tôi tham gia với vai trò người nghe, nhưng sự kiện đã mang lại nhiều kiến thức thực tế về cách giám sát hệ thống trong môi trường production.

Tôi hiểu rõ hơn cách các hệ thống lớn được theo dõi và vận hành, cũng như cách các công cụ như Datadog giúp đơn giản hóa quá trình debug.

Ngoài ra, sự kiện cũng giúp tôi có thêm định hướng trong việc xây dựng hệ thống và giao diện phù hợp với trải nghiệm người dùng.

Những kiến thức này rất hữu ích cho dự án hiện tại của tôi, đặc biệt khi làm việc với API và hệ thống cloud.

---

## Kết luận

Sự kiện đã cung cấp cái nhìn tổng quan về full-stack observability và cách triển khai trên AWS với Datadog.

Nó giúp tôi nâng cao hiểu biết về giám sát hệ thống và cách xây dựng các ứng dụng có khả năng mở rộng, ổn định và dễ theo dõi trên nền tảng cloud.

---

## Hình ảnh sự kiện

![datadogpic](/Datadog.jpg)
