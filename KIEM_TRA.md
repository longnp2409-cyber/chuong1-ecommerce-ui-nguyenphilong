# Kiểm tra

## Danh sách kiểm tra và trạng thái thực tế

| Hạng mục | Trạng thái thực tế | Người kiểm tra |
| --- | --- | --- |
| Có đủ `index.html`, `css/style.css`, 4 SVG và tài liệu | Đã kiểm tra tĩnh | Codex |
| HTML có `lang="vi"`, UTF-8 và viewport | Đã kiểm tra tĩnh | Codex |
| Có 4 sản phẩm, ảnh, tên, giá và liên kết thao tác | Đã kiểm tra tĩnh | Codex |
| Ảnh dùng đường dẫn tương đối đến file tồn tại | Đã kiểm tra tĩnh | Codex |
| Phép tính giảm giá khớp dữ liệu hiển thị | Đã kiểm tra tĩnh | Codex |
| Liên kết “Xem thông tin” và “Quay lại danh sách” trỏ đến `id` tồn tại | Đã kiểm tra tĩnh | Codex |
| CSS Grid, media query, `object-fit` và `focus-visible` | Đã kiểm tra tĩnh | Codex |
| Mở `index.html` bằng Chrome trên máy tính | Đã thực hiện | Sinh viên |
| Thử liên kết “Xem thông tin” và “Quay lại danh sách” | Đã thực hiện | Sinh viên |
| Bốn ảnh bìa hiển thị trong trình duyệt | Đã xác nhận hiển thị đủ và đúng | Sinh viên |
| 1440 × 900 trong Chrome DevTools | Đã quan sát 4 cột | Sinh viên |
| 768 × 1440 trong Chrome DevTools | Đã quan sát 2 cột | Sinh viên |
| 390 × 844 trong Chrome DevTools | Đã quan sát 1 cột | Sinh viên |
| Tab có focus dễ nhìn, Enter mở đúng thông tin | Đã kiểm tra và xác nhận | Sinh viên |
| Cuộn toàn trang ở 390/768/1440px | Không phát hiện tràn ngang trong lần kiểm tra | Sinh viên |
| Nội dung và ảnh ở ba kích thước | Không phát hiện lỗi bố cục; bốn ảnh bìa hiển thị đúng | Sinh viên |
| Chạy trang cải tiến trên iPhone thật/Safari | Chưa xác nhận; chỉ mô phỏng trong DevTools | — |

## Hướng dẫn tự kiểm tra

1. Mở `index.html` bằng Chrome trên máy tính.
2. Kiểm tra đủ 4 bìa, tên sách, tác giả, giá bán, giá gốc và nhãn giảm giá.
3. Bấm từng nút “Xem thông tin”, sau đó bấm “Quay lại danh sách”.
4. Mở DevTools, bật chế độ thiết bị và kiểm tra 1440 × 900, 768 × 1440 và 390 × 844.
5. Khi sửa mã tiếp, kiểm tra lại Tab/Enter, cuộn ngang, ảnh méo và nội dung chồng lấn. Kết quả lần kiểm tra đã hoàn tất được ghi trong bảng trên.
6. Nếu có điện thoại, mở file dự án bằng cách phù hợp với máy của bạn và quan sát ở chiều rộng nhỏ. Không ghi kết quả Safari/iPhone nếu chưa thực sự kiểm tra trên Safari/iPhone.

## Điểm sinh viên tự phát hiện và chỉnh sửa

Thầy yêu cầu sinh viên tự phát hiện và chỉnh ít nhất một điểm. Không cố tình tạo lỗi và không giả mạo việc đã sửa.

- Vấn đề quan sát được: chữ tác giả nhỏ, muốn tăng thêm 1 px để dễ đọc.
- File và thành phần liên quan: `css/style.css`, `.author`.
- Mã trước khi sửa: `font-size: 0.92rem;`
- Mã sau khi sửa: `font-size: calc(0.92rem + 1px);`
- Lý do thay đổi: tăng khả năng đọc. `font-size` quy định cỡ chữ; `calc` cho phép kết hợp `rem` và `px`. Cú pháp `font-size: (0.92rem + 1px);` từng được nhập thử là không hợp lệ và bị trình duyệt bỏ qua; ChatGPT đã chỉ ra lỗi và sinh viên sửa bằng `calc`.
- Kết quả kiểm tra lại: sinh viên xác nhận chữ tác giả sau sửa dễ đọc hơn; bốn bìa hiển thị đúng; Tab có viền focus, Enter mở đúng thông tin; cuộn toàn trang ở ba kích thước không phát hiện lỗi bố cục hoặc tràn ngang. Trang cải tiến trên Safari/iPhone thật chưa có kết quả kiểm tra.

### Đề xuất AI được tiếp thu

ChatGPT nhận xét phần giới thiệu và bìa sách chiếm nhiều chiều cao trước khi đến giá và nút. Sinh viên đồng ý và trực tiếp sửa CSS với hướng dẫn của AI:

- Trong `@media (max-width: 620px)`, `.site-header`: từ `padding: 3rem 0 2.4rem;` thành `padding: 1.75rem 0 1.5rem;`.
- `.cover-frame`: từ `min-height: 220px;` thành `min-height: 0; padding: 0.75rem;`.
- `.cover-frame img`: bổ sung `max-width: 140px;`, trong khi giá trị chung trước đó là `180px`.

Media query giới hạn thay đổi ở màn hình tối đa 620px; padding giảm khoảng trống, `min-height: 0` bỏ chiều cao tối thiểu và `max-width` giới hạn chiều rộng bìa trong khi vẫn giữ tỷ lệ ảnh.

## Lưu bản ban đầu

Sinh viên đã xác nhận lưu bản ban đầu trước khi sửa và giữ ảnh mã/giao diện để đối chiếu. Trong lượt tạo mã ban đầu chưa tạo repository; sau đó sinh viên đã tạo repository Public, upload bằng giao diện GitHub và triển khai Pages.

- Repository: https://github.com/longnp2409-cyber/chuong1-ecommerce-ui-nguyenphilong
- Pages: https://longnp2409-cyber.github.io/chuong1-ecommerce-ui-nguyenphilong/

Sinh viên đã mở website công khai, quan sát đủ bốn ảnh bìa và thử liên kết Xem thông tin/Quay lại danh sách. URL thêm dấu # là điều hướng trong cùng trang. Các kiểm tra kích thước và bàn phím nêu trên được sinh viên thực hiện ở bản chạy trên máy; không ghi thành kiểm thử tự động hoặc thử trên mọi thiết bị.

Sau khi upload ba tài liệu cập nhật, cần mở lại từng file trên GitHub để kiểm tra nội dung mới đã được lưu. Lượt cập nhật tài liệu không thay đổi HTML, CSS hoặc SVG.

