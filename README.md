# LaTeX-ĐAMH

[![LaTeX PDF and release](https://github.com/Ex6TenZ13/LaTeX-DAMH/actions/workflows/latex.yml/badge.svg?branch=main)](https://github.com/Ex6TenZ13/LaTeX-DAMH/actions/workflows/latex.yml)

> 📣 **Mẫu LaTeX ĐAMH đang trong quá trình chỉnh sửa và hoàn thiện**
>
> Nội dung, cấu trúc và định dạng trong các tệp `.tex` có thể thay đổi; PDF và ảnh xem trước sẽ được cập nhật theo. Nếu đang sử dụng mẫu, hãy kiểm tra [bản phát hành mới nhất](https://github.com/Ex6TenZ13/LaTeX-DAMH/releases/latest) trước khi bắt đầu hoặc tiếp tục báo cáo.
>
> Có ý tưởng hoặc phát hiện lỗi? Hãy gửi góp ý tại [Issues](https://github.com/Ex6TenZ13/LaTeX-DAMH/issues). Vui lòng nêu tệp hoặc phần liên quan, đề xuất hoặc vấn đề, và ảnh minh họa nếu phù hợp.

[![Mở bản PDF](preview.png)](https://github.com/Ex6TenZ13/LaTeX-DAMH/blob/main/Quyen_DAMH.pdf)

Nhấn vào ảnh xem trước để mở PDF trực tiếp trên GitHub. Các bản PDF đã phát hành
có tại trang [Releases](https://github.com/Ex6TenZ13/LaTeX-DAMH/releases/latest).

## Tải và sử dụng gói ZIP

1. Tải [gói ZIP mã nguồn của bản phát hành mới nhất](https://github.com/Ex6TenZ13/LaTeX-DAMH/releases/latest/download/LaTeX-DAMH-source.zip) từ mục **Assets** trong trang Releases.
2. Giải nén ZIP vào một thư mục trên máy tính; không mở hoặc biên dịch tệp `.tex` trực tiếp bên trong ZIP. Giữ nguyên cấu trúc thư mục và các tệp đi kèm.
3. Mở TeXstudio, dùng **File → Open** để đi tới thư mục vừa giải nén và mở `Quyen_DAMH.tex`. TeXstudio sẽ hiển thị các tệp cùng thư mục trong **File Explorer**; chọn **Build & View** hoặc nhấn `F5` để biên dịch và xem PDF.

Gói ZIP chứa mã nguồn và tài nguyên của mẫu, không phải file PDF đã biên dịch. Nếu TeXstudio/MiKTeX hỏi cài package còn thiếu, hãy cho phép cài đặt rồi biên dịch lại.

## Cài đặt trên Windows

1. Cài [MiKTeX](https://miktex.org/download) bằng **Basic MiKTeX Installer**.
   Nên chọn cài cho người dùng hiện tại, đặt khổ giấy A4 và chọn **Always** hoặc
   **Ask me first** để MiKTeX cài các package còn thiếu. Sau khi cài, mở
   **MiKTeX Console**, chọn **Updates** và cập nhật toàn bộ package.
2. Cài [TeXstudio](https://texstudio.org/) bằng bản Windows Installer. Mở
   **Options → Configure TeXstudio → Build**, chọn **PdfLaTeX** làm trình biên
   dịch mặc định. Mở `Quyen_DAMH.tex`, sau đó dùng **Build & View** (`F5`).
3. Cài [SumatraPDF](https://www.sumatrapdfreader.org/download-free-pdf-viewer).
   Để dùng SumatraPDF thay trình xem tích hợp, vào **Options → Configure
   TeXstudio → Commands** và đặt lệnh External PDF Viewer:

   ```text
   "C:/Program Files/SumatraPDF/SumatraPDF.exe" -reuse-instance -forward-search "?c:am.tex" @ "?am.pdf"
   ```

   Trong SumatraPDF, nhấn `Ctrl+K`, chọn **Set Inverse Search Command Line** và
   nhập:

   ```text
   "C:\Program Files\TeXstudio\texstudio.exe" "%f" -line %l
   ```

Nếu TeXstudio báo thiếu package, mở MiKTeX Console để cập nhật hoặc cho phép
MiKTeX cài package tự động, rồi build lại.

## Gói nguồn của release

Mỗi release chứa `Quyen_DAMH.pdf` và `LaTeX-DAMH-source.zip`. File ZIP được tạo
trực tiếp từ commit của tag bằng `git archive`; README, thư mục `.git` và các file
build tạm không nằm trong gói.

