## Tổng quan Tiện ích Tạo chiến dịch Email Marketing từ Bảng Động

Tiện ích **Tạo chiến dịch Email Marketing từ Bảng Động** là công cụ gửi thư điện tử quy mô lớn chuyên nghiệp trên **RedAI Database**. Tiện ích kết nối trực tiếp dữ liệu danh bạ bảng tính với hệ thống máy chủ gửi thư doanh nghiệp (hỗ trợ xoay vòng đa máy chủ SMTP, Amazon SES, SendGrid), cho phép chèn biến dữ liệu cá nhân hóa, thiết lập hạn ngạch an toàn chống rơi vào thư rác (Spam) và kích hoạt chuỗi hành động tự động hóa phản hồi thông minh dựa trên hành vi mở thư và nhấp liên kết của khách hàng.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Khai báo định danh & Nguồn gửi** | • **Tiêu đề chiến dịch:** | Tên định danh chiến dịch (ví dụ: `Bản tin Tri ân Khách Hàng Tháng 11`). |
| | • **Bảng nguồn & Dạng xem:** | Xác nhận bảng dữ liệu và View lọc sẵn khách hàng nhận thư. |
| | • **Cột Email (Email Field):** | Chọn cột chứa hòm thư điện tử. Hệ thống tự động lọc các dòng có email hợp lệ. |
| | • **Cột Tên người nhận (Name Field):** | Chọn cột họ tên để phục vụ chào hỏi cá nhân hóa (ví dụ: *Chào anh Long*). |
| **2. Chọn mẫu Email & Ánh xạ biến** | • <img src="https://api.iconify.design/lucide:layout-template.svg?color=%23ff3333" width="16" alt="" /> **Chọn mẫu email:** | Mở thư viện mẫu thư (HTML Responsive) được thiết kế chỉn chu theo chuẩn hiển thị di động. |
| | • **Bảng ánh xạ biến mẫu (Variable Mapping):** | Khớp nối các placeholder trong mẫu `{{ten_khach}}`, `{{ma_voucher}}`, `{{ngay_het_han}}` với các cột tương ứng trong Bảng Động. |
| **3. Xoay vòng Máy chủ gửi thư (Email Server Rotation)** | • <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **Chọn máy chủ gửi thư:** | Cho phép tích chọn đồng thời nhiều tài khoản máy chủ gửi thư đã kết nối (SMTP riêng, SES, SendGrid). |
| | • **Cơ chế cân bằng tải (Load Balancing):** | Hệ thống tự động chia đều số lượng thư gửi luân phiên qua từng máy chủ, giúp tăng tốc độ truyền tải và bảo vệ độ uy tín (Reputation) của địa chỉ IP gửi thư. |
| **4. Hạn ngạch & Kiểm soát an toàn hòm thư** | • **Hạn ngạch gửi tối đa:** | Cấu hình `Số lượng gửi tối đa mỗi giờ (Max Hourly Quota)` và `Số lượng tối đa mỗi ngày (Max Daily Quota)`. |
| | • **Ngưỡng lỗi máy chủ liên tiếp (Max Server Failures):** | Tự động tạm ngắt hoặc chuyển server nếu gặp 3–5 lỗi gửi liên tiếp để bảo vệ tên miền. |
| | • **Bộ lọc danh sách chặn (Suppression List):** | Tự động loại trừ các email đã từng hủy đăng ký hoặc đánh dấu thư rác trong quá khứ. |
| | • **Đường dẫn hủy đăng ký (Unsubscribe URL):** | Chèn liên kết từ chối nhận thư để tuân thủ quy định phòng chống spam quốc tế. |
| **5. Chuỗi hành động tự động hóa phản hồi (Campaign Actions)** | • **Khi người nhận mở email:** | Tự động cập nhật cột `Trạng thái chăm sóc` thành `Đã quan tâm` trong Bảng Động. |
| | • **Khi người nhận bấm nút kêu gọi hành động (CTA):** | Tự động gán thẻ `Khách hàng tiềm năng cao` và bắn thông báo cho chuyên viên tư vấn. |
| | • **Khi gửi email thất bại:** | Cập nhật nhãn `Email sai/không tồn tại` vào ô tính tương ứng. |
| **6. Thời gian phát động** | • **Gửi ngay lập tức:** | Kích hoạt gửi thư ngay khi hoàn tất tạo chiến dịch. |
| | • **Lên lịch hẹn giờ:** | Chọn Ngày và Giờ phát thư chính xác vào khung giờ vàng mở mail của khách hàng. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Tạo chiến dịch Email]
               │
               ▼
[Nhập Tên chiến dịch, Chọn Cột Email & Cột Tên người nhận]
               │
               ▼
[Chọn Mẫu Email HTML ➔ Ánh xạ các Biến {{placeholder}} vào Cột bảng]
               │
               ▼
[Tích chọn 1 hoặc nhiều Máy chủ gửi thư để Xoay vòng cân bằng tải]
               │
               ▼
[Thiết lập Hạn ngạch gửi/giờ, Ngưỡng lỗi liên tiếp & Link Hủy đăng ký]
               │
               ▼
[Cấu hình Chuỗi hành động tự động khi khách Mở mail hoặc Bấm link CTA]
               │
               ▼
[Chọn Gửi ngay HOẶC Lên lịch hẹn giờ ➔ Bấm "Tạo chiến dịch"]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:mail-plus.svg?color=%23ff3333" width="16" alt="" /> **Tạo chiến dịch Email**. |
| **2** | **Khai báo người nhận** | Nhập tiêu đề chiến dịch, xác nhận cột Email và cột Họ tên đại diện trong Bảng Động. |
| **3** | **Chọn mẫu & Khớp biến** | Bấm **Chọn mẫu email**, chọn mẫu thư mong muốn, sau đó khớp các biến dữ liệu tương ứng với cột trong bảng. |
| **4** | **Chọn máy chủ & An toàn** | Bấm **Chọn máy chủ gửi thư**, tích chọn các server gửi và thiết lập hạn ngạch giờ/ngày. |
| **5** | **Thêm kịch bản phản hồi** | Thêm quy tắc: nếu khách nhấp link CTA thì tự động cập nhật trạng thái ô tính trong bảng thành `Khách tiềm năng`. |
| **6** | **Khởi chạy chiến dịch** | Chọn gửi ngay hoặc hẹn giờ phát thư $\rightarrow$ Bấm nút **Tạo chiến dịch** để hệ thống tiếp nhận tiến trình. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Hộp thư đến của khách hàng** | Email gửi tới thẳng Hộp thư chính (Inbox), hiển thị đầy đủ hình ảnh, định dạng HTML và họ tên cá nhân hóa. |
| **Báo cáo thống kê chiến dịch** | Mở <img src="https://api.iconify.design/lucide:bar-chart-2.svg?color=%23ff3333" width="16" alt="" /> **Danh sách chiến dịch Email** để theo dõi tỷ lệ mở thư, tỷ lệ nhấp chuột vào link CTA theo thời gian thực. |
| **Tự động cập nhật Bảng Động** | Khi khách mở thư hoặc nhấp link, các ô tính tương ứng trong bảng tự động đổi trạng thái theo kịch bản phản hồi đã cấu hình. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Thông số cấu hình | Giá trị chính xác |
| :--- | :--- |
| **Tên Kỹ năng (Skill Name)** | `RedAI - Module - Database` |
| **Mã định danh Kỹ năng (Skill ID)** | `65f9c362-0a8b-4ce6-9ba0-d29375b4cea6` |
| **Bộ công cụ (Tool Suite)** | `RedAI - Module - Database` |
| **Mã định danh Bộ công cụ (Tool Suite ID)** | `eb8a7504-5844-4e6e-ba7f-7645f104c0af` |
| **Quyền tài khoản yêu cầu** | Đã đăng nhập tài khoản có quyền tiếp thị (`MARKETING_CREATE`) và quyền đọc bản ghi (`RECORD_READ`). |

### Bảng ánh xạ tính năng kèm Prompt mẫu tương ứng cho AI Agent

| Hành động trên Giao diện UI | Công cụ AI Agent tương ứng | Khung lệnh (Prompt) mẫu chuẩn thực thi |
| :--- | :--- | :--- |
| **Lọc danh sách email để chuẩn bị phát động chiến dịch** | `listRecords` | *"Hãy truy vấn bảng 'Khách Hàng', lọc danh sách các khách hàng có địa chỉ email hợp lệ và chưa từng nhận thư trong 30 ngày qua để chuẩn bị tệp gửi email tri ân."* |
| **Ghi nhận trạng thái phản hồi email vào Bảng Động** | `updateRecords` | *"Hãy cập nhật cột 'Trạng thái Email' thành 'Đã mở thư' cho các bản ghi khách hàng có mã 'KH-101', 'KH-102'."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Phát động chiến dịch Email trên giao diện | Gọi `listRecords` thấy số lượng bản ghi thỏa mãn bộ lọc trùng khớp với số lượng email được đưa vào hàng đợi gửi thư. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent cập nhật trạng thái phản hồi email | Người dùng mở Dạng xem bảng tính (Grid View), các ô tính hiển thị trạng thái đã mở thư đồng bộ. |
