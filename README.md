# E-commerce UI Improvement

## 1. Giới thiệu

Đây là bài tập cá nhân Chương 1 của Nguyễn Phi Long (MSSV: 87234020044), sinh viên năm cuối ngành Thương mại điện tử tại UEH, môn Phát triển ứng dụng thương mại điện tử, giảng viên TS. Nguyễn Mạnh Tuấn.

Sản phẩm là một giao diện minh họa độc lập cho danh sách sách kinh tế. Minh Khai là website được khảo sát; sản phẩm này không phải website chính thức của Minh Khai và không sao chép logo, bìa sách hay mã nguồn của Minh Khai/Fahasa.

## 2. Website tham khảo

- Tên: Nhà sách Minh Khai
- URL: https://minhkhai.com.vn/store2/index.aspx
- Năm khu vực khảo sát: trang chủ, danh mục, chi tiết sản phẩm, tìm kiếm và giỏ hàng.
- Nhận xét khảo sát do sinh viên cung cấp: tên và giá trong danh sách chưa nổi bật; mô tả dài làm khó đọc lướt và so sánh; giao diện nhiều cột trên ảnh chụp Safari iPhone bị thu nhỏ; trang chi tiết phân biệt giá gốc, giá bán và mức giảm; giỏ hàng cập nhật số lượng và tổng tiền đúng theo dữ liệu khảo sát.

## 3. Chức năng thực tế của trang minh họa

- Hiển thị 4 thẻ sách mẫu với ảnh bìa SVG, tên, tác giả, giá bán, giá gốc và nhãn giảm giá.
- Liên kết “Xem thông tin” nhảy đến phần mô tả tương ứng; mỗi phần có liên kết quay lại danh sách.
- Bố cục responsive 4 cột trên màn hình rộng, 2 cột ở màn hình vừa và 1 cột trên điện thoại nhỏ.
- Không có mua hàng, giỏ hàng, tìm kiếm hay bộ lọc vì đây không phải chức năng được yêu cầu.
- Tên sách, tác giả, giá và bìa là dữ liệu minh họa tự tạo.

## 4. Công nghệ

Chỉ sử dụng HTML5, CSS3 và 4 ảnh SVG tự tạo. Không dùng JavaScript, framework, thư viện ngoài, npm, backend, cơ sở dữ liệu, đăng nhập hoặc thanh toán.

## 5. Cách chạy bằng index.html

Mở trực tiếp file `index.html` bằng Chrome trên máy tính. Sinh viên đã dùng Chrome DevTools để mô phỏng các kích thước 1440 × 900, 768 × 1440 và 390 × 844.

Các đường dẫn tương đối đến `css/style.css` và thư mục `images/` được giữ để hoạt động khi mở file trực tiếp hoặc khi triển khai GitHub Pages.

GitHub/Pages: Chưa triển khai.

## 6. Cải tiến đã thực hiện và vấn đề tương ứng

- Tên sách và giá được tách thành các vùng rõ ràng, giúp đọc nhanh hơn.
- Các thẻ dùng cùng một cấu trúc, giúp so sánh thông tin dễ hơn.
- Giá gốc, giá bán và phần trăm giảm được trình bày cạnh nhau; phép tính sử dụng các cặp giá chính xác: 320.000 → 248.000 (-22,5%), 420.000 → 315.000 (-25%), 280.000 → 224.000 (-20%), 360.000 → 270.000 (-25%).
- CSS Grid và media query giúp nội dung chuyển từ 4 cột sang 2 cột rồi 1 cột, thay vì thu nhỏ toàn trang. Sinh viên đã quan sát đúng 4 cột ở 1440 × 900, 2 cột ở 768 × 1440 và 1 cột ở 390 × 844 trong Chrome DevTools.
- `object-fit: contain` giữ tỷ lệ ảnh bìa và không làm méo hình.
- Sinh viên tự phát hiện chữ tác giả nhỏ và đã chỉnh `.author` trong `css/style.css` từ `font-size: 0.92rem;` thành `font-size: calc(0.92rem + 1px);`. Trong lúc sửa, sinh viên từng nhập thiếu `calc`; ChatGPT đối chiếu mã nguồn và chỉ ra lỗi cú pháp, sau đó sinh viên sửa lại.
- Theo đề xuất của AI, sinh viên đã tự chỉnh CSS mobile để phần giới thiệu và bìa chiếm ít chiều cao hơn: trong `@media (max-width: 620px)`, `.site-header` dùng `padding: 1.75rem 0 1.5rem`, `.cover-frame` dùng `min-height: 0; padding: 0.75rem`, và `.cover-frame img` bổ sung `max-width: 140px`.
- Không dùng banner lớn hoặc hiệu ứng chuyển động không cần thiết.

## 7. AI hỗ trợ và phần sinh viên tự kiểm tra, điều chỉnh

ChatGPT hỗ trợ phân tích và chuẩn bị phương án theo thông tin sinh viên cung cấp. Sinh viên đã lựa chọn phương án cải tiến thẻ sách trước khi yêu cầu Codex tạo mã. Codex hỗ trợ tạo file và giải thích mã trong lượt tạo mã. Sau đó, ChatGPT tiếp tục góp ý về chiều cao phần giới thiệu và bìa; sinh viên đã tiếp thu và trực tiếp sửa CSS với hướng dẫn của AI.

Codex đã thực hiện kiểm tra tĩnh cấu trúc file, đường dẫn tương đối, liên kết `id`, dữ liệu giảm giá và nội dung HTML/CSS. Sinh viên đã mở trang bằng Chrome trên máy tính, thử hai loại liên kết và kiểm tra ba kích thước bằng Chrome DevTools. Đây là mô phỏng kích thước màn hình, không phải kiểm tra trên iPhone thật. Chưa xác nhận kiểm tra Tab/focus, toàn bộ trang có tràn ngang hay không hoặc chạy trang cải tiến trên Safari/iPhone thật. Phần giải thích mã là nội dung để sinh viên ôn và tự đối chiếu; không khẳng định sinh viên đã hiểu toàn bộ mã.
