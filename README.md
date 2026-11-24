# Google Switch

Đổi nhanh nhiều tài khoản Google cho **Antigravity CLI (agy)** trên Windows.

- Lưu nhiều tài khoản Google, chọn một cái rồi bấm **Áp dụng** là agy chuyển sang tài khoản đó.
- Xem hạn mức còn lại của từng tài khoản: Gemini và Claude/GPT, khung 5 giờ và theo tuần, kèm giờ reset.
- Icon nhỏ cạnh đồng hồ hiện % Gemini (5 giờ) của tài khoản đang dùng, đổi màu khi sắp hết.
  Bấm chuột trái: menu chuyển tài khoản. Bấm chuột phải: mở cửa sổ chính.
- **Tự cập nhật**: khi có bản mới ở mục Releases, app tự tải về, kiểm tra mã SHA-256 rồi mở lại.

## Tải về

Vào [Releases](https://github.com/danielisdn/google-switch/releases/latest), tải `GoogleSwitch.exe` và chạy luôn.
Không cần cài, không cần Python.

## Cần có

- Windows 10/11.
- Antigravity CLI (`agy`) đã cài và đăng nhập thử được một lần.
  Nếu agy nằm chỗ khác mặc định, đặt biến môi trường `ANTIGRAVITY_COMMAND` trỏ tới `agy.exe`.

## Cách dùng

1. Bấm **+ Thêm tài khoản**, đặt tên (hoặc để trống để lấy theo email), bấm **Tiếp tục**.
2. Cửa sổ agy mở ra: đăng nhập Google, xong gõ `/exit`. **Không** gõ `/logout`.
3. Lặp lại cho các tài khoản khác.
4. Chọn một tài khoản rồi bấm **Áp dụng**.

Windows 11 có thể giấu icon trong mục `^` cạnh đồng hồ: kéo nó ra taskbar để ghim.

## Dữ liệu và bảo mật

- Token đăng nhập được mã hoá bằng DPAPI theo user Windows, lưu ở `%LOCALAPPDATA%\GoogleSwitch`.
  Chỉ đúng user Windows đó giải mã được; file exe không chứa dữ liệu cá nhân nào.
- App chỉ nói chuyện với máy chủ Google (đọc hạn mức) và GitHub (kiểm tra bản mới).
- Xoá thư mục `%LOCALAPPDATA%\GoogleSwitch` là xoá hết tài khoản đã lưu.
