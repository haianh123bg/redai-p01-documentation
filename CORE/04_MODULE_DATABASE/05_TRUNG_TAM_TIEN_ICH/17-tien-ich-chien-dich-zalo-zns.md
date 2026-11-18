## Tổng quan Tiện ích Tạo chiến dịch Zalo ZNS Chăm sóc khách hàng

Tiện ích **Tạo chiến dịch Zalo ZNS Chăm sóc khách hàng** là kênh giao tiếp chính thức giữa doanh nghiệp với khách hàng qua nền tảng Zalo Official Account (OA). Tiện ích kết nối Bảng Động với kho mẫu ZNS (Zalo Notification Service) đã được Ban quản trị Zalo phê duyệt, tự động bóc tách các tham số động trên mẫu (Họ tên, Mã đơn, Số tiền, Thời gian giao hàng), ánh xạ chính xác với các cột dữ liệu trong bảng và gửi thông báo dịch vụ chuẩn mực với tích xanh uy tín của thương hiệu.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Khai báo định danh & OA gửi** | • **Tiêu đề chiến dịch:** | Nhập tên định danh chiến dịch (ví dụ: `Thông báo xác nhận đơn hàng Tháng 11`). |
| | • **Bảng dữ liệu & Dạng xem:** | Xác nhận bảng dữ liệu và View lọc tệp khách hàng cần gửi ZNS. |
| | • **Cột số điện thoại (Phone Field):** | Chọn cột chứa số di động của người nhận. |
| | • <img src="https://api.iconify.design/lucide:building-2.svg?color=%23ff3333" width="16" alt="" /> **Chọn tài khoản Zalo OA:** | Mở hộp thoại danh sách các trang Zalo Official Account chính thức của doanh nghiệp đã liên kết trong hệ thống. |
| **2. Chọn mẫu ZNS kiểm duyệt** | • <img src="https://api.iconify.design/lucide:layout-template.svg?color=%23ff3333" width="16" alt="" /> **Chọn mẫu ZNS:** | Hiển thị kho mẫu ZNS đã đăng ký thành công với Zalo, phân loại theo mục đích: *Xác nhận đơn hàng*, *Trạng thái vận chuyển*, *Nhắc thanh toán*, *Xác nhận lịch hẹn*. |
| | • **Xem trước mẫu ZNS:** | Quan sát cấu trúc trực quan của mẫu tin nhắn ZNS, bao gồm tiêu đề, các trường dữ liệu và nút bấm hành động (CTA). |
| **3. Tự động bóc tách và Ánh xạ tham số ZNS** | • **Danh sách tham số bắt buộc:** | Hệ thống tự động phân tích cấu trúc mẫu và liệt kê toàn bộ các tham số `<param>` (ví dụ: `<customer_name>`, `<order_code>`, `<amount>`, `<tracking_link>`). |
| | • **Khớp nối cột Bảng Động:** | Mỗi tham số cho phép chọn một cột tương ứng trong bảng:<br>&nbsp;&nbsp;+ `<customer_name>` $\rightarrow$ Cột `Họ và tên`.<br>&nbsp;&nbsp;+ `<order_code>` $\rightarrow$ Cột `Mã đơn hàng`.<br>&nbsp;&nbsp;+ `<amount>` $\rightarrow$ Cột `Tổng tiền thanh toán`.<br>Hỗ trợ nhập giá trị cố định nếu tham số mang nội dung bất biến. |
| **4. Lên lịch phát tin & Đối soát chi phí** | • **Gửi ngay lập tức:** | Kích hoạt gửi tin ZNS ngay sau khi bấm xác nhận. |
| | • **Hẹn giờ phát tin:** | Lên lịch gửi tin theo ca làm việc qua bộ chọn lịch tương tác. |
| | • <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Danh sách chiến dịch ZNS:** | Mở bảng theo dõi lịch sử gửi tin, kiểm tra số lượng tin nhắn thành công, tin nhắn thất bại và chi phí đã trừ trong tài khoản Zalo Cloud Account. |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Tạo chiến dịch Zalo ZNS]
                  │
                  ▼
[Chọn Tài khoản Zalo OA & Mẫu ZNS đã kiểm duyệt]
                  │
                  ▼
[Hệ thống tự động bóc tách danh sách tham số <param>]
                  │
                  ▼
[Ánh xạ từng tham số ZNS với các Cột tương ứng trong bảng]
                  │
                  ▼
[Chọn Gửi ngay HOẶC Hẹn giờ phát tin]
                  │
                  ▼
[Bấm "Tạo chiến dịch" ➔ Zalo OA gửi thông báo có tích xanh]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:message-circle.svg?color=%23ff3333" width="16" alt="" /> **Tạo chiến dịch Zalo ZNS**. |
| **2** | **Chọn OA và mẫu ZNS** | Nhấp **Chọn tài khoản Zalo OA**, chọn trang OA của công ty, sau đó bấm **Chọn mẫu ZNS** để chọn mẫu thông báo đơn hàng. |
| **3** | **Khớp nối tham số** | Quan sát bảng tham số: chọn cột `Họ và tên` điền vào `<customer_name>`, chọn cột `Mã đơn` điền vào `<order_code>`, chọn cột `Số tiền` điền vào `<amount>`. |
| **4** | **Phát động chiến dịch** | Chọn gửi ngay $\rightarrow$ Nhấp nút **Tạo chiến dịch**. Hệ thống gọi API Zalo ZNS và thông báo kết quả tức thời. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Tin nhắn hiển thị trên Zalo khách hàng** | Khách hàng nhận được tin nhắn từ Zalo OA có logo và tích xanh xác thực, các trường thông tin đơn hàng hiển thị chính xác theo bảng tính. |
| **Đối soát báo cáo chiến dịch** | Trong bảng lịch sử ZNS, chiến dịch hiển thị tỷ lệ gửi thành công đạt mức tối đa và số dư tài khoản ZCA được cập nhật tương ứng. |

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
| **Truy vấn dữ liệu đơn hàng để chuẩn bị tham số ZNS** | `listRecords`, `getRecord` | *"Hãy đọc danh sách 10 đơn hàng có trạng thái 'Đã thanh toán' trong bảng 'Đơn Hàng', lấy Họ tên khách, Mã đơn và Tổng tiền để chuẩn bị dữ liệu gửi Zalo ZNS."* |
| **Ghi nhận trạng thái gửi ZNS vào Bảng Động** | `updateRecords` | *"Hãy cập nhật cột 'Trạng thái ZNS' thành 'Đã gửi' cho các bản ghi đơn hàng vừa được xử lý thành công."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Phát động gửi ZNS trên giao diện | Gọi `listRecords` thấy các giá trị cột đơn hàng hoàn toàn trùng khớp với nội dung ZNS hiển thị tới khách hàng. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent kiểm tra dữ liệu tham số | Người dùng mở giao diện Chiến dịch ZNS trên UI, các ô ánh xạ hiển thị đúng các trường dữ liệu mà Agent đã xác nhận. |
