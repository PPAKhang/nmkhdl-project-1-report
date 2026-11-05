# Introduction to Data Science — arXiv Project

## Nhóm 18

Báo cáo đồ án môn Introduction to Data Science.

Đồ án tập trung xây dựng pipeline xử lý dữ liệu bài báo khoa học từ arXiv,
bao gồm thu thập dữ liệu, phân tích cấu trúc tài liệu và đối sánh tài liệu tham khảo.

## Các giai đoạn

1. Milestone 1 — Data Crawling
2. Milestone 2 — Hierarchical Parsing and Standardization
3. Milestone 3 — Reference Matching Pipeline

## Báo cáo tiến độ

Nội dung báo cáo được cập nhật theo tiến độ thực hiện đồ án.
Các số liệu thực nghiệm chưa được xác minh sẽ được đánh dấu PENDING.


File milestone-1/index.md
# Milestone 1 — Data Crawling

## 1. Giới thiệu

Milestone 1 tập trung xây dựng pipeline thu thập dữ liệu bài báo khoa học
từ arXiv và thông tin tài liệu tham khảo từ Semantic Scholar.

Pipeline gồm các giai đoạn:

1. Discovery — phát hiện và thu thập metadata bài báo.
2. Version Resolution — xác định các phiên bản của bài báo.
3. Source Crawling — tải source archive.
4. Source Extraction — trích xuất các file `.tex` và `.bib`.
5. Reference Crawling — thu thập metadata tài liệu tham khảo.
6. Storage and Validation — lưu trữ và kiểm tra dữ liệu.

## 2. Trạng thái thực hiện

- Cấu trúc pipeline: Đã có trong mã nguồn.
- Kiểm thử đơn vị: Đã có các test tương ứng.
- Crawl toàn bộ dữ liệu: PENDING.
- Semantic Scholar: PENDING.
- Benchmark đầy đủ: PENDING.

