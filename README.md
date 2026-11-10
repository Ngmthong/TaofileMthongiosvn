# Mthong iOSVN Web

## Thành phần
- `index.html`: website và công cụ xử lý UnityFS chạy phía trình duyệt.
- `manifest.webmanifest`: cấu hình cài website như ứng dụng (PWA).
- `sw.js`: cache tài nguyên cơ bản để hỗ trợ mở lại khi mạng chập chờn.
- `icon.svg`: biểu tượng website.

## Đưa website lên mạng bằng GitHub Pages
1. Tạo repository mới trên GitHub.
2. Tải toàn bộ các tệp trong thư mục này lên thư mục gốc repository.
3. Mở **Settings → Pages**.
4. Chọn **Deploy from a branch**, nhánh `main`, thư mục `/root`, rồi lưu.
5. Đợi GitHub cấp địa chỉ website. Mở bằng HTTPS để PWA/service worker hoạt động.

## Đưa lên hosting/VPS
- Tải toàn bộ tệp vào thư mục web root, ví dụ `/var/www/html/`.
- Cấu hình domain và HTTPS.
- Không cần cài Node.js, PHP hay database cho bản hiện tại.

## Lưu ý kỹ thuật
- Đây là bản web tĩnh; công cụ xử lý tệp chạy trong trình duyệt. Tệp người dùng chọn không được gửi lên server bởi logic hiện tại.
- Chưa có đăng nhập quản trị, database, đồng bộ dữ liệu, thanh toán hoặc quản lý sản phẩm từ xa. Những tính năng đó cần backend/API và cấu hình bảo mật riêng.
- Chỉ sử dụng với các tệp bạn có quyền chỉnh sửa và tuân thủ điều khoản của trò chơi/dịch vụ liên quan.
- Nên giữ bản sao lưu tệp gốc trước khi xử lý.
