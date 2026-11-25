# FPOSE — Kho Mẫu Ảnh & Trợ Lý Setup Chụp Hình

Bản triển khai website tĩnh từ `FPOSE V1.0.html`, sẵn sàng xuất bản miễn phí bằng GitHub Pages.

## Chạy thử trên máy

Mở `index.html` bằng trình duyệt hiện đại. Để có môi trường ổn định hơn, có thể chạy một static server tại thư mục này, ví dụ:

```bash
python -m http.server 8000
```

Sau đó truy cập `http://localhost:8000`.

## Xuất bản miễn phí bằng GitHub Pages

1. Đăng nhập hoặc tạo tài khoản tại https://github.com/.
2. Tạo repository mới, ví dụ `fpose`, và chọn **Public** nếu muốn công khai mã nguồn.
3. Upload `index.html`, `README.md` và `LICENSE` lên thư mục gốc repository.
4. Mở **Settings → Pages**.
5. Trong **Build and deployment**, chọn **Deploy from a branch**.
6. Chọn branch `main`, folder `/ (root)`, rồi nhấn **Save**.
7. Chờ GitHub Pages triển khai. Địa chỉ thường có dạng `https://TEN-GITHUB.github.io/fpose/`.

## Lưu ý kỹ thuật và quyền riêng tư

- Đây là website tĩnh, không có backend hoặc cơ sở dữ liệu máy chủ.
- Ảnh, thư viện mẫu và Shot List được lưu trong IndexedDB của trình duyệt hiện tại. Dữ liệu không tự đồng bộ giữa thiết bị hoặc trình duyệt. Dùng tính năng xuất/nhập JSON trong ứng dụng để chuyển dữ liệu.
- Gemini API Key được lưu trong LocalStorage của trình duyệt và được gửi trực tiếp từ trình duyệt đến Google Gemini API khi sử dụng tính năng AI. Không đưa API Key vào mã nguồn công khai, không chia sẻ hồ sơ trình duyệt có lưu khóa. Nếu triển khai cho nhiều người dùng, cân nhắc backend/proxy bảo vệ khóa.
- Trang hiện tải Tailwind CSS, exifr và Google Fonts từ các CDN/dịch vụ bên ngoài; cần kết nối Internet để tải các tài nguyên này.
- GitHub Pages cung cấp hosting tĩnh miễn phí, không cung cấp database/backend cho ứng dụng này.

## Giấy phép

Mã nguồn được chuẩn bị theo giấy phép MIT trong file `LICENSE`. Hãy thay `[COPYRIGHT HOLDER]` bằng tên cá nhân/tổ chức sở hữu bản quyền trước khi công bố. Chỉ công bố với giấy phép này nếu bạn có quyền cấp phép cho toàn bộ mã nguồn và tài nguyên đi kèm.
