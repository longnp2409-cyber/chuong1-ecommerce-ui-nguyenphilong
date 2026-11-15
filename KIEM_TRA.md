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
| Tài nguyên tải đúng trong trình duyệt | Chưa xác nhận riêng | — |
| 1440 × 900 trong Chrome DevTools | Đã quan sát 4 cột | Sinh viên |
| 768 × 1440 trong Chrome DevTools | Đã quan sát 2 cột | Sinh viên |
| 390 × 844 trong Chrome DevTools | Đã quan sát 1 cột | Sinh viên |
| Tab có focus dễ nhìn | Chưa xác nhận | — |
| Toàn bộ trang không tràn ngang | Chưa xác nhận | — |
| Nội dung không chồng lấn và ảnh không méo | Chưa xác nhận đầy đủ | — |
| Chạy trang cải tiến trên iPhone thật/Safari | Chưa xác nhận; chỉ mô phỏng trong DevTools | — |

## Hướng dẫn tự kiểm tra

1. Mở `index.html` bằng Chrome trên máy tính.
2. Kiểm tra đủ 4 bìa, tên sách, tác giả, giá bán, giá gốc và nhãn giảm giá.
3. Bấm từng nút “Xem thông tin”, sau đó bấm “Quay lại danh sách”.
4. Mở DevTools, bật chế độ thiết bị và kiểm tra 1440 × 900, 768 × 1440 và 390 × 844.
5. Nếu chưa thực hiện, kiểm tra riêng bằng `Tab`, kiểm tra thanh cuộn ngang, ảnh méo và nội dung chồng lấn. Chỉ ghi “Đã đạt” sau khi thật sự quan sát.
6. Nếu có điện thoại, mở file dự án bằng cách phù hợp với máy của bạn và quan sát ở chiều rộng nhỏ. Không ghi kết quả Safari/iPhone nếu chưa thực sự kiểm tra trên Safari/iPhone.

## Mẫu ghi điểm tự phát hiện và chỉnh sửa

Thầy yêu cầu sinh viên tự phát hiện và chỉnh ít nhất một điểm. Không cố tình tạo lỗi và không giả mạo việc đã sửa.

- Vấn đề quan sát được: chữ tác giả nhỏ, muốn tăng thêm 1 px để dễ đọc.
- File và thành phần liên quan: `css/style.css`, `.author`.
- Mã trước khi sửa: `font-size: 0.92rem;`
- Mã sau khi sửa: `font-size: calc(0.92rem + 1px);`
- Lý do thay đổi: tăng khả năng đọc. `font-size` quy định cỡ chữ; `calc` cho phép kết hợp `rem` và `px`. Cú pháp `font-size: (0.92rem + 1px);` từng được nhập thử là không hợp lệ và bị trình duyệt bỏ qua; ChatGPT đã chỉ ra lỗi và sinh viên sửa bằng `calc`.
- Kết quả kiểm tra lại: sinh viên đã lưu ảnh chụp giao diện và mã CSS chỉnh sửa; việc kiểm tra Tab/focus, tràn ngang và Safari/iPhone thật vẫn chưa xác nhận.

### Đề xuất AI được tiếp thu

ChatGPT nhận xét phần giới thiệu và bìa sách chiếm nhiều chiều cao trước khi đến giá và nút. Sinh viên đồng ý và trực tiếp sửa CSS với hướng dẫn của AI:

- Trong `@media (max-width: 620px)`, `.site-header`: từ `padding: 3rem 0 2.4rem;` thành `padding: 1.75rem 0 1.5rem;`.
- `.cover-frame`: từ `min-height: 220px;` thành `min-height: 0; padding: 0.75rem;`.
- `.cover-frame img`: bổ sung `max-width: 140px;`, trong khi giá trị chung trước đó là `180px`.

Media query giới hạn thay đổi ở màn hình tối đa 620px; padding giảm khoảng trống, `min-height: 0` bỏ chiều cao tối thiểu và `max-width` giới hạn chiều rộng bìa trong khi vẫn giữ tỷ lệ ảnh.

## Lưu bản ban đầu

Trước khi tự chỉnh sửa, hãy sao chép nguyên thư mục dự án thành một thư mục như `Chuong1-ban-dau` hoặc nén lại thành một file ZIP. Giữ bản hiện tại làm mốc đối chiếu. Trong lượt tạo mã ban đầu chưa tạo repository; theo yêu cầu bài tập, repository cần để Public, còn GitHub Pages là tùy chọn. GitHub và GitHub Pages hiện vẫn: Chưa triển khai.
