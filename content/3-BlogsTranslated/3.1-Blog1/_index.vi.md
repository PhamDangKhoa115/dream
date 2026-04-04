---
title: "Blog 1"
date: 2026-04-01
weight: 2
chapter: false
pre: " <b> 3.1. </b> "
---

# Thiết kế hệ thống hỗ trợ phát triển Agentic AI trên AWS

Bài viết này tập trung vào cách thiết kế kiến trúc hệ thống trên AWS để hỗ trợ **Agentic AI**, nơi AI không chỉ gợi ý code mà còn có thể tự viết, test và cải thiện code thông qua các vòng lặp phản hồi liên tục.

Trong các hệ thống truyền thống, kiến trúc chủ yếu phục vụ cho lập trình viên, dẫn đến việc quá trình triển khai và kiểm thử diễn ra chậm. Điều này khiến AI khó có thể hoạt động hiệu quả do phải chờ đợi lâu để xác nhận kết quả.

---

## Vấn đề của kiến trúc truyền thống

Các hệ thống hiện tại gặp một số hạn chế khi áp dụng AI:

- Chu kỳ deploy và test quá chậm
- Các service bị phụ thuộc chặt chẽ (tight coupling)
- Khó test nếu không deploy lên cloud
- Code khó hiểu đối với AI

Điều này khiến AI không thể hoạt động tự động hoàn toàn

---

## Kiến trúc hỗ trợ phản hồi nhanh

Để AI hoạt động hiệu quả, hệ thống cần tối ưu cho **feedback nhanh**.

### 1. Giả lập cục bộ (Local Emulation)

- Sử dụng AWS SAM để chạy Lambda và API Gateway locally
- Chạy container tương tự ECS/Fargate
- Dùng DynamoDB Local để test database

Giảm thời gian test từ vài phút xuống vài giây

---

### 2. Phát triển offline

Đối với hệ thống xử lý dữ liệu:

- Test logic bằng dữ liệu mẫu
- Sử dụng môi trường local như AWS Glue

Giảm chi phí và thời gian sử dụng cloud

---

### 3. Kiểm thử kết hợp (Hybrid Testing)

- Một số service AWS không thể chạy local
- Sử dụng môi trường cloud nhỏ gọn

Dùng CloudFormation hoặc CDK để deploy nhanh

---

### 4. Preview Environment

- Tạo môi trường test tạm thời
- Kiểm thử toàn hệ thống
- Xóa sau khi hoàn thành

Giảm rủi ro khi deploy production

---

## Thiết kế code thân thiện với AI

Không chỉ kiến trúc, code cũng cần rõ ràng để AI hiểu.

### Domain-Driven Design

Chia code thành các layer:

- `/domain` → logic nghiệp vụ
- `/application` → xử lý luồng
- `/infrastructure` → AWS services

Giúp AI dễ đọc và chỉnh sửa

---

### Test như specification

- Unit test → kiểm tra logic
- Contract test → đảm bảo API
- Smoke test → kiểm tra hệ thống  
  Test đóng vai trò như “hướng dẫn” cho AI

---

### Tài liệu cho AI

- AGENT.md
- RUNBOOK.md
- File cấu hình (YAML)

Giúp AI hiểu hệ thống tốt hơn

---

## CI/CD và kiểm soát

- Áp dụng pipeline CI/CD
- Bắt buộc chạy test
- Review code

Đảm bảo an toàn khi dùng AI

---

## Kết luận

Để tận dụng tối đa AI trong phát triển phần mềm, hệ thống cần:

- Feedback nhanh
- Kiến trúc rõ ràng
- Code dễ hiểu

Khi đó, AI sẽ trở thành công cụ mạnh giúp tăng tốc phát triển thay vì gây cản trở.
