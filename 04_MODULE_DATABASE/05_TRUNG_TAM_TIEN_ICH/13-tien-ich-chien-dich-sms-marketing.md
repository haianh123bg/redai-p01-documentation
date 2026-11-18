## Tổng quan Tiện ích Chiến dịch SMS Marketing & Chăm sóc khách hàng

Tiện ích **Chiến dịch SMS Marketing & Chăm sóc khách hàng** là công cụ kết nối viễn thông trực tiếp từ **RedAI Database**, cho phép phát động các đợt gửi tin nhắn SMS thương hiệu (Brandname) hàng loạt tới danh bạ khách hàng lưu trong bảng. Tiện ích hỗ trợ quản lý Brandname FPT/Viettel, tự động phân tích độ dài ký tự GSM-7 và Unicode tiếng Việt có dấu theo chuẩn tính cước nhà mạng, tự động trộn biến cá nhân hóa `{placeholder}`, thiết lập khoảng trễ an toàn và xem trước trực tiếp dữ liệu trước khi phát động.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Khai báo định danh chiến dịch** | • **Tên chiến dịch:** | Ô nhập văn bản bắt buộc (ví dụ: `Thông báo bảo trì hệ thống tháng 11/2026`). |
| | • **Mô tả chiến dịch:** | Ghi chú mục đích chiến dịch phục vụ quản lý nội bộ. |
| | • **Loại chiến dịch (Campaign Type):** | Chọn giữa 2 hình thức:<br>• `Chăm sóc khách hàng (CUSTOMER_CARE)`: Dành cho thông báo dịch vụ, mã xác thực, nhắc lịch hẹn (ưu tiên tốc độ và độ tin cậy viễn thông cao nhất).<br>• `Quảng cáo (ADS)`: Dành cho chương trình khuyến mãi, ưu đãi bán hàng. |
| **2. Bảng dữ liệu nguồn & Bộ lọc** | • **Bảng dữ liệu & Dạng xem:** | Xác nhận bảng nguồn và View lọc sẵn (ví dụ: View `Khách hàng VIP`). Hỗ trợ chọn toàn bộ bảng hoặc chỉ áp dụng bộ lọc của View. |
| | • **Cột số điện thoại (Phone Field):** | Hệ thống tự nhận diện cột kiểu `Phone` hoặc tên cột chứa `SĐT`/`Điện thoại`. Tự động chuẩn hóa đầu số hợp lệ. |
| | • **Giới hạn số lượng (Limit):** | Nhập số lượng người nhận tối đa cho chiến dịch (mặc định: `10.000` số). |
| **3. Cấu hình Brandname viễn thông** | • **Danh sách Brandname FPT/Viettel:** | Menu thả xuống liệt kê các Brandname đã được kết nối và cấp phép sử dụng. |
| | • **Brandname tùy biến (`__CUSTOM__`):** | Cho phép nhập trực tiếp tên thương hiệu riêng nếu sử dụng tài khoản tích hợp viễn thông độc lập. |
| **4. Soạn nội dung & Đo lường độ dài ký tự** | • **Chế độ nội dung:** | Tùy chọn `Chọn Mẫu SMS có sẵn` (từ danh sách mẫu đã được nhà mạng phê duyệt) hoặc `Tự soạn nội dung trực tiếp`. |
| | • **Thước đo ký tự & Số trang SMS thời gian thực:** | Hệ thống tự động đếm ký tự và tính toán số lượng trang tin viễn thông:<br>• *Không dấu (GSM-7):* Tối đa 160 ký tự = 1 SMS; từ 161 ký tự trở lên tính 153 ký tự/SMS.<br>• *Có dấu tiếng Việt (Unicode):* Tối đa 70 ký tự = 1 SMS; từ 71 ký tự trở lên tính 67 ký tự/SMS.<br>Cảnh báo trực quan hiển thị ngay dưới ô soạn thảo: *"Tin nhắn có dấu (Unicode) - Chi phí tính theo 67 ký tự/SMS"*. |
| **5. Bảng ánh xạ biến trộn dữ liệu** | **Ghép nối biến mẫu với cột dữ liệu** | Tự động bóc tách các biến `{ten_bien}` hoặc `{{ten_bien}}` trong nội dung. Mỗi biến cho phép chọn:<br>• `Biến động (Dynamic)`: Chọn cột dữ liệu trong Bảng Động (ví dụ: `{Ho_Ten}` $\rightarrow$ Cột `Họ và tên`, `{Ma_Don}` $\rightarrow$ Cột `Mã đơn hàng`).<br>• `Giá trị tĩnh (Static)`: Điền giá trị cố định cho toàn bộ người nhận. |
| **6. Giãn cách an toàn & Lên lịch gửi** | • **Khoảng trễ ngẫu nhiên (Delay):** | Thiết lập thời gian chờ từ `1` đến `3` giây giữa các tin nhắn để bảo vệ cổng truyền tải viễn thông. |
| | • **Lên lịch hẹn giờ gửi tin:** | Bật công tắc `Hẹn giờ gửi` và chọn Ngày/Giờ phát tin chính xác qua bộ chọn lịch tương tác (`DateTimePicker`). |
| **7. Xem trước dữ liệu (Live Preview)** | <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Xem trước dữ liệu trích xuất** | Truy vấn thử 5 bản ghi thực tế, hiển thị số điện thoại và nội dung sau khi trộn biến để đối soát trước khi gửi. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Chiến dịch SMS]
              │
              ▼
[Nhập Tên chiến dịch & Chọn Loại (CSKH / Quảng cáo)]
              │
              ▼
[Chọn Brandname & Cột Số điện thoại nguồn]
              │
              ▼
[Soạn nội dung SMS / Chọn Mẫu ➔ Kiểm tra Thước đo ký tự GSM/Unicode]
              │
              ▼
[Ánh xạ các Biến trộn dữ liệu {placeholder} vào các Cột trong bảng]
              │
              ▼
[Cấu hình Giãn cách Delay & Chọn Hẹn giờ gửi nếu cần]
              │
              ▼
[Bấm "Xem trước dữ liệu trích xuất" để kiểm tra 5 bản ghi mẫu]
              │
              ▼
[Bấm "Phát động chiến dịch" ➔ Hệ thống kích hoạt gửi tin]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:message-square.svg?color=%23ff3333" width="16" alt="" /> **Chiến dịch SMS**. |
| **2** | **Khai báo thông tin** | Nhập tên chiến dịch, chọn loại *Chăm sóc khách hàng*, chọn Brandname và chỉ định cột Số điện thoại. |
| **3** | **Soạn thảo và trộn biến** | Nhập nội dung tin nhắn, chèn biến `{Ho_Ten}`, quan sát thước đo ký tự để kiểm soát số trang SMS không vượt quá dự toán. |
| **4** | **Ánh xạ cột** | Tại bảng ánh xạ, chọn cột `Họ và tên` khớp với biến `{Ho_Ten}`. |
| **5** | **Xem trước & Phát động** | Bấm nút **Xem trước dữ liệu trích xuất**. Khi thấy nội dung đã khớp nối hoàn hảo với số điện thoại thực tế, bấm **Phát động chiến dịch**. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Trạng thái chiến dịch** | Nút <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Lịch sử chiến dịch SMS** hiển thị chiến dịch vừa tạo ở trạng thái `PROCESSING` hoặc `COMPLETED`. |
| **Nhận tin nhắn trên thiết bị** | Số điện thoại nhận tin hiển thị đúng tên Brandname thương hiệu, nội dung tin nhắn hiển thị đúng họ tên và thông số cá nhân hóa. |

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
| **Lọc danh sách số điện thoại chuẩn bị gửi SMS** | `listRecords`, `countRecords` | *"Hãy truy vấn bảng 'Đơn Hàng', đếm số lượng khách hàng có trạng thái 'Chờ giao hàng' và lấy danh sách Họ tên cùng Số điện thoại để chuẩn bị gửi tin nhắn SMS thông báo."* |
| **Kiểm tra độ dài ký tự và nội dung tin nhắn** | `listRecords` | *"Hãy kiểm tra xem cột 'Nội dung tin nhắn' trong bảng 'Chiến Dịch' có bản ghi nào vượt quá 160 ký tự không dấu hoặc 70 ký tự có dấu không."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Phát động chiến dịch SMS trên giao diện | Gọi `listRecords` kiểm tra thấy danh sách số điện thoại trong View hoàn toàn trùng khớp với danh sách người nhận của chiến dịch. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent lọc danh sách gửi SMS | Người dùng mở biểu mẫu Chiến dịch SMS trên UI, số lượng người nhận hiển thị đúng tệp mà Agent đã thống kê. |
