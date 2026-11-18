## Tổng quan Tiện ích Chiến dịch Email Marketing User hệ thống (30+ Phân khúc)

Tiện ích **Chiến dịch Email Marketing User hệ thống** là công cụ tiếp thị phân khúc chuyên sâu cấp quản trị trên **RedAI Database**. Khác với các chiến dịch thông thường lấy danh bạ từ bảng tính, tiện ích này kết nối trực tiếp vào cơ sở dữ liệu người dùng toàn hệ thống (System Users) với bộ lọc đa tầng hơn 30 tiêu chí (xác thực KYC, tình trạng nạp tiền, hạn gói dịch vụ, số dư R-Point, hành vi sử dụng tính năng và sinh nhật), cho phép doanh nghiệp cá nhân hóa thông điệp tiếp thị và tối ưu hóa tỷ lệ chuyển đổi cho từng nhóm khách hàng mục tiêu.

---

## Chi tiết các tiêu chí phân khúc chuyên sâu trên giao diện

| Nhóm phân khúc | Tiêu chí lọc chi tiết | Giá trị lựa chọn & Quy tắc nghiệp vụ |
| :--- | :--- | :--- |
| **1. Định danh & Mức độ tin cậy (KYC)** | • **Trạng thái tài khoản:** | `Tất cả`, `Đang hoạt động (Active)` hoặc `Đã khóa`. |
| | • **Xác thực Email / SĐT:** | Bật công tắc lọc chỉ những tài khoản đã xác thực hòm thư hoặc số điện thoại qua mã OTP. |
| | • **Cấp độ tin cậy danh tính (Trust Level):** | `Chưa xác thực (UNVERIFIED)`, `Xác thực cơ bản (BASIC_VERIFIED)` hoặc `Xác thực toàn diện (FULL_VERIFIED)`. |
| **2. Phân loại tài khoản & Gói thuê bao** | • **Loại đối tượng:** | `Cá nhân (INDIVIDUAL)` hoặc `Doanh nghiệp (BUSINESS)`. |
| | • **Trạng thái thanh toán:** | `Đã trả phí (PAID)` hoặc `Dùng miễn phí (FREE)`. |
| | • **Gói dịch vụ kích hoạt:** | Chọn gói cụ thể trong danh mục thuê bao (ví dụ: Gói Pro, Gói Enterprise). |
| | • **Trạng thái thuê bao:** | `Đang hiệu lực (ACTIVE)`, `Hủy gia hạn vào cuối kỳ (CANCEL_AT_PERIOD_END)`, `Quá hạn thanh toán (PAST_DUE)`, `Đã hết hạn (EXPIRED)`. |
| | • **Chu kỳ thanh toán:** | `Hàng tuần`, `Hàng tháng`, `Hàng quý`, `6 tháng`, `Hàng năm`. |
| **3. Cảnh báo thời hạn gói thuê bao** | **Bộ lọc đếm ngược ngày hết hạn** | Menu chọn mốc thời gian đặc biệt phục vụ chiến dịch giữ chân khách hàng:<br>• `Sắp hết hạn trong 7 ngày`<br>• `Sắp hết hạn trong 15 ngày`<br>• `Sắp hết hạn trong 16–30 ngày`<br>• `Đã hết hạn (Expired)`. |
| **4. Tài chính, Điểm thưởng & Chi tiêu** | • **Khoảng số dư R-Point:** | Nhập số dư tối thiểu và tối đa (ví dụ: từ 0 đến 50 R-Point) để nhắc người dùng sử dụng điểm tích lũy. |
| | • **Khoảng tổng tiền đã chi tiêu:** | Lọc khách hàng theo tổng giá trị thanh toán tích lũy (ví dụ: trên 10 triệu đồng để chăm sóc tệp VIP). |
| | • **Số ngày kể từ lần thanh toán cuối:** | Lọc khách hàng đã quá hạn lâu ngày chưa phát sinh giao dịch mới. |
| **5. Hành vi hoạt động & Kích hoạt tính năng** | • **Số ngày chưa đăng nhập:** | Tìm người dùng không truy cập hệ thống trong 15, 30 hoặc 60 ngày để gửi thư mời quay lại. |
| | • **Đã đổi mật khẩu lần đầu:** | Lọc tài khoản chưa từng đổi mật khẩu để gửi hướng dẫn bảo mật tài khoản. |
| | • **Đã tạo AI Agent chưa:** | Lọc người dùng chưa từng tạo trợ lý ảo để gửi email hướng dẫn tính năng ban đầu. |
| | • **Đã kết nối kênh chat chưa:** | Lọc người dùng chưa tích hợp Zalo/Fanpage để hỗ trợ kỹ thuật kết nối. |
| | • **Sinh nhật trong tháng:** | Chọn tháng sinh (từ tháng 1 đến 12) để tự động gửi thư chúc mừng và mã quà tặng tri ân. |
| **6. Kênh tiếp cận & Tiếp thị liên kết** | • **Kênh tiếp cận nguồn:** | Tiếp thị liên kết (Affiliate), Chiến dịch quảng cáo (UTM), Tự nhiên (Organic), Nội bộ. |
| | • **Hợp đồng Affiliate:** | `Đã ký hợp đồng điện tử`, `Chưa ký` hoặc `Không tham gia`. |
| | • **Thẻ người dùng (User Tag):** | Lọc theo thẻ tùy biến đã gán trong phân hệ Quản trị User. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Chiến dịch Email Marketing User hệ thống]
                          │
                          ▼
[Thiết lập Bộ lọc Phân khúc nâng cao (30+ tiêu chí lọc sâu)]
                          │
                          ▼
[Kiểm tra Bảng Xem trước danh sách Người dùng đạt chuẩn]
                          │
                          ▼
[Chọn Mẫu Email HTML ➔ Ánh xạ biến Họ tên, Gói, Hạn dùng]
                          │
                          ▼
[Tích chọn Máy chủ gửi thư xoay vòng & Thiết lập Hạn ngạch]
                          │
                          ▼
[Chọn Gửi ngay HOẶC Lên lịch phát thư ➔ Bấm "Tạo chiến dịch"]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:mail-plus.svg?color=%23ff3333" width="16" alt="" /> **Chiến dịch Email Marketing User hệ thống**. |
| **2** | **Phân khúc người nhận** | Thiết lập các tiêu chí lọc: ví dụ chọn đối tượng *Doanh nghiệp*, gói dịch vụ *Pro*, và chọn *Sắp hết hạn trong 7 ngày*. |
| **3** | **Xem trước đối tượng** | Khung xem trước hiển thị chính xác danh sách các tài khoản thỏa mãn tiêu chí cùng tổng số lượng người nhận thực tế. |
| **4** | **Chọn mẫu email & Cấu hình** | Chọn mẫu thư nhắc gia hạn, khớp nối các biến tên người dùng và hạn dùng, chọn máy chủ gửi thư xoay vòng. |
| **5** | **Khởi chạy chiến dịch** | Kiểm tra hạn ngạch an toàn $\rightarrow$ Nhấp nút **Tạo chiến dịch** để hệ thống tự động phát động tiến trình gửi thư hàng loạt. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Tỷ lệ gửi thư thành công** | Mở bảng theo dõi chiến dịch, toàn bộ email gửi tới đúng nhóm người dùng mục tiêu, không gửi nhầm sang tệp đối tượng khác. |
| **Hiệu quả kích hoạt** | Người dùng nhận được thư nhắc gia hạn hoặc mã quà tặng đúng thời điểm, tỷ lệ nhấp liên kết và gia hạn gói tăng trưởng rõ rệt. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Tài khoản có quyền quản trị người dùng hệ thống (`UTILITY_CAMPAIGN_EMAIL_MARKETING_USER`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Thống kê người dùng theo tiêu chí gói thuê bao** | `countRecords`, `listRecords` | *"Hãy thống kê số lượng tài khoản người dùng có gói thuê bao sắp hết hạn trong 7 ngày tới và trích xuất danh sách email đại diện."* |
| **Lọc người dùng theo ngày sinh nhật trong tháng** | `listRecords` | *"Hãy tìm tất cả người dùng có sinh nhật trong tháng 11 để chuẩn bị danh sách gửi email chúc mừng và tặng điểm R-Point."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Thiết lập bộ lọc trên giao diện | Số lượng người dùng hiển thị trong khung Preview trùng khớp với kết quả đếm của Agent qua các trường lọc. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent kiểm tra tệp người dùng hệ thống | Người dùng mở giao diện Chiến dịch Email User hệ thống, con số thống kê đối tượng hiển thị đồng bộ. |
