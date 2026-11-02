## Tổng quan quy trình quản lý hồ sơ cá nhân và xác thực thông tin

Trang **Hồ sơ cá nhân (Profile Page)** trên hệ thống **RedAI** là trung tâm quản trị danh tính người dùng, giúp bạn thiết lập hình ảnh đại diện chuyên nghiệp, hoàn thiện thông tin định danh và xác thực các kênh liên lạc thiết yếu (Email và Số điện thoại). Việc hoàn thiện và xác thực hồ sơ cá nhân mang lại nhiều lợi ích quan trọng:

- **Bảo mật và phục hồi tài khoản**: Email và Số điện thoại đã xác thực là điều kiện tiên quyết để kích hoạt cơ chế Xác thực 2 bước (2FA) và nhận mã khôi phục khi quên mật khẩu.
- **Độ tin cậy trong Không gian làm việc**: Hiển thị ảnh đại diện và huy hiệu xác minh chính thức trên toàn bộ các kênh chat, bảng phân công nhiệm vụ và lịch sử thao tác của Workspace.
- **Tối ưu hóa dung lượng và tốc độ**: Ảnh bìa và ảnh đại diện được hệ thống tự động xử lý, nén chuẩn WebP chất lượng cao và lưu trữ đám mây tốc độ cao.

---

## Các bước thực hiện chi tiết trên giao diện

Quy trình quản lý hồ sơ và xác thực thông tin cá nhân bao gồm 7 bước tuần tự trên giao diện:

```
[Truy cập /profile] ──> [Đổi Ảnh bìa & Avatar] ──> [Điền Họ tên, Giới tính, Ngày sinh, Địa chỉ]
                              │
                              ├──> [Xác thực Email qua OTP 6 số]
                              └──> [Xác thực SĐT qua OTP SMS/ZNS] ──> [Bấm Lưu thay đổi]
```

| Bước | Thành phần UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Truy cập trang Profile** | Nhấp vào ảnh đại diện cá nhân ở góc dưới bên trái thanh điều hướng hoặc góc trên bên phải $\rightarrow$ Chọn <img src="https://api.iconify.design/lucide:user.svg?color=%23ff3333" width="16" alt="" /> **Hồ sơ cá nhân** (đường dẫn `/profile`). Trang quản lý tài khoản hiển thị với phần Ảnh bìa nổi bật trên đỉnh và các khối thông tin thu gọn (Accordion) bên dưới. |
| **2** | **Cập nhật Ảnh bìa (Cover Image)** | • Rê chuột (Hover) lên khu vực ảnh bìa trên đỉnh trang $\rightarrow$ Lớp phủ bán trong suốt xuất hiện kèm biểu tượng máy ảnh và dòng chữ *Đang tải lên...* nếu có tiến trình.<br>• Nhấp chuột trực tiếp vào ảnh bìa $\rightarrow$ Hộp thoại chọn tệp của máy tính mở ra $\rightarrow$ Chọn hình ảnh mong muốn (hỗ trợ JPG, PNG, WebP; tỷ lệ khuyến nghị 16:9 hoặc 3:1).<br>• Hệ thống sẽ trực tiếp tải ảnh lên kho lưu trữ đám mây an toàn, cập nhật tức thì vào giao diện và hiển thị thông báo nổi màu xanh: *"Cập nhật ảnh bìa thành công"*. |
| **3** | **Cập nhật Ảnh đại diện (Avatar)** | • Nhấp chuột trực tiếp vào khung ảnh đại diện tròn nằm đè lên chân ảnh bìa $\rightarrow$ Chọn tệp hình ảnh chân dung rõ nét từ máy tính.<br>• **Bộ xử lý ảnh tự động**: Hệ thống tự động kiểm tra kích thước (tối đa 2MB), nén ảnh về định dạng tối ưu WebP chất lượng cao và đồng bộ sang toàn bộ Không gian làm việc.<br>• Biểu tượng xoay tròn (loading spinner) xuất hiện trong lúc tải lên, sau đó ảnh đại diện mới sẽ hiển thị ngay lập tức kèm thông báo: *"Cập nhật avatar thành công"*. |
| **4** | **Soạn thảo thông tin nhận diện cơ bản** | Nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:user.svg?color=%23ff3333" width="16" alt="" /> **Thông tin cá nhân** để hiển thị biểu mẫu:<br>• **Họ và tên \***: Nhập họ và tên đầy đủ của bạn (bắt buộc, ví dụ: `Nguyễn Văn An`). Trường này sẽ hiển thị làm tên đại diện của bạn trong các cuộc trò chuyện và bảng phân công.<br>• **Địa chỉ**: Nhập địa chỉ cư trú hoặc địa chỉ liên hệ hiện tại.<br>• **Giới tính \***: Nhấp ô chọn thả xuống để chọn một trong 3 tùy chọn: *Nam*, *Nữ* hoặc *Khác*.<br>• **Ngày sinh**: Nhấp vào ô chọn ngày sinh để mở bộ chọn ngày sinh dạng lịch tương tác, hỗ trợ chọn Năm/Tháng/Ngày theo định dạng chuẩn `yyyy-MM-dd`. Hệ thống tự động giới hạn không cho phép chọn ngày trong tương lai. |
| **5** | **Xác thực địa chỉ Email** | Nhìn vào ô nhập **Email** trong biểu mẫu:<br>• Nếu tài khoản chưa xác thực email, bên cạnh ô nhập sẽ xuất hiện nút viền nổi bật <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **Xác thực**.<br>• Nhập chính xác địa chỉ email hợp lệ $\rightarrow$ Bấm nút **Xác thực**.<br>• Hệ thống gửi mã OTP xác nhận về hộp thư của bạn và mở hộp thoại **Xác thực Email**.<br>• Mở email, lấy mã số OTP gồm **6 chữ số** $\rightarrow$ Điền vào ô nhập mã trên hộp thoại $\rightarrow$ Bấm nút **Xác nhận**.<br>• Sau khi xác thực thành công, cạnh chữ Email sẽ xuất hiện dấu tích xanh chính thức <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" />, ô nhập email tự động khóa chống sửa đổi trái phép. |
| **6** | **Xác thực Số điện thoại** | Nhìn vào ô nhập **Số điện thoại** trong biểu mẫu:<br>• Ô nhập sử dụng thành phần chọn cờ quốc gia và mã vùng quốc tế, mặc định là cờ Việt Nam (mã vùng `+84`), tự động giữ số `0` ở đầu số.<br>• Nếu số điện thoại chưa xác thực, nút viền <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **Xác thực** sẽ sáng lên.<br>• Nhập số điện thoại của bạn $\rightarrow$ Bấm nút **Xác thực** $\rightarrow$ Hộp thoại **Xác thực Số điện thoại** hiển thị.<br>• Hệ thống gửi mã OTP 6 số qua tin nhắn SMS hoặc thông báo Zalo ZNS $\rightarrow$ Nhập 6 chữ số vào hộp thoại $\rightarrow$ Bấm **Xác nhận**.<br>• Khi xác thực thành công, dấu tích xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> xuất hiện cạnh nhãn Số điện thoại và ô nhập được bảo vệ chống sửa đổi. |
| **7** | **Lưu thay đổi hồ sơ** | Ở góc dưới bên phải của thẻ Thông tin cá nhân:<br>• Nút <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> **Hủy**: Đóng thẻ và giữ nguyên dữ liệu ban đầu.<br>• Nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **Lưu**: Gửi dữ liệu cập nhật lên hệ thống. Thông báo nổi *"Cập nhật thông tin cá nhân thành công"* xuất hiện ở góc trên màn hình. |

---

## Kiểm tra kết quả

Sau khi hoàn tất cập nhật hồ sơ, bạn có thể kiểm chứng kết quả trực quan trên các vị trí sau của giao diện:

1. **Trên thanh Profile Header**: Tên hiển thị mới xuất hiện với cỡ chữ lớn in đậm kèm dấu tích xanh xác thực danh tính <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> và Chip loại tài khoản (*Tài khoản cá nhân* hoặc *Tài khoản doanh nghiệp*).
2. **Trên thanh điều hướng chính**: Ảnh đại diện Avatar mới hiển thị sắc nét ở góc trái/phải màn hình thay cho biểu tượng chữ cái mặc định.
3. **Trên dòng trạng thái Email và SĐT**: Cả hai kênh đều hiển thị biểu tượng khiên tích xanh đã xác thực, các nút yêu cầu xác thực biến mất.
4. **Trong các Không gian làm việc**: Mọi tương tác của bạn trong Chat, Bảng dữ liệu và Luồng Workflow đều hiển thị đúng tên và ảnh đại diện mới vừa thiết lập.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tra cứu thông tin hồ sơ, hỗ trợ cập nhật thông tin cá nhân hoặc đối soát trạng thái xác thực tài khoản của người dùng, bạn cần đảm bảo Agent đã được trang bị Kỹ năng (Skill) sau:

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - User Profile & Account` |
| **Mã định danh Kỹ năng (Skill ID)** | `c8319e04-7a1b-4f92-91ef-8d5421ac0721` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - User & Account` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `387d45d1-3e2a-4ec5-9572-218d70618d5c` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản (JWT Authenticated Scope) |

---

### Bảng ánh xạ từng tính năng kèm Prompt mẫu tương ứng cho AI Agent

Dưới đây là bảng ánh xạ chi tiết các công cụ API của AI Agent và câu lệnh thực thi cụ thể cho từng thao tác quản lý hồ sơ cá nhân:

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Xem hồ sơ cá nhân hiện tại** | `getCurrentUserProfile` | `Hãy tra cứu thông tin hồ sơ cá nhân của tôi xem họ tên, email, số điện thoại và trạng thái xác thực hiện tại như thế nào.` |
| **Cập nhật họ tên và địa chỉ** | `updatePersonalProfile` | `Hãy cập nhật họ tên của tôi thành "Nguyễn Văn An" và cập nhật địa chỉ liên hệ thành "Tòa nhà Landmark 81, TP. Hồ Chí Minh".` |
| **Cập nhật ngày sinh và giới tính** | `updatePersonalProfile` | `Hãy đổi giới tính của tôi thành "MALE" và ngày sinh thành "1992-08-15".` |
| **Gửi OTP xác thực email** | `sendEmailVerificationOtp` | `Hãy kích hoạt gửi mã OTP xác thực tài khoản về hòm thư "nguyenvanan@gmail.com" giúp tôi.` |
| **Xác nhận mã OTP email** | `verifyEmailOtp` | `Tôi vừa nhận được mã xác thực email là "829104", hãy gửi mã này kèm verificationKey để hoàn tất xác thực email.` |
| **Gửi OTP xác thực số điện thoại** | `sendPhoneVerificationOtp` | `Hãy gửi mã OTP xác thực số điện thoại đến số "+84912345678" giúp tôi.` |
| **Xác nhận mã OTP số điện thoại** | `verifyPhoneOtp` | `Mã OTP gửi về điện thoại của tôi là "472910", hãy kích hoạt xác minh số điện thoại cho tài khoản của tôi.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Đổi họ tên và bấm Lưu trên giao diện Profile | Gọi `getCurrentUserProfile` thấy trường `fullName` trả về đúng tên mới. |
| Hoàn tất nhập mã OTP 6 số xác thực Email trên hộp thoại | Gọi `getCurrentUserProfile` thấy trường `isVerifyEmail` chuyển thành `true`. |
| Hoàn tất nhập mã OTP xác thực Số điện thoại | Gọi `getCurrentUserProfile` thấy trường `isVerifyPhone` chuyển thành `true`. |
| Tải ảnh đại diện mới lên avatar | Gọi `getCurrentUserProfile` thấy trường `avatarUrl` chứa liên kết ảnh WebP hợp lệ. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `updatePersonalProfile` đổi tên | Tải lại trang Profile, tên lớn trên Profile Header và ô nhập Họ và tên tự động đổi sang tên mới. |
| Agent gọi `verifyEmailOtp` thành công | Biểu tượng tích xanh <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> xuất hiện ngay cạnh nhãn Email và nút Xác thực biến mất. |
| Agent gọi `verifyPhoneOtp` thành công | Biểu tượng tích xanh xuất hiện cạnh nhãn Số điện thoại trên thẻ Thông tin cá nhân. |
