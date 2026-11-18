## Tổng quan hệ thống bảo mật tài khoản và kiểm soát phiên truy cập

Hệ thống bảo mật trên **RedAI** được xây dựng theo tiêu chuẩn bảo mật đa lớp nghiêm ngặt, bảo vệ an toàn tuyệt đối cho tài khoản người dùng, dữ liệu Không gian làm việc và các phiên giao dịch nhạy cảm. Hệ sinh thái bảo mật bao gồm 3 trụ cột cốt lõi:

1. **Quản trị mật khẩu đăng nhập**: Cơ chế đổi mật khẩu với kiểm tra độ mạnh tự động, hỗ trợ ẩn/hiện mật khẩu và kiểm soát phiên đổi mật khẩu đầu tiên sau khi kích hoạt tài khoản.
2. **Xác thực hai lớp (Two-Factor Authentication — 2FA)**: Hỗ trợ linh hoạt 3 kênh bảo vệ song song:
   - *Xác thực qua tin nhắn SMS*: Nhận mã OTP trực tiếp về số điện thoại cá nhân.
   - *Xác thực qua hòm thư Email*: Nhận mã OTP qua email đã được kiểm chứng.
   - *Ứng dụng bảo mật Google Authenticator (TOTP)*: Sinh mã số biến động theo thời gian thực 30 giây, hoạt động ngoại tuyến không phụ thuộc sóng mạng.
3. **Trung tâm Quản lý Phiên đăng nhập (Session Security)**: Giám sát toàn bộ các thiết bị, trình duyệt, hệ điều hành và địa chỉ IP đang duy trì đăng nhập tài khoản; hỗ trợ thu hồi quyền truy cập từ xa cho từng thiết bị hoặc đăng xuất khẩn cấp toàn bộ các phiên khác chỉ với 1 cú nhấp chuột.

---

## Các bước thực hiện chi tiết trên giao diện

Quy trình quản lý bảo mật và kiểm soát phiên truy cập được thiết kế trực quan theo các bước dưới đây:

```
[Thẻ Bảo mật] ──> [Đổi mật khẩu tài khoản]
             │
             ├──> [Bật/Tắt 2FA: SMS / Email / Google Authenticator]
             │
             └──> [Mở /settings/security] ──> [Thu hồi phiên lẻ hoặc Thu hồi tất cả phiên khác]
```

| Bước | Thành phần UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở thẻ Bảo mật tài khoản** | Tại trang Profile (`/profile`), nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **Bảo mật**. Thẻ hiển thị các khối chức năng: Đổi mật khẩu, Các phương thức xác thực 2 bước (2FA) và liên kết mở nhanh Trung tâm Quản lý phiên. |
| **2** | **Đổi mật khẩu đăng nhập** | • Nhấp vào nút <img src="https://api.iconify.design/lucide:key.svg?color=%23ff3333" width="16" alt="" /> **Đổi mật khẩu**: Biểu mẫu nhập mật khẩu xuất hiện gồm 3 trường:<br>  + **Mật khẩu hiện tại \***: Nhập mật khẩu bạn đang sử dụng để đăng nhập.<br>  + **Mật khẩu mới \***: Nhập mật khẩu mới (yêu cầu tối thiểu 8 ký tự, kết hợp chữ hoa, chữ thường, chữ số và ký tự đặc biệt).<br>  + **Xác nhận mật khẩu mới \***: Nhập lại chính xác mật khẩu mới vừa tạo.<br>• Mỗi ô nhập đều có biểu tượng con mắt <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="14" alt="" /> / <img src="https://api.iconify.design/lucide:eye-off.svg?color=%23ff3333" width="14" alt="" /> ở đuôi ô giúp bạn kiểm tra ký tự trước khi xác nhận.<br>• Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Cập nhật mật khẩu**. Hệ thống lưu mật khẩu mới và gửi thông báo xác nhận thành công. |
| **3** | **Bật/Tắt Xác thực 2FA qua SMS** | • Tìm đến mục **Xác thực qua tin nhắn (SMS)**.<br>• **Điều kiện tiên quyết**: Số điện thoại của bạn phải ở trạng thái đã xác minh (có dấu tích xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> ở thẻ Thông tin cá nhân). Nếu chưa xác minh, công tắc sẽ bị mờ kèm hướng dẫn xác thực SĐT trước.<br>• Gạt công tắc <img src="https://api.iconify.design/lucide:toggle-right.svg?color=%23ff3333" width="18" alt="" /> **Bật**: Hệ thống kích hoạt gửi mã OTP qua SMS mỗi khi có phiên đăng nhập mới từ thiết bị lạ. |
| **4** | **Bật/Tắt Xác thực 2FA qua Email** | • Tìm đến mục **Xác thực qua thư điện tử (Email)**.<br>• **Điều kiện tiên quyết**: Hòm thư Email phải được xác thực hoàn tất trước đó.<br>• Gạt công tắc chuyển sang trạng thái **Bật** màu xanh: Mỗi lần đăng nhập, hệ thống sẽ gửi một mã số 6 chữ số về hòm thư để xác minh danh tính. |
| **5** | **Kích hoạt Google Authenticator (TOTP)** | • Tìm đến mục **Ứng dụng Google Authenticator** $\rightarrow$ Gạt công tắc sang trạng thái **Bật**.<br>• Khung hướng dẫn thiết lập trượt vào từ góc phải màn hình:<br>  + **Mã QR bí mật**: Mở ứng dụng Google Authenticator hoặc Microsoft Authenticator trên điện thoại $\rightarrow$ Chọn *Quét mã QR* $\rightarrow$ Đưa camera quét mã QR hiển thị trên màn hình máy tính.<br>  + **Khóa cài đặt thủ công (Secret Key)**: Nếu không quét được camera, bấm biểu tượng sao chép <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="14" alt="" /> cạnh chuỗi ký tự bí mật để nhập thủ công vào ứng dụng trên điện thoại.<br>  + **Nhập mã OTP xác nhận**: Nhập 6 chữ số đang hiển thị trên ứng dụng Authenticator vào 6 ô vuông nhập mã số chuyên dụng $\rightarrow$ Bấm nút **Xác nhận kích hoạt**.<br>• Hệ thống xác thực mã chuẩn xác và chuyển trạng thái Google Authenticator sang **Đã kích hoạt**. |
| **6** | **Mở Trung tâm Quản lý Phiên đăng nhập** | • Cuộn xuống cuối thẻ Bảo mật, nhấp vào liên kết <img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> **Quản lý phiên đăng nhập thiết bị** (hoặc truy cập trực tiếp đường dẫn `/settings/security`).<br>• Trang **Bảo mật phiên đăng nhập** mở ra với bảng danh sách các phiên thiết bị đang hoạt động. |
| **7** | **Xem chi tiết các phiên đang hoạt động** | Mỗi phiên đăng nhập được hiển thị dưới dạng một thẻ danh thiếp thiết bị trực quan:<br>• **Tên thiết bị & Trình duyệt**: Hiển thị rõ Trình duyệt và Hệ điều hành (ví dụ: `Chrome 128 · Windows 11`, `Safari 17 · iOS 17`).<br>• **Huy hiệu Phiên hiện tại**: Thiết bị bạn đang thao tác trực tiếp sẽ có huy hiệu tròn màu xanh lá nổi bật: <img src="https://api.iconify.design/lucide:check-circle.svg?color=%23ff3333" width="14" alt="" /> **Phiên hiện tại**.<br>• **Địa chỉ IP**: Hiển thị địa chỉ IP truy cập (ví dụ: `IP: 118.69.182.xxx`).<br>• **Thời gian hoạt động gần nhất**: Ghi nhận ngày giờ phiên gửi yêu cầu cuối cùng lên hệ thống.<br>• **Thời điểm hết hạn**: Ngày giờ phiên sẽ tự động hết hạn nếu không tiếp tục sử dụng. |
| **8** | **Thu hồi phiên đơn lẻ & Đăng xuất khẩn cấp** | • **Thu hồi một phiên cụ thể**: Rê chuột đến phiên nghi vấn hoặc thiết bị không còn sử dụng $\rightarrow$ Bấm biểu tượng nút <img src="https://api.iconify.design/lucide:log-out.svg?color=%23ff3333" width="16" alt="" /> **Thu hồi phiên này** ở góc phải $\rightarrow$ Hộp thoại xác nhận hiển thị $\rightarrow$ Bấm **Xác nhận**. Thiết bị tương ứng sẽ lập tức bị đá văng khỏi tài khoản.<br>• **Thu hồi toàn bộ các phiên khác (Revoke Others)**: Trên thanh tiêu đề của bảng phiên, bấm nút đỏ <img src="https://api.iconify.design/lucide:log-out.svg?color=%23ff3333" width="16" alt="" /> **Thu hồi các phiên khác** $\rightarrow$ Hộp thoại cảnh báo bảo mật **Xác nhận thu hồi** mở ra $\rightarrow$ Bấm **Xác nhận thu hồi**. Ngay lập tức, tất cả các thiết bị khác (điện thoại, máy tính bảng, máy tính văn phòng) đều bị đăng xuất, chỉ duy nhất phiên hiện tại của bạn được giữ lại an toàn. |

---

## Kiểm tra kết quả

Sau khi cấu hình bảo mật và quản lý phiên, bạn có thể kiểm tra hiệu lực trên hệ thống:

1. **Sau khi đổi mật khẩu**: Đăng xuất tài khoản và đăng nhập lại bằng mật khẩu mới để đảm bảo mật khẩu cũ đã bị vô hiệu hóa.
2. **Sau khi bật 2FA**: Khi đăng nhập từ trình duyệt ẩn danh hoặc thiết bị mới, hệ thống sẽ tự động yêu cầu bước thứ 2: nhập mã OTP qua SMS, Email hoặc Google Authenticator tùy theo các kênh bạn đã bật.
3. **Trên trang Bảo mật phiên (`/settings/security`)**: Sau khi bấm *Thu hồi các phiên khác*, danh sách phiên chỉ còn lại duy nhất dòng thẻ có huy hiệu xanh `Phiên hiện tại`, huy hiệu số lượng phiên rút gọn về `1`.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể hỗ trợ bạn kiểm tra trạng thái 2FA, theo dõi danh sách các phiên đăng nhập lạ hoặc thực hiện lệnh thu hồi phiên từ xa, bạn cần cấu hình Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - User Profile & Account` |
| **Mã định danh Kỹ năng (Skill ID)** | `c8319e04-7a1b-4f92-91ef-8d5421ac0721` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - User & Account` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `387d45d1-3e2a-4ec5-9572-218d70618d5c` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Kiểm tra trạng thái bảo mật 2FA** | `getTwoFactorAuthStatus` | `Hãy kiểm tra trạng thái xác thực 2 bước của tài khoản tôi xem SMS, Email hay Google Authenticator đang được bật.` |
| **Bật/Tắt xác thực 2 bước qua SMS** | `toggleSmsAuth` | `Hãy bật chế độ xác thực hai lớp qua SMS (enabled: true) cho tài khoản của tôi.` |
| **Bật/Tắt xác thực 2 bước qua Email** | `toggleEmailAuth` | `Hãy bật chế độ nhận mã OTP đăng nhập qua Email để tăng cường an toàn.` |
| **Lấy mã QR kích hoạt Authenticator** | `setupGoogleAuth` | `Hãy khởi tạo liên kết Google Authenticator mới và gửi cho tôi khóa bí mật secretKey dạng text để tôi thêm vào điện thoại.` |
| **Xác nhận mã OTP kích hoạt Authenticator** | `verifyGoogleAuth` | `Mã OTP trên ứng dụng Authenticator của tôi hiện tại là "619284", hãy gửi xác thực để hoàn tất kích hoạt.` |
| **Xem danh sách các phiên đăng nhập** | `getBrowserSessions` | `Hãy quét toàn bộ danh sách các phiên đăng nhập hiện tại của tôi xem có thiết bị hoặc IP lạ nào không.` |
| **Thu hồi một phiên thiết bị lạ** | `revokeBrowserSession` | `Hãy thu hồi phiên đăng nhập có publicId là "sess_win_chrome_9918" ngay lập tức.` |
| **Đăng xuất toàn bộ các thiết bị khác** | `revokeOtherBrowserSessions` | `Tôi nghi ngờ tài khoản bị lộ mật khẩu, hãy đăng xuất ngay lập tức tất cả các phiên đăng nhập khác, chỉ giữ lại phiên hiện tại.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Gạt công tắc bật SMS 2FA trên giao diện | Gọi `getTwoFactorAuthStatus` thấy `otpSmsEnabled` trả về `true`. |
| Bấm Thu hồi một phiên đăng nhập trên trang `/settings/security` | Gọi `getBrowserSessions` thấy mảng danh sách phiên không còn chứa phiên bị xóa. |
| Bấm nút "Thu hồi các phiên khác" trên giao diện | Gọi `getBrowserSessions` thấy chỉ còn duy nhất 1 item có thuộc tính `current: true`. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `toggleEmailAuth` thành true | Công tắc Xác thực qua Email trên thẻ Bảo mật tự động gạt sang màu xanh. |
| Agent gọi `revokeOtherBrowserSessions` | F5 trang `/settings/security`, danh sách phiên được dọn dẹp sạch sẽ, chỉ còn lại phiên đang dùng. |
