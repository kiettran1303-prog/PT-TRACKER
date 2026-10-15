# Theo dõi tập luyện – app cho huấn luyện viên

Ứng dụng web chạy được như một app trên điện thoại (PWA): có icon riêng trên màn hình chính, mở toàn màn hình và dùng được khi không có mạng.

## Các file trong thư mục này

| File | Vai trò |
|---|---|
| `index.html` | Toàn bộ app |
| `manifest.webmanifest` | Khai báo tên, màu, icon để cài thành app |
| `sw.js` | Giúp app mở được khi không có mạng |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Icon app |
| `.nojekyll` | Báo GitHub Pages phục vụ file nguyên trạng |

## Bước 1. Đưa lên GitHub

1. Đăng nhập [github.com](https://github.com), bấm **New repository**.
2. Đặt tên, ví dụ `pt-tracker`. Chọn **Public** (GitHub Pages miễn phí yêu cầu repository công khai). Bấm **Create repository**.
3. Trong repository vừa tạo, bấm **uploading an existing file** (hoặc **Add file → Upload files**).
4. Giải nén file zip trước, rồi kéo **tất cả các file bên trong** vào trang upload (không kéo file `.zip`). Nhớ có cả file `.nojekyll`; nếu máy ẩn file bắt đầu bằng dấu chấm thì bỏ qua cũng được.
5. Bấm **Commit changes**.

> Dữ liệu khách hàng **không** nằm trên GitHub. Repository chỉ chứa mã của app. Toàn bộ dữ liệu chỉ lưu trong điện thoại của bạn. Đừng upload các file sao lưu `pt-backup-….json` lên GitHub.

## Bước 2. Bật GitHub Pages

1. Vào **Settings → Pages**.
2. Mục **Build and deployment → Source**: chọn **Deploy from a branch**.
3. Mục **Branch**: chọn `main`, thư mục `/ (root)`, bấm **Save**.
4. Đợi 1–2 phút, tải lại trang. Link app sẽ hiện ở đầu trang, dạng:
   `https://TEN-GITHUB-CUA-BAN.github.io/pt-tracker/`

## Bước 3. Cài thành app trên iPhone

1. Mở link trên bằng **Safari** (bắt buộc dùng Safari, không dùng Chrome).
2. Bấm nút **Chia sẻ** (hình vuông có mũi tên) → **Thêm vào Màn hình chính** → **Thêm**.
3. Từ giờ luôn mở app bằng **icon trên màn hình chính**.

Với Android: mở link bằng Chrome → menu ba chấm → **Cài đặt ứng dụng** (hoặc **Thêm vào màn hình chính**).

## Lưu ý quan trọng về dữ liệu

- **Chỉ nhập dữ liệu thật sau khi đã cài app và mở từ icon.** Dữ liệu trong Safari và trong app ở màn hình chính là hai nơi lưu tách biệt. Dữ liệu đã nhập trên Safari sẽ không tự xuất hiện trong app.
- **Sao lưu mỗi tuần:** vào app → **Sao lưu → Xuất file sao lưu** → chọn **Lưu vào Tệp** → chọn thư mục **Google Drive**. App sẽ nhắc nếu quá 7 ngày chưa sao lưu.
- **Đổi điện thoại hoặc cài lại app:** cài app như Bước 3, vào **Sao lưu → Khôi phục từ file sao lưu**, chọn file mới nhất trong Drive.
- Xóa app khỏi màn hình chính hoặc xóa dữ liệu trang web của Safari sẽ **mất dữ liệu chưa sao lưu**.

## Cập nhật app sau này

1. Trên GitHub, thay file `index.html` bằng bản mới (Add file → Upload files, tải đè cùng tên).
2. Mở file `sw.js`, đổi `pt-tracker-v1` thành `pt-tracker-v2` (lần sau `v3`, …), rồi Commit.
3. Trên điện thoại, đóng hẳn app rồi mở lại 2 lần để nhận bản mới. Dữ liệu của bạn được giữ nguyên.
