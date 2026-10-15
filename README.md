# Mẫu báo cáo LaTeX ĐAMH

[![Xem PDF của bản phát hành mới nhất](preview.png)](https://github.com/Ex6TenZ13/mau-latex-damh/releases/latest/download/Quyen_DAMH.pdf)

Nhấn vào ảnh xem trước để tải PDF của bản phát hành mới nhất.

## Biên dịch

Tài liệu chính là `Quyen_ĐAMH.tex`. Dự án dùng TeX Live, `latexmk`,
`pdflatex` và BibTeX:

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error Quyen_ĐAMH.tex
```

GitHub Actions biên dịch tài liệu khi có thay đổi trên `main`, khi mở pull
request, hoặc khi đẩy tag bắt đầu bằng `v`. Với tag `v*`, workflow tạo GitHub
Release gồm PDF và gói mã nguồn lấy trực tiếp từ commit được gắn tag.

## Định dạng gói nguồn

Release dùng `mau-latex-damh-source.tar.gz` thay cho `.rar`. Công cụ RAR chính
thức chỉ được dùng miễn phí trong thời gian đánh giá 40 ngày; runner hiện không
có giấy phép thương mại. 7-Zip cũng không hỗ trợ tạo RAR, nên dự án không đổi tên
ZIP thành `.rar`. Nếu có giấy phép RAR hợp lệ, có thể bổ sung khóa giấy phép dưới
dạng GitHub Actions secret và thay bước `git archive` bằng RAR CLI đã đăng ký.

