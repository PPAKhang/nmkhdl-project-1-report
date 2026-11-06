# Introduction to Data Science — arXiv Project

Jupyter Book báo cáo đồ án arXiv của nhóm 18, thuộc học phần **Introduction to Data Science (Nhập môn Khoa học Dữ liệu)**.

Repository này quản lý nội dung báo cáo học thuật của đồ án dưới dạng Jupyter Book và công bố báo cáo thông qua GitHub Pages.

## 1. Tổng quan đồ án

Đồ án tập trung xây dựng một quy trình xử lý dữ liệu khoa học từ nguồn arXiv, bao gồm thu thập thông tin công bố, phân tích và chuẩn hóa nội dung bài báo, sau đó xây dựng quy trình đối sánh tài liệu tham khảo.

Đồ án được chia thành ba milestone:

- **Milestone 1 — Data Crawling:** Thu thập thông tin publication, các phiên bản bài báo, mã nguồn LaTeX và dữ liệu tài liệu tham khảo.
- **Milestone 2 — Hierarchical Parsing and Standardization:** Phân tích cấu trúc phân cấp của tài liệu LaTeX, xử lý nội dung nhiều tệp và nhiều phiên bản, chuẩn hóa dữ liệu và khử trùng lặp.
- **Milestone 3 — Reference Matching Pipeline:** Xây dựng quy trình đối sánh và liên kết các trích dẫn trong bài báo với những tài liệu tham khảo tương ứng.

Các milestone có quan hệ kế tiếp và sử dụng kết quả xử lý của giai đoạn trước làm đầu vào cho giai đoạn sau.

## 2. Các repository của đồ án

Đồ án sử dụng hai repository riêng biệt với mục đích khác nhau.

### 2.1. Repository mã nguồn

**GitHub:** [bingsu1103/nmkhdl-project-1](https://github.com/bingsu1103/nmkhdl-project-1)

Đây là repository mã nguồn chung của nhóm 18, chịu trách nhiệm quản lý:

- Source code triển khai các pipeline của ba milestone.
- Các module xử lý dữ liệu, cấu hình và giao diện dòng lệnh (CLI).
- Unit tests và integration tests.
- Data contracts, tài liệu kỹ thuật và kế hoạch phân công thành viên.
- Hướng dẫn cài đặt môi trường và thực thi chương trình.

Repository mã nguồn không lưu trữ corpus, dữ liệu Parquet, các tệp archive đã tải về, checkpoint hoặc thông tin xác thực nhạy cảm.

### 2.2. Repository báo cáo

Đây là repository Jupyter Book được sử dụng để xây dựng, quản lý và công bố báo cáo của đồ án.

Nội dung báo cáo bao gồm:

- Giải thích phương pháp và quy trình triển khai.
- Phân tích cấu trúc dữ liệu và cách thức xử lý.
- Thống kê, bảng biểu và biểu đồ đánh giá kết quả.
- Đánh giá hiệu năng, các hạn chế và kết luận của từng milestone.

Hai repository có chức năng độc lập nhưng bổ trợ cho nhau: repository mã nguồn cung cấp cơ sở triển khai và thực nghiệm, trong khi repository báo cáo trình bày phương pháp, phân tích và kết quả của đồ án.

## 3. Cấu trúc báo cáo

Jupyter Book được tổ chức theo từng milestone. Các milestone mới được bổ sung vào cùng một cuốn sách, không tạo repository báo cáo riêng.

Cấu trúc hiện tại:

```text
nmkhdl-project-1-report/
├── index.md
├── README.md
├── requirements.txt
├── _config.yml
├── _toc.yml
├── .github/
│   └── workflows/
│       └── deploy-book.yml
│
├── milestone-1/
│   ├── index.md
│   ├── methodology.md
│   ├── discovery.md
│   ├── source-crawling.md
│   ├── reference-crawling.md
│   ├── data-validation.md
│   ├── performance.md
│   └── limitations.md
│
├── milestone-2/
│   ├── index.md
│   ├── hierarchical-parsing.md
│   ├── standardization.md
│   ├── dataset-structure.md
│   ├── statistics.md
│   ├── performance.md
│   └── discussion.md
│
└── milestone-3/
    (Sẽ được bổ sung khi triển khai Milestone 3)
```

### 3.1. Milestone 1 — Data Crawling

Trình bày phương pháp và quy trình thu thập dữ liệu từ arXiv, bao gồm:

- Khám phá và thu thập metadata của publication.
- Tải và xử lý mã nguồn bài báo.
- Thu thập thông tin tài liệu tham khảo.
- Kiểm tra tính đầy đủ và hợp lệ của dữ liệu.
- Đánh giá hiệu năng và các hạn chế của quá trình crawling.

### 3.2. Milestone 2 — Hierarchical Parsing and Standardization

Trình bày quy trình phân tích và chuẩn hóa dữ liệu bài báo, bao gồm:

- Phân tích cấu trúc phân cấp của mã nguồn LaTeX.
- Xử lý compilation path và tài liệu LaTeX nhiều tệp.
- Xử lý tất cả phiên bản của mỗi publication.
- Làm sạch nội dung và chuẩn hóa biểu thức toán học.
- Khử trùng lặp các phần tử nội dung giữa các phiên bản.
- Trích xuất, chuẩn hóa và hợp nhất các mục tài liệu tham khảo BibTeX.
- Xây dựng cấu trúc ba bảng dữ liệu: `elements`, `hierarchy` và `bibtex`.
- Thống kê mức độ bao phủ, tỷ lệ parsing thành công và kết quả deduplication.
- Đánh giá thời gian chạy, mức sử dụng RAM và dung lượng lưu trữ đầu ra.

### 3.3. Milestone 3 — Reference Matching Pipeline

Phần báo cáo này sẽ được bổ sung khi nhóm triển khai milestone tiếp theo, dựa trên dữ liệu đã thu thập, phân tích và chuẩn hóa từ các giai đoạn trước.

## 4. Báo cáo trực tuyến

**🌐 Jupyter Book — GitHub Pages:**

[https://ppakhang.github.io/nmkhdl-project-1-report/](https://ppakhang.github.io/nmkhdl-project-1-report/)

Báo cáo được công bố dưới dạng website tĩnh, cho phép truy cập và điều hướng giữa các milestone.

## 5. Yêu cầu môi trường

Để biên dịch báo cáo trên máy tính cá nhân, cần chuẩn bị:

- Python tương thích với các phiên bản thư viện trong `requirements.txt`.
- pip để cài đặt các gói phụ thuộc.
- Jupyter Book và các thư viện cần thiết.

Danh sách dependencies được quản lý tập trung trong file `requirements.txt` của repository này.

Lưu ý: Môi trường chạy Jupyter Book của repository báo cáo được quản lý độc lập với môi trường chạy pipeline xử lý dữ liệu trong repository mã nguồn.

## 6. Hướng dẫn cài đặt và biên dịch Jupyter Book

Thực hiện các bước sau từ thư mục gốc của repository.

### 6.1. Tạo môi trường ảo

Trên Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Trên Linux/macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 6.2. Cài đặt dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 6.3. Biên dịch Jupyter Book

```bash
jupyter-book build .
```

Jupyter Book sẽ đọc cấu hình, mục lục và các trang Markdown để tạo website HTML.

### 6.4. Xem báo cáo trên máy tính cá nhân

Sau khi biên dịch thành công, kết quả được lưu trong:

```text
_build/html/
```

Mở file sau bằng trình duyệt:

```text
_build/html/index.html
```

Có thể sử dụng website local để kiểm tra nội dung, cấu trúc điều hướng, hình ảnh, bảng biểu và các liên kết trước khi công bố.

## 7. Nguyên tắc tổ chức dữ liệu và báo cáo

Để đảm bảo khả năng tái lập thực nghiệm và quản lý phiên bản, repository áp dụng các nguyên tắc sau:

- Chỉ quản lý các tệp nguồn của báo cáo, bao gồm Markdown, YAML, cấu hình và các tệp cần thiết để biên dịch Jupyter Book.
- Không commit corpus dữ liệu thực, các tệp LaTeX archive, dữ liệu Parquet, checkpoint, log thực nghiệm hoặc các dữ liệu trung gian có dung lượng lớn.
- Không commit API keys, credentials hoặc thông tin xác thực.
- Dữ liệu xử lý của Milestone 2 được nhóm lưu trữ làm đầu vào cho Milestone 3; không yêu cầu nộp corpus trong milestone này.
- Các thống kê, bảng và biểu đồ trong báo cáo cần được tạo từ dữ liệu và quy trình xử lý tương ứng khi biên dịch, thay vì sử dụng ảnh chụp màn hình tĩnh.
- Mỗi milestone được bổ sung vào cùng một Jupyter Book và được quản lý thông qua `_toc.yml`.

## 8. Cấu hình và triển khai GitHub Pages

Các tệp cấu hình chính:

- `_config.yml`: Cấu hình Jupyter Book.
- `_toc.yml`: Quản lý cấu trúc và thứ tự các chương, mục.
- `requirements.txt`: Danh sách dependencies.
- `.github/workflows/deploy-book.yml`: Workflow GitHub Actions phục vụ quá trình triển khai website.

Khi bổ sung nội dung cho milestone mới:

1. Tạo các trang Markdown trong thư mục milestone tương ứng.
2. Cập nhật `_toc.yml` để bổ sung các trang vào mục lục.
3. Biên dịch và kiểm tra Jupyter Book trên máy tính cá nhân.
4. Commit và push các thay đổi lên repository.
5. Kiểm tra trạng thái workflow GitHub Actions và website GitHub Pages sau khi triển khai.

Việc triển khai trực tuyến phụ thuộc vào cấu hình workflow và nhánh Git được thiết lập trong repository.

---

**Nhóm 18 — Introduction to Data Science**  
**arXiv Project Report**
