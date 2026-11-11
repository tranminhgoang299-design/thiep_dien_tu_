# Thiệp điện tử Tri ân thầy cô – Trường THCS & THPT Đắk Mai

## Chạy thử
- Giải nén thư mục.
- Mở `index.html` bằng trình duyệt. Để thử ổn định, có thể dùng VS Code + Live Server.
- Cần Internet để tải font Google và thư viện tạo QR. Các chức năng chính, ảnh và thiệp PNG vẫn chạy cục bộ.

## Đã có
- Trang bìa, hiệu ứng cánh hoa, điều hướng và bố cục responsive.
- Sử dụng nguyên trạng 3 ảnh người dùng cung cấp: logo, ảnh khai giảng, ảnh kỷ niệm thầy trò.
- Lời tri ân xuất hiện khi cuộn đến.
- Thiệp tự điền, lời chúc mẫu, hiệu ứng lật và xuất PNG.
- Bảng lời chúc có trạng thái chờ duyệt, giao diện quản lý demo.
- Chọn tệp MP3 từ thiết bị, nút phát/tạm dừng và âm lượng.
- Tạo QR từ URL website công khai.

## Âm nhạc
Vì chưa có tệp MP3 được cung cấp, website không nhúng bản ghi “Bụi Phấn”. Người quản trị có thể nhấn `MP3 +` và chọn tệp MP3 có quyền sử dụng. Trình duyệt không tự phát nhạc khi chưa có thao tác của người dùng.

## Lưu ý quan trọng về dữ liệu
Bản này là website tĩnh hoàn chỉnh để chạy thử và triển khai nhanh. Lời chúc được lưu bằng `localStorage` trên chính trình duyệt/thiết bị gửi; không tự đồng bộ giữa các máy. Mã quản lý demo là `2011`, chỉ để trình diễn. **Không dùng mã này để bảo vệ dữ liệu thật** vì mã nằm trong mã nguồn phía trình duyệt. Muốn nhận lời chúc tập trung và kiểm duyệt an toàn, cần kết nối backend (ví dụ Supabase/Firebase), bật Row Level Security và chỉ cho quản trị viên có quyền duyệt/xóa.

## Đưa website lên Internet
### Cách 1 – Netlify Drop (nhanh)
1. Truy cập https://app.netlify.com/drop và đăng nhập.
2. Kéo thả cả thư mục `thiep-tri-an-dak-mai` (hoặc thư mục đã giải nén) vào trang.
3. Netlify cấp một URL dạng `https://....netlify.app`.
4. Mở URL đó trên điện thoại để kiểm tra. Dán URL vào mục “Tạo mã QR” ở cuối website.

### Cách 2 – GitHub Pages
1. Tạo repository GitHub mới và tải toàn bộ `index.html` cùng thư mục `assets/` lên.
2. Vào Settings → Pages → Deploy from a branch → chọn `main` và thư mục `/root`.
3. Chờ GitHub Pages xuất bản, sau đó dùng URL được cấp để tạo QR.

## Cấu trúc
- `index.html`: toàn bộ giao diện, CSS và JavaScript.
- `assets/logo-dak-mai.jpg`: logo trường gốc.
- `assets/khai-giang-2026-2027.jpg`: ảnh tập thể lễ khai giảng.
- `assets/ky-niem-thay-tro.jpg`: ảnh thầy trò trong lớp.

Giữ nguyên thư mục `assets` khi tải website lên hosting để ảnh hiển thị chính xác.
