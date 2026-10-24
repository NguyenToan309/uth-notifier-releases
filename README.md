# UTH Notifier

Ứng dụng Windows cho sinh viên **Trường ĐH Giao thông vận tải TP.HCM (UTH)**: mở lên là thấy ngay **lịch học** (Portal) và **deadline bài tập** (Moodle), không cần vào web.

**[⬇ Tải bản mới nhất (UTH_Notifier.exe)](https://github.com/NguyenToan309/uth-notifier-releases/releases/latest/download/UTH_Notifier.exe)**

Chỉ cần 1 file `.exe`: không cần cài Python hay thư viện gì thêm. Chạy trên Windows 10/11.

![Màn Hôm nay](docs/hom-nay.png)

> Ảnh minh hoạ dùng dữ liệu mẫu, tên môn và giảng viên trong ảnh là giả.

## Tính năng

- **Hôm nay**: các buổi học trong ngày theo giờ. Buổi đang học có viền cam, buổi kế tiếp có "Còn X phút", buổi đổi phòng hoặc tạm ngưng có nhãn cảnh báo. Bên cạnh là các deadline trong 7 ngày tới.
- **Tuần**: lịch Thứ 2 → Chủ nhật theo giờ thật; deadline hiện ở đầu cột ngày. Bấm vào một buổi để xem chi tiết môn: các buổi trong tuần, deadline, nút **Mở trên Moodle**.
- **Deadline**: chia nhóm *Quá hạn / Hôm nay / 3 ngày tới / Sau đó*, lọc theo môn và tìm theo tên bài. Mức khẩn có cả màu, icon và chữ.
- **Cài đặt thông báo**: mốc nhắc trước giờ học và trước hạn nộp, tóm tắt buổi sáng, giờ im lặng (có thể qua nửa đêm), cài riêng cho từng môn.
- **Chạy nền ở khay hệ thống**: đóng cửa sổ thì app ẩn xuống khay. App tự đồng bộ mỗi 20 phút, hoặc bấm **Đồng bộ ngay** / `Ctrl+R`.
- **Tự cập nhật**: khi có bản mới, app tự tải về và chỉ hỏi bạn **Khởi động lại**.
- Giao diện sáng/tối theo Windows. Phím tắt: `Ctrl+1…4` chuyển màn, `←/→` đổi ngày/tuần, `Esc` đóng panel chi tiết.

| Lịch tuần + chi tiết môn | Deadline |
|---|---|
| ![Tuần](docs/tuan.png) | ![Deadline](docs/deadline.png) |

## Cài và chạy lần đầu

1. Tải `UTH_Notifier.exe` ở link trên và đặt vào một thư mục của bạn, ví dụ `Documents\UTH Notifier`.
   Tránh để trong `Program Files`, vì ở đó app không có quyền tự cập nhật.
2. Mở file. Nếu Windows hiện **"Windows protected your PC"**, bấm **More info → Run anyway**. Cảnh báo này xuất hiện vì app chưa có chữ ký số trả phí, không phải vì app có virus.
3. Lần đầu, app hiện banner vàng **"Hết phiên đăng nhập"**. Bấm **Đăng nhập lại**:
   - **Moodle**: nhập tài khoản và mật khẩu Moodle (courses.ut.edu.vn). Chỉ cần nhập một lần.
   - **Portal**: app mở cửa sổ portal.ut.edu.vn để **bạn tự đăng nhập và tự giải CAPTCHA**. Cửa sổ tự đóng khi xong. Phiên đăng nhập giữ khoảng **30 ngày**; khi hết hạn, app sẽ nhắc đăng nhập lại.
4. Xong. Lịch và deadline hiện ngay.

**Muốn app tự chạy khi bật máy:** nhấn `Win + R`, gõ `shell:startup`, rồi tạo shortcut tới `UTH_Notifier.exe` trong thư mục vừa mở.

## Bảo mật và quyền riêng tư

- Mật khẩu Moodle và phiên đăng nhập Portal được lưu trong **Windows Credential Manager** của chính máy bạn, không lưu ở file thường.
- App chỉ kết nối tới **portal.ut.edu.vn**, **courses.ut.edu.vn** và **GitHub** (để kiểm tra bản mới). Không có máy chủ nào khác, không thu thập dữ liệu.
- App **không vượt CAPTCHA**: bạn luôn tự đăng nhập Portal.
- Mỗi bản cập nhật được kiểm tra mã SHA-256 trước khi thay thế; file không khớp sẽ bị bỏ.

## Câu hỏi thường gặp

**Lịch trống, thanh dưới báo "Portal: Hết phiên đăng nhập"?**
Phiên Portal đã hết hạn (khoảng 30 ngày một lần). Bấm **Đăng nhập lại** trên banner.

**Thanh dưới báo "Lỗi mạng"?**
App vẫn hiển thị dữ liệu lần đồng bộ trước (ghi rõ "Dữ liệu từ HH:mm") và sẽ thử lại sau. Bạn cũng có thể bấm **Đồng bộ ngay**.

**Sao không thấy "Đã nộp" / "Chưa nộp" cho mọi bài?**
Moodle không cho biết trạng thái nộp bài. App chỉ ghi "Chưa nộp" khi Moodle còn hiện nút nộp bài cho bài đó.

**Gỡ app thế nào?**
Thoát app (chuột phải icon ở khay → **Thoát**), xoá file `.exe`, xoá thư mục `%APPDATA%\UTH Notifier`, rồi vào **Credential Manager → Windows Credentials** xoá các mục `UTH_Notifier`.

## Các phiên bản

Xem lịch sử thay đổi ở mục **[Releases](https://github.com/NguyenToan309/uth-notifier-releases/releases)**. App đã cài sẽ tự cập nhật, không cần tải lại.

---

Dự án cá nhân của sinh viên, không phải ứng dụng chính thức của nhà trường. Có lỗi hoặc góp ý? Mở một [Issue](https://github.com/NguyenToan309/uth-notifier-releases/issues).
