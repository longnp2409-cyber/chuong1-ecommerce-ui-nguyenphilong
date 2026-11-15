# AI Usage Log

## 1. Công cụ AI

- ChatGPT: hỗ trợ phân tích yêu cầu và chuẩn bị phương án theo thông tin sinh viên cung cấp.
- Codex: hỗ trợ tạo các file HTML, CSS, SVG và tài liệu trong lượt này.

## 2. Mục đích sử dụng

Tạo một giao diện HTML5/CSS3 minh họa cải tiến thẻ sách trong danh sách sách kinh tế, với cấu trúc dễ đọc, responsive và có thể mở trực tiếp bằng `index.html`.

## 3. Prompt đã sử dụng

Prompt dưới đây là nguyên văn yêu cầu sinh viên đã gửi trong lượt này:

> Bạn là trợ lý lập trình hướng dẫn sinh viên thực hành HTML5/CSS3. Hãy tạo dự án trực tiếp trong thư mục đang mở, theo phương án tôi đã lựa chọn dưới đây.
> 
> 1. BỐI CẢNH BÀI TẬP
> - Sinh viên: Nguyễn Phi Long.
> - MSSV: 87234020044.
> - Sinh viên năm cuối ngành Thương mại điện tử tại UEH.
> - Môn: Phát triển ứng dụng thương mại điện tử.
> - Giảng viên: TS. Nguyễn Mạnh Tuấn.
> - Bài tập cá nhân Chương 1.
> Website khảo sát:
> https://minhkhai.com.vn/store2/index.aspx
> 
> Tôi đã khảo sát năm khu vực: trang chủ, danh mục, chi tiết sản phẩm, tìm kiếm và giỏ hàng.
> 
> Nhận xét do tôi cung cấp:
> - Trong danh sách sách, tên và giá chưa nổi bật; mô tả dài khiến việc đọc lướt và so sánh khó hơn.
> - Trên ảnh chụp Safari iPhone, giao diện nhiều cột bị thu nhỏ, khiến chữ và thao tác khó đọc.
> - Trang chi tiết đã phân biệt giá gốc, giá bán và mức giảm.
> - Giỏ hàng cập nhật đúng: số lượng từ 1 lên 2, đơn giá 248.000 đồng, tổng tiền từ 248.000 lên 496.000 đồng.
> 
> Đây là dữ liệu khảo sát của tôi, không phải kết quả bạn tự kiểm thử. Không suy diễn website thiếu chức năng hoặc có lỗi khi chưa kiểm chứng.
> 
> 2. PHƯƠNG ÁN ĐÃ THỐNG NHẤT
> Tôi đã chọn cải tiến thẻ sách trong danh sách sách kinh tế bằng một trang HTML/CSS.
> 
> Mục tiêu:
> - Tên sách và giá dễ đọc.
> - Thông tin giữa các thẻ nhất quán, dễ so sánh.
> - Hình ảnh không méo.
> - Giao diện phù hợp máy tính và điện thoại.
> - Mã đơn giản để tôi hiểu và tự chỉnh sửa.
> 
> Hãy triển khai ngay phương án này, không cần yêu cầu tôi xác nhận lại.
> 
> 3. GIAO DIỆN
> - Tiêu đề chính: “Sách kinh tế dành cho người học”.
> - Có giới thiệu ngắn, khu vực 4 sản phẩm, phần mô tả chi tiết tương ứng và chân trang.
> - Nền sáng, chữ tối, xanh navy làm màu nhấn.
> - Bố cục thoáng nhưng không tạo khoảng trống quá lớn.
> - Không dùng banner lớn lấn át sản phẩm.
> - Không thêm hiệu ứng chuyển động không cần thiết.
> 
> Mỗi thẻ sách có:
> - Ảnh bìa.
> - Tên sách.
> - Tác giả.
> - Giá bán nổi bật.
> - Giá gốc và nhãn giảm giá nếu có; phép tính phải chính xác.
> - Liên kết dạng nút “Xem thông tin”, dẫn đến phần mô tả của sách đó trong cùng trang.
> 
> Không tạo nút mua hàng, giỏ hàng, tìm kiếm hoặc bộ lọc không hoạt động.
> 
> Bố cục:
> - Màn hình rộng: 4 cột.
> - Màn hình vừa: 2 cột.
> - Điện thoại nhỏ: 1 cột.
> - Chọn breakpoint hợp lý theo độ rộng nội dung.
> - Không tràn ngang; không thu nhỏ toàn trang để giả lập responsive.
> 
> Chân trang:
> “Nguyễn Phi Long · MSSV: 87234020044”
> “Bài thực hành môn Phát triển ứng dụng thương mại điện tử – UEH”
> “Giao diện minh họa phục vụ học tập, không phải website chính thức của Nhà sách Minh Khai.”
> 
> 4. DỮ LIỆU VÀ HÌNH ẢNH
> - Tạo 4 sách mẫu hư cấu thuộc các chủ đề kinh tế, quản trị, marketing và thương mại điện tử.
> - Dùng tên tác giả minh họa, không gán nội dung hư cấu cho người thật.
> - Ghi rõ trên trang: “Tên sách, tác giả và giá là dữ liệu minh họa.”
> - Tự tạo 4 ảnh bìa SVG đơn giản, có thiết kế khác nhau, lưu trong images/.
> - Không sao chép logo, ảnh bìa hoặc mã nguồn của Minh Khai/Fahasa.
> - Không tải tài nguyên trên Internet hoặc tạo đường dẫn ảnh không tồn tại.
> 
> 5. KỸ THUẬT VÀ CẤU TRÚC FILE
> Tạo:
> - index.html
> - css/style.css
> - images/ với 4 file SVG
> - README.md
> - AI_USAGE.md
> - KIEM_TRA.md
> 
> Chỉ HTML5 và CSS3.
> Không dùng JavaScript, framework, thư viện ngoài, npm, backend, cơ sở dữ liệu, đăng nhập hoặc thanh toán.
> 
> HTML:
> - Khai báo lang="vi", UTF-8 và viewport.
> - Có cấu trúc ngữ nghĩa: header, main, section, article, footer.
> - Một h1 chính; các tiêu đề phân cấp hợp lý.
> - Ảnh có alt phù hợp.
> - Liên kết đến đúng id tồn tại trên trang.
> - Có liên kết quay lại danh sách ở phần thông tin sách.
> 
> CSS:
> - Tách toàn bộ định dạng vào css/style.css.
> - Dùng CSS Grid cho danh sách.
> - Dùng phông chữ hệ thống hỗ trợ tiếng Việt.
> - Cỡ chữ và độ tương phản dễ đọc.
> - Vùng thao tác đủ rộng; hover và focus-visible rõ ràng.
> - Ảnh giữ đúng tỷ lệ, không méo.
> - Có chú thích ngắn bằng tiếng Việt ở các phần quan trọng.
> - Ưu tiên mã dễ hiểu, tránh thủ thuật phức tạp.
> 
> Dùng đường dẫn tương đối, hoạt động khi mở trực tiếp index.html và khi triển khai GitHub Pages.
> 
> Trước khi sửa, kiểm tra thư mục hiện tại. Không xóa hoặc ghi đè mất công việc có sẵn không liên quan.
> 
> 6. README.md
> Viết bằng tiếng Việt, tiêu đề “E-commerce UI Improvement”, gồm:
> 1. Giới thiệu.
> 2. Website tham khảo: tên, URL và năm khu vực khảo sát.
> 3. Chức năng thực tế của trang minh họa.
> 4. Công nghệ.
> 5. Cách chạy bằng index.html.
> 6. Cải tiến đã thực hiện và vấn đề tương ứng.
> 7. AI hỗ trợ và phần sinh viên tự kiểm tra, điều chỉnh.
> 
> Phân biệt rõ:
> - Minh Khai là website được khảo sát.
> - Sản phẩm này là giao diện minh họa độc lập.
> - Dữ liệu và bìa sách là minh họa tự tạo.
> 
> Chưa có URL GitHub/Pages thì ghi “Chưa triển khai”, không bịa đường dẫn.
> 
> 7. AI_USAGE.md
> Tiêu đề “AI Usage Log”, gồm:
> 1. Công cụ AI.
> 2. Mục đích sử dụng.
> 3. Prompt đã sử dụng.
> 4. Kết quả AI đề xuất và tạo ra.
> 5. Kiểm tra và điều chỉnh.
> 6. Phần sinh viên hiểu và có thể giải thích.
> 
> Ghi rõ:
> - ChatGPT hỗ trợ phân tích và chuẩn bị phương án theo thông tin tôi cung cấp.
> - Tôi đã lựa chọn phương án trước khi yêu cầu Codex tạo mã.
> - Codex hỗ trợ tạo file và giải thích mã trong lượt này.
> - Lưu nguyên prompt này trong mục prompt đã sử dụng.
> - Không tự dựng lại các prompt hoặc phản hồi của cuộc trò chuyện ChatGPT mà bạn không thấy.
> - Phân biệt kiểm tra do Codex thực hiện và kiểm tra do sinh viên thực hiện.
> - Phần sinh viên tự chỉnh sửa và xác nhận hiểu mã để chờ tôi bổ sung.
> - Không viết rằng tôi đã chạy thử, sửa mã hoặc hiểu các thành phần khi chưa có xác nhận.
> 
> 8. KIỂM TRA
> Nếu có môi trường trình duyệt, hãy chạy thử:
> - Trang mở được.
> - Đủ 4 sản phẩm với ảnh, tên, giá và thao tác.
> - Tài nguyên tải đúng.
> - Giá giảm khớp phép tính.
> - Liên kết Xem thông tin và quay lại hoạt động.
> - Bàn phím Tab có focus dễ nhìn.
> - Bố cục ở chiều rộng 1440, 768 và 390 px.
> - Không tràn ngang, ảnh không méo, nội dung không chồng lấn.
> 
> Chỉ ghi những kiểm tra thực sự đã làm.
> Nếu chỉ đọc mã thì ghi “kiểm tra tĩnh”.
> Không khẳng định đã thử Safari/iPhone nếu chưa thực hiện.
> 
> Tạo KIEM_TRA.md:
> - Danh sách kiểm tra và trạng thái thực tế.
> - Hướng dẫn tôi tự kiểm tra trên máy tính và điện thoại.
> - Mẫu ghi điểm tôi tự phát hiện:
>   + Vấn đề quan sát được.
>   + File và thành phần liên quan.
>   + Mã trước khi sửa.
>   + Mã sau khi sửa.
>   + Lý do thay đổi.
>   + Kết quả kiểm tra lại.
> 
> Thầy yêu cầu tôi tự phát hiện và chỉnh ít nhất một điểm.
> Không cố tình tạo lỗi, không giả mạo việc tôi đã sửa.
> Sau khi bàn giao phiên bản đầu, hướng dẫn tôi quan sát và lựa chọn một điểm thật sự cần cải thiện.
> 
> 9. BÀN GIAO
> - Tạo đầy đủ các file trực tiếp trong thư mục.
> - Chưa tạo repository, chưa commit hoặc push lên GitHub.
> - Không triển khai dịch vụ bên ngoài trong lượt này.
> - Liệt kê file đã tạo hoặc sửa.
> - Hướng dẫn mở index.html.
> - Giải thích ngắn vai trò của article, CSS Grid, media query, object-fit và focus-visible trong mã thực tế.
> - Nêu các kiểm tra đã thực hiện và các phần còn chờ tôi kiểm tra.
> - Hướng dẫn lưu bản ban đầu trước khi tôi chỉnh sửa để có thể đối chiếu.
> - Không cần chép lại toàn bộ mã trong câu trả lời nếu đã tạo đầy đủ file.
> 
> Chỉ hoàn thành phạm vi trên. Ưu tiên sản phẩm chạy được, dễ đọc, dễ sửa và giải thích được.

Lưu ý: prompt được lưu lại theo nội dung Codex nhận được; không tự dựng lại các prompt hoặc phản hồi khác của cuộc trò chuyện.

### Prompt cập nhật tài liệu đã sử dụng

> Hãy cập nhật README.md, AI_USAGE.md và KIEM_TRA.md trong dự án hiện tại theo tiến độ thực tế dưới đây. Chỉ chỉnh ba file tài liệu, không sửa HTML, CSS hoặc SVG. Chưa commit, push hoặc triển khai.
>
> 1. NHỮNG VIỆC TÔI ĐÃ THỰC HIỆN
> - Mở index.html bằng Chrome trên máy tính.
> - Thử liên kết “Xem thông tin” và “Quay lại danh sách”.
> - Kiểm tra giao diện bằng Chrome DevTools tại:
>   + 1440 × 900: danh sách hiển thị 4 cột.
>   + 768 × 1440: danh sách hiển thị 2 cột.
>   + 390 × 844: danh sách hiển thị 1 cột.
> - Đã lưu ảnh chụp giao diện và mã CSS chỉnh sửa.
> - Đây là mô phỏng kích thước màn hình trong DevTools, không phải kiểm tra trang cải tiến trên iPhone thật.
>
> 2. ĐIỂM TÔI TỰ PHÁT HIỆN VÀ ĐIỀU CHỈNH
> Tôi nhận thấy chữ tác giả nhỏ và muốn tăng thêm 1 px để dễ đọc.
> File: css/style.css.
> Thành phần: .author.
> Ban đầu: font-size: 0.92rem;
> Sau chỉnh sửa: font-size: calc(0.92rem + 1px);
> Trong quá trình sửa, tôi từng nhập thiếu calc:
> font-size: (0.92rem + 1px);
> ChatGPT đối chiếu ảnh mã nguồn và chỉ ra lỗi cú pháp; tôi đã sửa lại bằng calc.
> Giải thích: font-size quy định cỡ chữ; calc cho phép tính giá trị kết hợp rem và px. Cú pháp thiếu calc không hợp lệ và bị trình duyệt bỏ qua.
>
> 3. ĐỀ XUẤT CỦA AI ĐƯỢC TÔI TIẾP THU
> ChatGPT nhận xét phần giới thiệu và bìa sách chiếm nhiều chiều cao trước khi đến giá và nút. Tôi đồng ý và tự chỉnh CSS theo hướng dẫn.
> Trong @media (max-width: 620px):
> - .site-header: Trước padding: 3rem 0 2.4rem; Sau padding: 1.75rem 0 1.5rem;
> - .cover-frame: Trước min-height: 220px; Sau min-height: 0; padding: 0.75rem;
> - .cover-frame img: Bổ sung max-width: 140px; Giá trị max-width chung trước đó là 180px.
> Giải thích: media query giới hạn thay đổi ở màn hình rộng tối đa 620px; padding giảm khoảng trống bên trong; min-height: 0 bỏ chiều cao tối thiểu đã đặt; max-width giới hạn chiều rộng bìa; các quy tắc giữ tỷ lệ ảnh vẫn được giữ.
> Phân biệt rõ: chữ tác giả là vấn đề do tôi phát hiện; giảm chiều cao phần giới thiệu và bìa là đề xuất của AI được tôi tiếp thu. Tôi trực tiếp sửa mã với hướng dẫn của AI.
>
> 4. QUY TẮC GHI KẾT QUẢ
> - Đọc CSS hiện tại trước khi mô tả trạng thái mã; nếu khác thông tin trên, báo lại, không tự sửa mã.
> - Phân biệt kiểm tra tĩnh của Codex, thao tác tôi báo đã thực hiện và quan sát từ ảnh.
> - Chưa xác nhận kiểm tra Tab/focus, toàn bộ trang có tràn ngang hay không, hoặc chạy trang cải tiến trên Safari/iPhone thật: để “Chưa xác nhận”, không ghi đạt.
> - Không viết rằng tôi đã hiểu toàn bộ mã. Phần giải thích mã là nội dung để tôi ôn và tự đối chiếu.
> - Giữ nguyên prompt tạo mã đã lưu. Thêm nguyên prompt cập nhật tài liệu này vào nhật ký AI.
> - Không tự dựng lại các prompt ChatGPT khác chưa có trong cuộc trò chuyện Codex.
> - GitHub và GitHub Pages vẫn “Chưa triển khai”.
> - Sửa câu cuối KIEM_TRA.md để làm rõ: chưa tạo repository trong lượt tạo mã ban đầu; bài tập yêu cầu repository Public, GitHub Pages là tùy chọn.
> - Giữ README đủ 7 mục và AI_USAGE đủ 6 mục theo đề.
> - Điền phần tự chỉnh sửa bằng dữ liệu trên, không để mẫu dấu ba chấm cho những việc đã thực hiện.
>
> Sau khi cập nhật, tóm tắt những mục đã thay đổi và những việc còn chưa xác nhận.

## 4. Kết quả AI đề xuất và tạo ra

- Tạo `index.html` với cấu trúc ngữ nghĩa gồm header, main, section, article và footer.
- Tạo `css/style.css` với CSS Grid, media query, kiểu chữ hệ thống, trạng thái hover/focus-visible và bố cục không tràn ngang.
- Tạo 4 bìa SVG minh họa khác nhau trong `images/`.
- Tạo README và tài liệu kiểm tra để phân biệt website khảo sát với giao diện minh họa độc lập.

## 5. Kiểm tra và điều chỉnh

Codex đã thực hiện kiểm tra tĩnh CSS hiện tại trước khi cập nhật tài liệu và xác nhận các giá trị đang có khớp với thông tin sinh viên cung cấp: `.author` đã là `font-size: calc(0.92rem + 1px);`, cùng các thay đổi mobile trong `@media (max-width: 620px)`. Codex cũng đã kiểm tra tĩnh cấu trúc file, đường dẫn tương đối, các `href` với `id`, phép tính giảm giá và các yêu cầu HTML/CSS chính trong lượt tạo mã.

Sinh viên đã báo đã mở trang bằng Chrome, thử hai loại liên kết, kiểm tra 3 kích thước trong Chrome DevTools và lưu ảnh chụp giao diện cùng mã CSS chỉnh sửa. Đây là thao tác do sinh viên báo, không phải kiểm tra tĩnh của Codex; các kích thước là mô phỏng DevTools, không phải iPhone thật. Chưa xác nhận Tab/focus, toàn bộ trang có tràn ngang hay không, hoặc chạy trang cải tiến trên Safari/iPhone thật. Không viết rằng sinh viên đã hiểu toàn bộ mã; phần giải thích chỉ để sinh viên ôn và tự đối chiếu.

## 6. Phần sinh viên hiểu và có thể giải thích

Sinh viên đã tự phát hiện và chỉnh `.author` vì chữ tác giả nhỏ. Sinh viên cũng đã tiếp thu đề xuất AI về việc giảm chiều cao phần giới thiệu và bìa trên màn hình nhỏ, rồi trực tiếp sửa CSS với hướng dẫn của AI. Có thể dùng các giải thích về `font-size`, `calc`, `article`, CSS Grid, media query, `object-fit` và `focus-visible` để ôn và tự đối chiếu; tài liệu này không khẳng định sinh viên đã hiểu toàn bộ mã.
