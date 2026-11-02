## Tổng quan Tiện ích Tạo chiến dịch Zalo Personal từ Bảng Động

Tiện ích **Tạo chiến dịch Zalo Personal từ Bảng Động** là công cụ gửi tin nhắn chăm sóc khách hàng và bán hàng tự động trực tiếp từ tài khoản Zalo cá nhân của chuyên viên tư vấn. Tiện ích đọc danh sách số điện thoại trong bảng tính, tự động gửi chuỗi tin nhắn đa phương tiện (văn bản cá nhân hóa, hình ảnh sản phẩm và liên kết tài liệu), đồng thời tích hợp cơ chế giãn cách an toàn thông minh (Random Delay) giúp bảo vệ tài khoản Zalo vĩnh viễn không bị thuật toán đánh dấu vi phạm spam.

---

## Chi tiết các trường và thành phần điều khiển trên giao diện

| Phân khu | Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- | :--- |
| **1. Khai báo định danh & Tài khoản gửi** | • **Tiêu đề chiến dịch:** | Nhập tên định danh chiến dịch (ví dụ: `CSKH Zalo Cá Nhân - Gửi Lịch Hẹn Tư Vấn`). |
| | • **Bảng dữ liệu & Dạng xem:** | Xác nhận bảng tính và View lọc khách hàng mục tiêu. |
| | • **Cột số điện thoại (Phone Field):** | Chọn cột chứa số di động của khách hàng. Hệ thống tự động lọc đầu số chuẩn Việt Nam. |
| | • <img src="https://api.iconify.design/lucide:user-check.svg?color=%23ff3333" width="16" alt="" /> **Chọn tài khoản Zalo thực thi:** | Mở hộp thoại danh sách tài khoản Zalo cá nhân đã quét mã QR liên kết, hiển thị ảnh đại diện, tên Zalo và trạng thái kết nối phiên làm việc. |
| **2. Thiết kế kịch bản tin nhắn đa hành động (Action Sequence)** | • **Hành động 1 — Tin nhắn văn bản:** | Soạn nội dung tin nhắn chào hỏi, hỗ trợ chèn biến động `{Ho_Ten}`, `{Ma_Don_Hang}` lấy từ bảng tính. |
| | • **Hành động 2 — Gửi hình ảnh đính kèm:** | Đính kèm ảnh banner khuyến mãi hoặc ảnh chụp mẫu sản phẩm thực tế. |
| | • **Hành động 3 — Gửi đường dẫn liên kết:** | Đính kèm link website hoặc link tải tài liệu hướng dẫn. |
| | • **Giãn cách giữa các hành động:** | Cấu hình độ trễ 3–5 giây giữa tin 1, tin 2 và tin 3 để mô phỏng tự nhiên thao tác gõ phím của con người. |
| **3. Chính sách an toàn chống khóa tài khoản (Safety Policy)** | • **Khoảng trễ ngẫu nhiên (Random Delay):** | Thiết lập thời gian chờ ngẫu nhiên giữa 2 khách hàng từ `10` đến `30` giây (hoặc 30–60 giây đối với tệp danh bạ lớn). |
| | • **Giới hạn số tin mỗi ngày (Daily Quota):** | Khuyến nghị đặt tối đa 50–100 tin nhắn/ngày cho mỗi tài khoản Zalo cá nhân để tuân thủ ngưỡng an toàn của nền tảng Zalo. |
| | • <img src="https://api.iconify.design/lucide:shield-alert.svg?color=%23ff3333" width="16" alt="" /> **Chính sách an toàn Zalo:** | Hộp thoại cảnh báo các nguyên tắc gửi tin nhắn không bị người dùng báo cáo vi phạm. |
| **4. Xem trước & Nhật ký lỗi tài khoản (Error Logs)** | • <img src="https://api.iconify.design/lucide:eye.svg?color=%23ff3333" width="16" alt="" /> **Xem trước người nhận:** | Hiển thị danh sách khách hàng thực tế sau khi áp dụng các bộ lọc của View. |
| | • <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **Nhật ký lỗi tài khoản:** | Tra cứu chi tiết các lý do gửi tin không thành công (ví dụ: *Số điện thoại chưa tạo tài khoản Zalo*, *Người nhận cài đặt chặn tin nhắn từ người lạ*). |

---

## Các bước thao tác tuần tự trên giao diện UI

```text
[Mở Tiện ích Tạo chiến dịch Zalo Personal]
                    │
                    ▼
[Chọn Tài khoản Zalo cá nhân liên kết & Cột Số điện thoại]
                    │
                    ▼
[Soạn Kịch bản tin nhắn đa hành động: Text ➔ Ảnh ➔ Link]
                    │
                    ▼
[Cấu hình Giãn cách ngẫu nhiên 10-30s & Giới hạn tin/ngày]
                    │
                    ▼
[Bấm "Xem trước người nhận" để kiểm tra danh sách]
                    │
                    ▼
[Bấm "Tạo chiến dịch" ➔ Tiến trình tự động gửi tin nhắn]
```

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:message-square.svg?color=%23ff3333" width="16" alt="" /> **Tạo chiến dịch Zalo Personal**. |
| **2** | **Chọn tài khoản và danh bạ** | Nhấp nút **Chọn tài khoản Zalo thực thi**, chọn tài khoản nhân viên phụ trách và chọn cột Số điện thoại trong Bảng Động. |
| **3** | **Soạn kịch bản chuỗi tin** | Thêm hành động 1 (soạn tin chào hỏi chèn biến `{Ho_Ten}`), thêm hành động 2 (chọn ảnh sản phẩm đính kèm). |
| **4** | **Thiết lập giãn cách an toàn** | Cài đặt Random Delay từ 15 đến 30 giây, giới hạn tối đa 50 tin nhắn cho đợt gửi này. |
| **5** | **Khởi chạy chiến dịch** | Bấm nút **Xem trước người nhận** để kiểm tra $\rightarrow$ Nhấp nút **Tạo chiến dịch** để hệ thống chạy tiến trình gửi tin tự động ngoài nền. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Ứng dụng Zalo trên điện thoại** | Mở ứng dụng Zalo của tài khoản gửi: các tin nhắn kèm hình ảnh hiển thị trong khung chat của khách hàng tuần tự theo đúng thời gian giãn cách. |
| **Báo cáo trạng thái chiến dịch** | Mở <img src="https://api.iconify.design/lucide:list.svg?color=%23ff3333" width="16" alt="" /> **Danh sách chiến dịch Zalo Personal**, các dòng gửi thành công chuyển sang màu xanh, hiển thị tỷ lệ phản hồi của khách hàng. |

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
| **Lọc danh bạ số điện thoại gửi tin nhắn Zalo cá nhân** | `listRecords` | *"Hãy truy vấn bảng 'Khách Hàng', lọc danh sách 30 khách hàng có trạng thái 'Hẹn gặp hôm nay', lấy Số điện thoại và Họ tên để chuẩn bị gửi tin nhắn Zalo nhắc lịch."* |
| **Ghi nhận lịch sử gửi Zalo vào Bảng Động** | `updateRecords` | *"Hãy cập nhật cột 'Kênh đã liên hệ' thành 'Zalo Personal' cho danh sách các khách hàng vừa được gửi tin nhắn."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Phát động chiến dịch Zalo Personal trên giao diện | Gọi `listRecords` thấy số điện thoại trong View trùng khớp với tệp người nhận được đưa vào hàng đợi gửi tin. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent lọc danh sách gửi tin | Người dùng mở biểu mẫu Zalo Personal trên UI, số lượng khách hàng hiển thị đúng theo thống kê của Agent. |
