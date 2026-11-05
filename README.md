# Portfolio CV - Hà Thị Kim Lệ

## Giới thiệu

Portfolio cá nhân giới thiệu Hà Thị Kim Lệ, Frontend Developer. Trang trình bày thông tin cá nhân, kỹ năng, một số dự án tiêu biểu và cách liên hệ. Giao diện được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày phần giới thiệu, vai trò nghề nghiệp và ảnh đại diện.
- Liệt kê kỹ năng và các dự án dưới dạng lưới thẻ.
- Cung cấp email và các liên kết mạng xã hội.
- Hỗ trợ bố cục nhiều kích thước màn hình và cuộn mượt đến từng phần.

Các thẻ dự án hiện là nội dung giới thiệu mẫu; một số liên kết chi tiết chưa được cấu hình.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện responsive, Flexbox, CSS Grid và các biến CSS.
- Python hoặc Nginx (tùy chọn): phục vụ tệp tĩnh khi chạy thử.
- Docker (tùy chọn): chạy Nginx trong container.

Trang hiện không cần JavaScript, framework frontend, trình biên dịch hay dịch vụ backend. JavaScript được nhắc trong danh sách kỹ năng trên trang, nhưng không được dùng để triển khai chức năng của website này.

## Yêu cầu môi trường

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để chạy bằng máy chủ cục bộ: Python 3.
- Để chạy bằng Docker: Docker Engine hoặc Docker Desktop đang hoạt động.
- Kết nối Internet nếu muốn tải ảnh dự án đang được tham chiếu từ các website bên ngoài. Ảnh đại diện nằm trong dự án tại `assets/img/avatar.jpg`.

Không cần cài gói phụ thuộc của dự án.

## Cài đặt

Lấy mã nguồn bằng cách tải và giải nén thư mục dự án, hoặc sao chép kho Git. Nếu dùng Git, thay `<URL_REPOSITORY>` bằng địa chỉ kho thực tế:

```bash
git clone <URL_REPOSITORY>
cd "KT A2.1"
```

Nếu đã có thư mục dự án trên máy, mở terminal tại thư mục chứa `index.html`.

### Windows

Mở PowerShell tại thư mục dự án. Cài Python 3 nếu máy chưa có; có thể kiểm tra bằng `py --version`. Không cần cài thêm thư viện.

### macOS

Mở Terminal tại thư mục dự án. Cài Python 3 nếu máy chưa có; có thể kiểm tra bằng `python3 --version`. Không cần cài thêm thư viện.

### Linux

Mở terminal tại thư mục dự án. Cài Python 3 bằng trình quản lý gói của bản phân phối nếu cần, rồi kiểm tra bằng `python3 --version`. Không cần cài thêm thư viện.

### Docker

Cài Docker Engine hoặc Docker Desktop và khởi động Docker. Không cần Dockerfile riêng: có thể phục vụ trực tiếp thư mục dự án bằng ảnh Nginx chính thức. Các lệnh chạy thử được trình bày bên dưới.

## Cấu hình

Dự án không có tệp cấu hình môi trường, biến môi trường hay backend cần thiết.

- Nội dung, tiêu đề, mô tả, thông tin liên hệ và các thẻ dự án: chỉnh trong `index.html`.
- Màu sắc, kiểu chữ và bố cục: chỉnh các biến CSS ở đầu `assets/css/styles.css` cùng các quy tắc liên quan.
- Ảnh đại diện: thay `assets/img/avatar.jpg` bằng ảnh khác và cập nhật đường dẫn trong `index.html` nếu đổi tên hoặc vị trí.
- Ảnh dự án hiện sử dụng URL bên ngoài; có thể thay bằng ảnh lưu trong `assets/img/` để không phụ thuộc kết nối Internet.

## Chạy thử

### Windows

Trong PowerShell, tại thư mục dự án:

```powershell
py -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Trong Terminal, tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Trong terminal, tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### Docker

Chạy các lệnh sau từ thư mục gốc của dự án. Lần đầu, Docker sẽ tải ảnh `nginx:alpine` nếu ảnh chưa có trên máy.

PowerShell trên Windows:

```powershell
docker run --rm --name portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

Terminal trên macOS hoặc Linux:

```bash
docker run --rm --name portfolio -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Truy cập <http://localhost:8080>. Dừng container bằng `Ctrl+C`. Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Kiểm tra nhanh

Sau khi mở trang, xác nhận rằng các mục điều hướng dẫn đến đúng phần, ảnh đại diện hiển thị, các thẻ kỹ năng và dự án được trình bày, và bố cục hoạt động trên cả màn hình nhỏ lẫn lớn. Các ảnh dự án được tải từ Internet nên có thể không hiển thị khi ngoại tuyến hoặc khi nguồn ảnh không còn khả dụng.

## Thông tin liên hệ

- Tác giả: Hà Thị Kim Lệ
- Email: [hale96226@gmail.com](mailto:hale96226@gmail.com)
- GitHub: `hale96226-jpg` (liên kết trên trang hiện chưa trỏ đến hồ sơ)
- Facebook: [facebook.com/kimle.05th3](https://facebook.com/kimle.05th3)
