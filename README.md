<p align="center"><img src="docs/logo.png" width="112" alt="UTH Notifier"></p>

<h1 align="center">UTH Notifier</h1>

<p align="center">Lịch học, deadline và nhắc nhở cho sinh viên UTH, ngay trên máy tính Windows.</p>

<p align="center">
  <b><a href="https://github.com/NguyenToan309/uth-notifier-releases/releases/latest/download/UTH_Notifier.exe">⬇ Tải UTH_Notifier.exe</a></b>
  · Windows 10/11 · Miễn phí · Tự cập nhật
</p>

![Màn Hôm nay](docs/hom-nay.png)

## App làm được gì

- **Lịch học**: xem hôm nay hoặc bất kỳ tuần nào, kể cả tuần đã qua và tuần sắp tới. Mỗi buổi có giờ, phòng và giảng viên.
- **Deadline Moodle**: xếp theo mức gấp, lọc theo môn.
- **Nhắc nhở**: thông báo Windows trước giờ học và trước hạn nộp. Bạn tự chọn nhắc trước bao lâu.
- **Báo lịch thay đổi**: dời buổi, đổi phòng, tạm ngưng, thêm hoặc bỏ buổi.
- **Thông tin lớp**: giảng viên, số liên hệ, nhóm Zalo, tỉ lệ điểm.

App chạy nền dưới khay hệ thống và tự đồng bộ, nên bạn không cần mở app để nhận nhắc.

## Cài đặt

1. Tải `UTH_Notifier.exe`, đặt trong thư mục cá nhân (ví dụ `Documents`), không đặt trong `Program Files`.
2. Mở file. Nếu Windows báo *"Windows protected your PC"*, chọn **More info → Run anyway**.
3. Đăng nhập theo banner trong app:
   - **Moodle**: nhập tài khoản `courses.ut.edu.vn` một lần.
   - **Portal**: app mở cửa sổ Portal, bạn tự đăng nhập và giải CAPTCHA. Khi phiên đăng nhập hết hạn, app sẽ nhắc bạn đăng nhập lại.

Lần đầu mở, app hỏi bạn có muốn khởi động cùng Windows và tạo lối tắt ngoài Desktop không.

## Sử dụng

- **Đóng cửa sổ** thì app vẫn chạy dưới khay hệ thống (góc phải thanh taskbar). Muốn tắt hẳn: chuột phải vào icon → **Thoát**.
- **Cài đặt thông báo**: chọn mốc nhắc, giờ im lặng, chu kỳ quét lịch.
- **Phím tắt**: `Ctrl+1…4` chuyển màn, `Ctrl+R` đồng bộ, `←` `→` đổi ngày hoặc tuần.

## Cập nhật

App tự kiểm tra bản mới mỗi khi mở. Bạn cũng có thể bấm **Kiểm tra cập nhật** ở thanh bên. Khi có bản mới, chỉ cần bấm cập nhật, không phải tải lại.

## Bảo mật

- Mật khẩu và phiên đăng nhập được lưu trong Windows Credential Manager, ngay trên máy bạn.
- App chỉ kết nối tới `portal.ut.edu.vn`, `courses.ut.edu.vn` và GitHub (để cập nhật). Bản cập nhật được kiểm tra SHA-256 trước khi cài.
- App không thu thập dữ liệu.

## Sự cố thường gặp

| Hiện tượng | Cách xử lý |
|---|---|
| "Hết phiên đăng nhập" | Bấm **Đăng nhập lại** trên banner |
| Không thấy thông báo | Kiểm tra Windows **Focus / Do not disturb** và giờ im lặng trong app |
| Icon vẫn là logo cũ sau khi cập nhật | Windows còn lưu icon cũ, khởi động lại máy là hết |
| "Unhandled exception" ngay sau khi cập nhật từ bản 1.2.1 trở về trước | Đóng hộp thoại rồi mở lại app. Lỗi chỉ xảy ra một lần |

## Gỡ cài đặt

1. Thoát app từ khay hệ thống.
2. Xoá file `UTH_Notifier.exe`.
3. Xoá thư mục `%APPDATA%\UTH Notifier`.
4. Xoá các mục `UTH_Notifier` trong Credential Manager.

---

Dự án cá nhân, không phải ứng dụng chính thức của nhà trường. Báo lỗi hoặc góp ý tại [Issues](https://github.com/NguyenToan309/uth-notifier-releases/issues).
