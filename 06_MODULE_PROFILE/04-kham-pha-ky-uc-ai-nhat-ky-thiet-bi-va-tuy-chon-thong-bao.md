## Tổng quan bộ nhớ ký ức AI, nhật ký thiết bị và cài đặt thông báo

Bên cạnh các thông tin định danh và bảo mật cơ bản, trang **Hồ sơ cá nhân (Profile Page)** trên hệ thống **RedAI** còn quy tụ 3 công cụ nâng cao hỗ trợ cá nhân hóa trải nghiệm người dùng, giám sát an ninh thiết bị và tùy biến kênh tiếp nhận thông tin từ hệ thống:

1. **Bộ nhớ cá nhân & Đồ thị Ký ức AI (User Memories & Knowledge Graph)**: Trợ lý ảo AI Agent trên RedAI sở hữu năng lực học hỏi liên tục. Mọi sở thích, phong cách làm việc, quy tắc nghiệp vụ và thói quen mà bạn chia sẻ trong các phiên trò chuyện sẽ được AI tự động phân tích, trích xuất và kết nối thành một **Đồ thị Ký ức Người dùng (User Memory Graph)**. Bạn có thể mở trực tiếp không gian đồ thị tương tác 3D để khám phá, kiểm tra và đồng bộ lại các ký ức này.
2. **Nhật ký xác thực & Thiết bị truy cập (Auth Verification Logs)**: Bảng dữ liệu ghi nhận lịch sử mọi lần gửi mã xác thực, đăng nhập và đổi mật khẩu kèm thông tin chi tiết về Địa chỉ IP, Trình duyệt, Hệ điều hành và thời điểm thực hiện; giúp bạn phát hiện sớm các dấu hiệu truy cập bất thường.
3. **Cài đặt Tùy chọn Thông báo (Notification Settings)**: Trung tâm kiểm soát 6 danh mục thư điện tử (Email) hệ thống gửi tới hòm thư của bạn, tích hợp cơ chế tự động lưu tức thì (Auto-save) khi bật/tắt công tắc.

---

## Các bước thực hiện chi tiết trên giao diện

Dưới đây là bảng hướng dẫn từng bước vận hành cho 3 tính năng nâng cao:

```
[Thẻ Bộ nhớ cá nhân] ───────> [Bấm "Khám phá Đồ thị Ký ức"] ──> [Mở Modal Đồ thị 3D & Đồng bộ ký ức]
              │
[Thẻ Danh sách Thiết bị] ────> [Xem Bảng nhật ký đăng nhập] ───> [Lọc IP, Trình duyệt, Ngày tháng]
              │
[Thẻ Tùy chọn thông báo] ────> [Gạt bật/tắt 6 công tắc Email] ──> [Hệ thống tự động lưu tức thì]
```

| Bước | Thành phần UI | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở thẻ Bộ nhớ cá nhân** | Tại trang Profile (`/profile`), nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> **Bộ nhớ cá nhân**. Thẻ hiển thị khu vực Bộ nhớ cá nhân với giao diện phẳng (border-0) sang trọng, biểu tượng Bộ não màu tím nổi bật kèm thông điệp tóm tắt về mục đích lưu trữ ký ức người dùng. |
| **2** | **Khám phá Đồ thị Ký ức toàn màn hình** | Bấm nút màu tím nổi bật <img src="https://api.iconify.design/lucide:network.svg?color=%23ff3333" width="16" alt="" /> **Khám phá Đồ thị Ký ức** ở góc phải của thẻ:<br>• Hộp thoại đồ thị tri thức **Khám phá Đồ thị Ký ức** mở ra với kích thước toàn màn hình.<br>• **Trực quan hóa không gian 3D**: Toàn bộ mạng lưới ký ức của bạn hiển thị dạng các nút cầu (Nodes) phát sáng lơ lửng trong không gian 3D, kết nối với nhau bằng các đường liên kết ngữ nghĩa (Edges).<br>• **Thao tác tương tác 3D**: Dùng chuột trái kéo để xoay góc nhìn 360 độ, cuộn bánh xe chuột để phóng to/thu nhỏ (Zoom in/out), và giữ chuột phải để di chuyển vị trí đồ thị.<br>• **Xem chi tiết nút ký ức**: Nhấp chuột trái vào bất kỳ quả cầu nào để xem bảng thông tin bên phải: Nội dung sự thật ghi nhớ, độ tin cậy, thời gian ghi nhận và các chủ đề liên quan.<br>• **Đồng bộ ký ức thủ công**: Bấm nút **Đồng bộ ký ức** trên thanh điều khiển của đồ thị để kích hoạt tiến trình đối soát và tổng hợp lại ký ức người dùng mới nhất từ các cuộc trò chuyện. Bấm dấu <img src="https://api.iconify.design/lucide:x.svg?color=%23ff3333" width="16" alt="" /> để đóng hộp thoại. |
| **3** | **Mở thẻ Lịch sử đăng nhập & Thiết bị** | Nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:smartphone.svg?color=%23ff3333" width="16" alt="" /> **Lịch sử đăng nhập & Thiết bị**. Bảng dữ liệu nhật ký xác thực nạp toàn bộ danh sách các phiên thao tác tài khoản gần nhất. |
| **4** | **Tra cứu và lọc nhật ký thiết bị** | Bảng hiển thị 5 cột thông tin chi tiết:<br>• **Phương thức xác thực (`authMethod`)**: Hiển thị loại hành động (ví dụ: `PASSWORD_LOGIN`, `SMS_OTP`, `EMAIL_OTP`, `GOOGLE_AUTHENTICATOR`, `PASSWORD_RESET`).<br>• **Trạng thái (`status`)**: Nhãn màu hiển thị kết quả thao tác: *Thành công (SUCCESS)* màu xanh lá hoặc *Thất bại (FAILED)* màu đỏ.<br>• **Địa chỉ IP (`ipAddress`)**: Ghi nhận chính xác IP mạng truy cập.<br>• **Thiết bị & Trình duyệt (`userAgent`)**: Tên trình duyệt, phiên bản và hệ điều hành của máy truy cập (ví dụ: `Mozilla/5.0 (Windows NT 10.0; Win64; x64)...`). Rê chuột lên để xem toàn bộ chuỗi User-Agent đầy đủ.<br>• **Thời gian (`createdAt`)**: Thời điểm diễn ra thao tác theo định dạng ngày giờ chính xác.<br>• **Thanh công cụ lọc và tìm kiếm**: Sử dụng ô tìm kiếm để gõ nhanh địa chỉ IP hoặc trình duyệt; nhấp vào bộ chọn ngày tháng để lọc các sự kiện theo khoảng thời gian tùy chọn; bấm nút xoay vòng để tải lại dữ liệu mới nhất. |
| **5** | **Mở thẻ Tùy chọn thông báo** | Nhấp mở thẻ thu gọn <img src="https://api.iconify.design/lucide:mail.svg?color=%23ff3333" width="16" alt="" /> **Tùy chọn thông báo**. Giao diện hiển thị danh sách 6 công tắc cài đặt nhận email từ hệ thống. |
| **6** | **Tùy biến 6 kênh thông báo qua Email** | Bạn có thể linh hoạt bật hoặc tắt bất kỳ danh mục email nào tùy theo nhu cầu công việc:<br>• **1. Thông báo tài khoản & hệ thống (`accountSystem`)**: Nhận email cảnh báo đăng nhập lạ, thay đổi mật khẩu và cập nhật trạng thái bảo mật.<br>• **2. Hóa đơn & thanh toán (`billing`)**: Nhận email thông báo xác nhận thanh toán, biên lai mua R-Point và hóa đơn gói dịch vụ.<br>• **3. Tính năng mới & cập nhật (`newFeature`)**: Nhận email giới thiệu các bản cập nhật tính năng mới trên nền tảng RedAI.<br>• **4. Chương trình đối tác & hoa hồng (`affiliate`)**: Nhận email đối soát doanh số đối tác, biến động hoa hồng kinh doanh và chính sách thưởng đại lý.<br>• **5. Tài liệu hướng dẫn & mẹo sử dụng (`documentation`)**: Nhận email tổng hợp cẩm nang sử dụng, bài viết hướng dẫn chuyên sâu và mẹo tối ưu quy trình AI.<br>• **6. Khuyến mãi & ưu đãi đặc biệt (`promotional`)**: Nhận các bản tin khuyến mãi, mã giảm giá Voucher và sự kiện tri ân khách hàng.<br>• **Cơ chế Tự động lưu tức thì (Auto-Save)**: Mỗi khi bạn gạt công tắc chuyển trạng thái Bật/Tắt, hệ thống sẽ tự động gọi API lưu cấu hình ngay lập tức và hiển thị thông báo nổi xanh *"Cập nhật tùy chọn thông báo thành công"* mà không cần bấm thêm nút Lưu. |

---

## Kiểm tra kết quả

Sau khi khám phá ký ức AI, xem nhật ký thiết bị và cấu hình thông báo, bạn có thể kiểm chứng kết quả trực quan trên hệ thống:

1. **Trên Đồ thị Ký ức AI**: Toàn bộ mạng lưới nút ký ức của bạn hiển thị sắc nét trong không gian 3D, khi bạn chat với AI Agent trong Không gian làm việc, AI sẽ chủ động xưng hô, ghi nhớ ngữ cảnh và sở thích đã được hiển thị trên đồ thị.
2. **Trên bảng Nhật ký thiết bị**: Mỗi lần bạn đổi mật khẩu, đăng nhập lại hoặc nhập mã OTP, một dòng nhật ký mới xuất hiện ngay trên đầu bảng với trạng thái `SUCCESS` và địa chỉ IP chính xác.
3. **Trên hòm thư Email**: Khi tắt công tắc nào trong Tùy chọn thông báo, hệ thống sẽ hoàn toàn ngừng gửi các email tiếp thị hoặc khuyến mãi thuộc danh mục đó, chỉ giữ lại các email bảo mật quan trọng mà bạn cho phép.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

Để trợ lý ảo AI Agent có thể tra cứu đồ thị ký ức người dùng, đọc nhật ký đăng nhập thiết bị hoặc hỗ trợ bật/tắt các tùy chọn thông báo, bạn cần trang bị Kỹ năng (Skill) sau cho Agent:

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
| **Tra cứu danh sách Ký ức người dùng** | `getUserMemories` | `Hãy kiểm tra xem trong bộ nhớ của bạn hiện đang ghi nhớ những thói quen, sở thích và thông tin cá nhân gì về tôi.` |
| **Kích hoạt Tổng hợp Ký ức Đồ thị** | `consolidateUserMemoryGraph` | `Hãy tổng hợp lại toàn bộ ký ức người dùng từ các phiên trò chuyện gần đây của tôi vào Đồ thị Tri thức.` |
| **Đọc Nhật ký xác thực và Đăng nhập** | `getAuthVerificationLogs` | `Hãy tra cứu 10 lần đăng nhập gần nhất của tài khoản tôi xem có địa chỉ IP hoặc trình duyệt lạ nào không.` |
| **Kiểm tra Cài đặt nhận thông báo hiện tại** | `getUserNotificationSettings` | `Hãy kiểm tra xem hiện tại tài khoản của tôi đang bật nhận những loại email thông báo nào.` |
| **Cập nhật Tùy chọn nhận thông báo qua Email** | `updateUserNotificationSettings` | `Tôi không muốn nhận email khuyến mại nữa, hãy tắt "receivePromotionalEmails" và bật nhận email hóa đơn "receiveBillingEmails" giúp tôi.` |

---

### Bảng kiểm tra chéo 2 chiều (UI $\leftrightarrow$ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Mở Đồ thị Ký ức và bấm Đồng bộ Ký ức | Gọi `getUserMemories` thấy danh sách các sự thật và node tri thức cá nhân được cập nhật thêm. |
| Gạt công tắc tắt nhận email khuyến mại trên giao diện | Gọi `getUserNotificationSettings` thấy `receivePromotionalEmails` trả về giá trị `false`. |
| Đăng nhập tài khoản trên thiết bị mới | Gọi `getAuthVerificationLogs` thấy xuất hiện thêm 1 bản ghi mới với IP và User-Agent tương ứng. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent gọi `updateUserNotificationSettings` đổi cờ email | Mở thẻ Tùy chọn thông báo trên trang Profile, công tắc tương ứng tự động đổi trạng thái sang Bật/Tắt mà không cần thao tác tay. |
| Agent gọi `consolidateUserMemoryGraph` | Mở hộp thoại Khám phá Đồ thị Ký ức, các node ký ức mới xuất hiện trên không gian 3D. |
