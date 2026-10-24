# UTH Notifier

Lịch học Portal và deadline Moodle của sinh viên UTH, ngay trên desktop Windows.

**[Tải bản mới nhất](https://github.com/NguyenToan309/uth-notifier-releases/releases/latest/download/UTH_Notifier.exe)** · Windows 10/11 · Tự cập nhật

![Màn Hôm nay](docs/hom-nay.png)

## Tính năng

- **Hôm nay và Tuần**: buổi học theo giờ, phòng, giảng viên, buổi đang học và buổi kế tiếp.
- **Deadline**: nhóm theo mức khẩn, lọc theo môn, tìm theo tên bài.
- **Thông tin lớp**: giảng viên, liên hệ, nhóm Zalo, tỉ lệ điểm, lấy từ trang môn trên Moodle.
- **Chạy nền**: ẩn xuống khay hệ thống, tự đồng bộ mỗi 20 phút.
- **Tự cập nhật**: kiểm tra bản mới khi mở app, hoặc bấm *Kiểm tra cập nhật*.

## Bắt đầu

1. Tải `UTH_Notifier.exe` và đặt trong thư mục cá nhân (ví dụ `Documents`), không đặt trong `Program Files`.
2. Nếu Windows cảnh báo, chọn **More info → Run anyway**.
3. Bấm **Đăng nhập lại** trên banner:
   - Moodle: nhập tài khoản một lần.
   - Portal: tự đăng nhập và giải CAPTCHA, khoảng 30 ngày một lần.

## Bảo mật

- Mật khẩu và phiên đăng nhập được lưu trong Windows Credential Manager.
- App chỉ kết nối tới `portal.ut.edu.vn`, `courses.ut.edu.vn` và GitHub (để cập nhật, có kiểm tra SHA-256).
- App không thu thập dữ liệu. File log đã che mật khẩu, token, số điện thoại và email.

## Sự cố thường gặp

- **Hiện "Unhandled exception" ngay sau khi cập nhật từ bản 1.2.1 trở về trước**: đóng hộp thoại rồi mở lại app. Lỗi chỉ xảy ra một lần.
- **"Hết phiên đăng nhập"**: bấm **Đăng nhập lại**.

## Gỡ cài đặt

Thoát app từ khay hệ thống, xoá file `.exe` và thư mục `%APPDATA%\UTH Notifier`, sau đó xoá các mục `UTH_Notifier` trong Credential Manager.

---

Dự án cá nhân, không phải ứng dụng chính thức của nhà trường. Báo lỗi tại [Issues](https://github.com/NguyenToan309/uth-notifier-releases/issues).
