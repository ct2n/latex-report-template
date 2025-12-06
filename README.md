# Mẫu báo cáo LaTeX - Overleaf

## 1. Giới thiệu

Mẫu báo cáo LaTeX tiếng Việt hỗ trợ định dạng công thức và tô màu mã nguồn.

## 2. Yêu cầu và tương thích

Bắt buộc biên dịch bằng pdfLaTeX và kích hoạt sẵn chế độ shell-escape để sử dụng gói minted.

> Overleaf đã cấu hình sẵn các thiết lập này, có thể dùng trực tiếp.

## 3. Cấu trúc thư mục chính

- `main.tex`: tệp tổng hợp toàn bộ nội dung, quản lý các tệp chương và phụ lục thông qua `\input`.
- `config/` gồm:
  - `info.tex`: thông tin trình bày trên trang bìa.
  - `titlepage.tex`: bố cục trang bìa.
  - `packages.tex`: danh sách các gói được sử dụng,
  - `settings.tex`: cấu hình khổ giấy, lề, giãn dòng và đánh số,...
- `chapters/`: các chương nội dung chính.
- `appendix/`: phần phụ lục.
- `reference/references.bib`: danh mục tài liệu tham khảo.
- `images/`: thư mục chứa hình minh họa.

## 4. Tùy chỉnh thông tin

- Cập nhật thông tin trong `config/info.tex` (trường, tên đề tài, nhóm, giảng viên, sinh viên,...).
- Thay đổi bố cục trang bìa tại `config/titlepage.tex` nếu cần.
- Điều chỉnh lề, giãn dòng hoặc đánh số,... trong `config/settings.tex`.
- Bổ sung hay loại bỏ gói trong `config/packages.tex` (giữ minted nếu cần tô màu code).

## 5. Thêm và quản lý nội dung

- Chương chính: viết ở `chapters/*.tex`; thêm/bớt chương bằng cách chỉnh danh sách `\input` trong `main.tex`.
- Phụ lục được khai báo sau lệnh `\appendix` trong `main.tex`, nội dung trong `appendix/*.tex`.
- Hình ảnh: lưu vào `images/`, chèn với `\includegraphics`.
- Bảng/code: tham khảo ví dụ sẵn trong các file chương và phụ lục.

## 6. Tài liệu tham khảo

- Thêm mục BibTeX vào `reference/references.bib`.
- Trích dẫn trong nội dung bằng `\cite{key}`; danh mục tham khảo hiển thị tự động khi có trích dẫn.

## 7. Lưu ý khi không dùng Overleaf

- Bật `-shell-escape` cho pdfLaTeX để minted hoạt động.
- Giữ mã nguồn ở UTF-8; dùng babel tiếng Việt và fontenc T1 (đã cấu hình sẵn trong `config/packages.tex`).
- Nếu gặp lỗi minted: kiểm tra Python/Pygments trong hệ LaTeX hoặc tạm thời đổi sang môi trường code khác nếu không bật được shell-escape.
