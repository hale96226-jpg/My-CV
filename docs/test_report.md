# BÁO CÁO KIỂM THỬ VÀ ĐÁNH GIÁ TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio CV - Hà Thị Kim Lệ |
| Phiên bản được đánh giá | v1.0.0 (theo `docs/RELEASENOTE.md`) |
| Ngày kiểm thử/đánh giá | 05/11/2026 |
| Người thực hiện/đánh giá | AI assistant — rà soát mã nguồn và kiểm tra hiển thị bằng Chrome |
| Phạm vi | `index.html`, `assets/css/styles.css` và tài liệu bàn giao hiện có |
| Môi trường kiểm thử | Google Chrome, trang mở cục bộ; viewport chụp: 390×844, 900×1100 và 1440×1000 |
| Loại đánh giá | Rà soát mã nguồn và kiểm tra hiển thị tại các viewport đã nêu; chưa kiểm thử trên thiết bị thật hoặc môi trường triển khai |

> **Lưu ý:** Báo cáo này không thay thế kiểm thử chấp nhận trên trình duyệt thực tế. Những hạng mục chưa có kết quả chạy thử cần được xác minh và cập nhật trước khi ký bàn giao.

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ phạm vi kiểm tra đã thực hiện; không đồng nghĩa đã kiểm thử trên mọi trình duyệt/thiết bị.
- **Chưa đạt:** Phát hiện lỗi hoặc nội dung chưa đáp ứng mong đợi cần được xử lý.
- **Cần cải thiện:** Chưa có đủ minh chứng, cần kiểm tra thêm hoặc nên hoàn thiện để giảm rủi ro bàn giao.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các mục nội dung chính hiện diện; có nhãn sai chính tả và một số liên kết dự án/liên hệ còn là mẫu hoặc chưa cấu hình. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Đã chụp ba viewport; ảnh mobile cần được xem xét thêm do phần nội dung/ảnh sát mép phải, đồng thời chưa kiểm tra khả năng tiếp cận và trình duyệt khác. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Trang tĩnh, không có backend; chưa chạy thử. Ảnh dự án phụ thuộc nguồn bên ngoài và chưa có đo lường hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy xử lý dữ liệu người dùng hoặc cấu hình bí mật trong phạm vi rà soát; cần xác minh URL bên ngoài và cấu hình triển khai. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có cấu trúc mã nguồn và tài liệu cơ bản; còn dấu nội dung tạm, thông tin chưa nhất quán và chưa có kết quả kiểm tra tự động. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã có ảnh minh chứng Responsive trong `docs/screenshots/`; chưa triển khai thử hoặc kiểm tra toàn bộ chức năng trên môi trường bàn giao. |

## 3. Nội dung chi tiết theo tiêu chí

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Các section tương ứng có trong `index.html`; điều hướng sử dụng các anchor `#about`, `#skills`, `#projects`, `#contact`. |
| Điều hướng đến đúng section | Cần cải thiện | Đích anchor có trong trang theo rà soát mã nguồn; chưa bấm kiểm tra trên trình duyệt. Nhãn “Giới thiụ” bị sai chính tả, cần sửa thành “Giới thiệu”. |
| Nút hành động dẫn đến khu vực phù hợp | Đạt | Các nút “Xem dự án” và “Liên hệ tôi” trỏ lần lượt đến `#projects` và `#contact`; chưa kiểm thử tương tác thực tế. |
| Thông tin liên hệ hoạt động và đúng hồ sơ | Chưa đạt | Email dùng liên kết `mailto:`; GitHub đang dùng `href="#"`; liên kết Facebook hiển thị `/in/` dù trỏ đến URL Facebook. Cần xác nhận và cập nhật URL/nhãn đúng trước bàn giao. |
| Liên kết “Xem chi tiết” của từng dự án | Chưa đạt | Một thẻ trỏ đến YouTube, các thẻ khác trỏ `#`; cần thay bằng URL dự án thật hoặc bỏ/đổi nhãn để không tạo kỳ vọng sai. |
| Nội dung giới thiệu và tiêu đề nhất quán | Chưa đạt | Tiêu đề trang có hậu tố `9999`, tiêu đề chính có `1111`; cần xác nhận và xóa nội dung thừa nếu không chủ đích. |
| Nội dung thẻ dự án phản ánh đúng sản phẩm | Cần cải thiện | Các thẻ mô tả Todo App và Weather Dashboard nhưng website hiện là trang tĩnh HTML/CSS; cần ghi rõ đây là dự án giới thiệu/mẫu hoặc cung cấp liên kết chứng minh. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

#### Minh chứng kiểm thử Responsive

| Viewport | Kích thước ảnh | Minh chứng |
|---|---:|---|
| Mobile | 390×844 | [responsive-mobile.png](./screenshots/responsive-mobile.png) |
| Tablet | 900×1100 | [responsive-tablet.png](./screenshots/responsive-tablet.png) |
| Desktop | 1440×1000 | [responsive-desktop.png](./screenshots/responsive-desktop.png) |

Ảnh được chụp từ trang hiện tại bằng Chrome. Đây là ảnh viewport, không phải ảnh chụp thiết bị vật lý; kết quả không thay thế kiểm thử trên thiết bị hoặc trình duyệt khác.

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bố cục thích ứng theo kích thước màn hình | Cần cải thiện | Đã chụp ba kích thước ở trên. Mã CSS khai báo breakpoint 768px và 1280px; ảnh tablet/desktop thể hiện lần lượt lưới dự án 2/3 cột. Ảnh mobile cho thấy nội dung phần giới thiệu/ảnh đại diện sát hoặc bị cắt ở mép phải; cần xác minh và xử lý trước khi đánh dấu Đạt. |
| Điều hướng, cuộn trang và trạng thái focus | Cần cải thiện | Có `scroll-behavior: smooth` và trạng thái `:focus-visible` cho liên kết menu; cần kiểm tra bằng bàn phím, đặc biệt với các liên kết dự án và liên hệ. |
| Ảnh đại diện hiển thị | Đạt | Ảnh đại diện tải và xuất hiện trong các ảnh minh chứng ở ba viewport. |
| Ảnh dự án và nội dung thay thế | Cần cải thiện | Ảnh dự án dùng URL bên ngoài; đã có alt text trong HTML nhưng việc tải ảnh và mức độ phù hợp của ảnh chưa được xác minh. |
| Độ tương phản và khả năng đọc | Cần cải thiện | Cần đo tương phản màu thực tế và kiểm tra cỡ chữ. Một số màu nền/chữ được khai báo trực tiếp trong CSS; chưa có đánh giá theo WCAG. |
| Chính tả, ngôn ngữ và tính nhất quán nội dung | Chưa đạt | Phát hiện nhãn “Giới thiụ”, hậu tố số ở tiêu đề và nhãn Facebook `/in/`; cần rà soát nội dung tiếng Việt toàn trang. |
| Tương thích Chrome, Firefox, Edge, Safari | Cần cải thiện | Chưa có kết quả kiểm tra trên các trình duyệt hoặc phiên bản cụ thể. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Trang tải bằng máy chủ tĩnh | Cần cải thiện | README hướng dẫn chạy bằng Python HTTP server hoặc Nginx; chưa khởi chạy và xác nhận phản hồi HTTP. |
| Tài nguyên nội bộ tải đúng | Cần cải thiện | CSS và ảnh đại diện dùng đường dẫn tương đối trong dự án; chưa kiểm tra mã phản hồi hoặc lỗi 404 khi triển khai. |
| Ứng xử khi mất kết nối Internet | Cần cải thiện | Các ảnh dự án lấy từ bên ngoài nên có thể không hiển thị ngoại tuyến hoặc khi nguồn thay đổi; cần chấp nhận rõ ràng hoặc lưu ảnh trong repository. |
| Xử lý lỗi và thông báo cho người dùng | Đạt | Trong phạm vi rà soát, đây là trang giới thiệu tĩnh, không có luồng nhập liệu, API hay thao tác ứng dụng cần thông báo lỗi. |
| Tốc độ tải và hiệu năng cơ bản | Cần cải thiện | Chưa đo thời gian tải, kích thước ảnh, chỉ số Lighthouse/Core Web Vitals hoặc hiệu năng mạng chậm. |
| Hoạt động khi tải trực tiếp và khi phục vụ qua HTTP | Cần cải thiện | Chưa chạy thử cả hai cách; ưu tiên xác minh theo hướng dẫn máy chủ tĩnh trong README. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Thu thập, lưu trữ hoặc truyền dữ liệu người dùng | Đạt | Không thấy biểu mẫu, backend, cookie hoặc luồng lưu dữ liệu người dùng trong trang tĩnh được rà soát. |
| Bí mật và cấu hình môi trường | Đạt | README nêu dự án không cần biến môi trường hay backend; không thấy thông tin xác thực trong phạm vi các tệp được kiểm tra. |
| Tài nguyên và liên kết bên thứ ba | Cần cải thiện | Ảnh dự án và một liên kết ngoài sử dụng tên miền bên ngoài; cần xác minh nguồn, quyền sử dụng, tính cần thiết và hành vi khi nguồn không khả dụng. |
| Cấu hình HTTPS và máy chủ khi triển khai | Cần cải thiện | Chưa có cấu hình môi trường triển khai để đánh giá HTTPS, header bảo mật, quyền truy cập hoặc cấu hình máy chủ. |
| Bề mặt tấn công phía client | Đạt | Không thấy mã JavaScript thực thi hoặc xử lý dữ liệu nhập trong phạm vi trang hiện tại; đánh giá này chỉ áp dụng cho mã đã rà soát, không phải kiểm thử xâm nhập. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu trúc tệp và phân tách HTML/CSS | Đạt | Có `index.html`, stylesheet riêng tại `assets/css/styles.css`, ảnh tại `assets/img/` và tài liệu trong `docs/`. |
| Tính ngữ nghĩa và metadata HTML | Cần cải thiện | Có `lang="vi"`, charset, viewport, description, cấu trúc header/nav/main/section/footer và alt text; cần kiểm tra HTML validator và sửa nội dung chưa nhất quán. |
| Tính dễ bảo trì của CSS | Cần cải thiện | CSS có custom properties, quy tắc bố cục và breakpoint; chưa chạy lint/format và chưa đánh giá các quy tắc không còn sử dụng. |
| Tài liệu hướng dẫn sử dụng và chạy thử | Đạt | README nêu công nghệ, yêu cầu môi trường, hướng dẫn chạy bằng Python và Docker/Nginx; các lệnh chưa được thực thi để xác nhận. |
| Release note và lịch sử thay đổi | Đạt | Có `docs/RELEASENOTE.md` ghi phiên bản v1.0.0 và `docs/AI_LOG.md` ghi thay đổi lớn. |
| Tính đầy đủ và chính xác của tài liệu | Cần cải thiện | README/Release Notes đã nêu một số giới hạn về liên kết; cần đồng bộ lại sau khi hoàn thiện link, nội dung liên hệ và kết quả kiểm thử. |
| Tính sạch của nội dung trước phát hành | Chưa đạt | Các chuỗi `9999`, `1111`, nhãn sai chính tả và link mẫu cần được rà soát/xác nhận trước khi bàn giao. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn triển khai/chạy cục bộ | Đạt | README có lệnh Python HTTP server và Docker với Nginx; chưa chạy xác minh trên máy sạch. |
| Có thể triển khai như website tĩnh | Cần cải thiện | Cấu trúc không yêu cầu build hay backend theo README; cần thử triển khai vào đích bàn giao thực tế và xác nhận đường dẫn tài nguyên. |
| Có kế hoạch kiểm thử trước bàn giao | Cần cải thiện | Báo cáo có checklist và kết quả kiểm tra hiển thị Responsive; chưa có kết quả pass/fail đầy đủ cho các chức năng, trình duyệt khác hoặc nghiệm thu người dùng. |
| Kiểm tra liên kết và tài nguyên | Cần cải thiện | Chưa chạy link checker hoặc kiểm tra mạng; các URL mẫu đã nhận diện trong mục 3.1. |
| Minh chứng ảnh chụp và kết quả chạy | Cần cải thiện | Đã bổ sung ảnh Responsive tại `docs/screenshots/` và liên kết ở mục 3.2; cần bổ sung ảnh các khu vực còn lại cùng kết quả kiểm thử chức năng/triển khai. |
| Bàn giao gói mã nguồn và hướng dẫn tái lập | Cần cải thiện | README có hướng dẫn cơ bản; cần xác nhận bản bàn giao chứa đủ `index.html`, `assets/` và `docs/`, đồng thời thử theo đúng hướng dẫn. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm đã có nền tảng portfolio tĩnh với các khu vực nội dung chính, stylesheet tách riêng, bố cục responsive được khai báo và tài liệu hướng dẫn chạy. Đã kiểm tra hiển thị bằng Chrome và lưu ảnh tại ba viewport; ảnh mobile cho thấy nội dung sát hoặc bị cắt ở mép phải, cần xác minh và xử lý. Chưa có kiểm thử chức năng đầy đủ, kiểm thử trên thiết bị thật hoặc xác minh môi trường triển khai mục tiêu.

**Kết luận: Chưa nên xác nhận bàn giao cuối cùng** cho đến khi xử lý các nội dung chưa đạt và hoàn thành kiểm thử thực tế. Có thể xem đây là bản ứng viên bàn giao sau khi các đề xuất dưới đây được thực hiện và xác minh.

### Vấn đề cần ưu tiên khắc phục

1. Xóa hoặc xác nhận các hậu tố `9999` và `1111` trong tiêu đề; sửa “Giới thiụ” thành “Giới thiệu”.
2. Thay các liên kết `href="#"` và URL YouTube không tương ứng bằng địa chỉ hồ sơ/dự án chính xác; sửa nhãn liên kết Facebook để khớp URL.
3. Rà soát tính xác thực của nội dung dự án, ảnh minh họa, quyền sử dụng ảnh và nội dung mẫu.
4. Kiểm tra hiển thị ở các kích thước màn hình và trình duyệt mục tiêu; kiểm tra điều hướng bằng bàn phím, khả năng đọc và tương phản màu.
5. Chạy trang theo hướng dẫn trong README, xác nhận ảnh/CSS tải thành công, kiểm tra các liên kết ngoài và ghi lại lỗi phát sinh.
6. Ghi lại môi trường, kết quả kiểm thử, ảnh chụp màn hình và thông tin người nghiệm thu vào báo cáo trước khi phát hành.

### Điều kiện đề xuất để đóng kiểm thử

- Các hạng mục **Chưa đạt** đã được sửa hoặc có quyết định chấp nhận ngoại lệ được ghi nhận.
- Các mục **Cần cải thiện** liên quan đến chức năng, giao diện và triển khai đã được kiểm tra trên môi trường mục tiêu.
- Có minh chứng chạy trang và ảnh chụp các giao diện chính; cập nhật trạng thái và ghi rõ trình duyệt/thiết bị đã dùng.
- README, Release Notes và AI Log phản ánh đúng trạng thái cuối cùng của sản phẩm.