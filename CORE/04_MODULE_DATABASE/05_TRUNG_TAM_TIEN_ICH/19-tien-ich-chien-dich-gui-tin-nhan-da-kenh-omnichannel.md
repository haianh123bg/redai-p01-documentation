## Tổng quan Tiện ích Tạo chiến dịch Gửi tin nhắn Đa kênh Tự động (Omnichannel Campaign Wizard 4 Bước)

Tiện ích **Tạo chiến dịch Gửi tin nhắn Đa kênh Tự động** là giải pháp điều phối chiến dịch tiếp thị và chăm sóc khách hàng đa nền tảng tối thượng trên **RedAI Database**. Tiện ích vận hành dưới dạng một Trình hướng dẫn trực quan 4 bước (4-Step Wizard), kết nối nguồn dữ liệu bảng tính với hệ thống OmniChat tập trung (hỗ trợ tích hợp đồng thời Zalo OA, Facebook Fanpage, Zalo cá nhân và Webchat), cho phép áp dụng chiến lược xoay vòng mẫu tin nhắn (A/B Testing), thiết lập giá trị dự phòng thông minh (Fallback Value) cho các ô tính bị rỗng và kích hoạt chuỗi hành động phản hồi khép kín (tự động bật trợ lý ảo AI Agent ngay khi khách hàng nhắn lại).

---

## Chi tiết các bước và thành phần điều khiển trong Trình hướng dẫn 4 bước

```text
┌─────────────────────────────────────────────────────────────────┐
│     TRÌNH HƯỚNG DẪN CHIẾN DỊCH GỬI TIN NHẮN ĐA KÊNH 4 BƯỚC      │
├─────────────────┬─────────────────┬────────────────┬────────────┤
│  BƯỚC 1: NGUỒN  │  BƯỚC 2: KÊNH   │ BƯỚC 3: BIẾN   │ BƯỚC 4: AN │
│    DỮ LIỆU      │   & XOAY VÒNG   │  & DỰ PHÒNG    │ TOÀN & AI  │
└─────────────────┴─────────────────┴────────────────┴────────────┘
```

---

### Bước 1 — Chọn đối tượng & Nguồn dữ liệu nhận tin

| Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- |
| **Nguồn Bảng Động (Custom Table):** | Nguồn mặc định khi mở từ Trung Tâm Tiện Ích: Đọc trực tiếp danh sách khách hàng từ bảng tính hiện tại. Hỗ trợ tích hợp bộ dựng bộ lọc chuyên sâu (`FilterBuilder`) đa điều kiện (VÀ/HOẶC) giúp người dùng khoanh vùng tệp khách hàng chính xác nhất. |
| **Nguồn Dạng xem hệ thống (System View):** | Cho phép chọn các View lọc sẵn khách hàng theo từng phân khúc định nghĩa trước trong hệ thống. |
| **Nguồn Hội thoại trực tiếp (Direct Conversations):** | Trích xuất trực tiếp từ các cuộc trò chuyện đang có trên OmniChat theo Nền tảng (Zalo OA, Fanpage, Webchat), Nhân viên phụ trách (Assignee), Trạng thái hội thoại, Thẻ nhãn, và **Số ngày chưa tương tác lại** (ví dụ: tìm các khách hàng không có tương tác trong 7 ngày gần nhất để gửi tin kích hoạt lại). |

---

### Bước 2 — Chọn kênh gửi & Chiến lược xoay vòng mẫu tin nhắn

| Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- |
| **Chọn tài khoản kênh gửi:** | Cho phép tích chọn một hoặc nhiều tài khoản kênh chat đã liên kết (Zalo OA chính thức, Fanpage Facebook, Zalo cá nhân). Hệ thống tự động phân bổ luân phiên giữa các tài khoản nếu tệp người nhận thuộc nhiều kênh khác nhau. |
| **Thư viện mẫu tin nhắn đa kênh:** | Cho phép tích chọn một hoặc nhiều mẫu tin nhắn thiết kế sẵn trong hệ thống OmniChat (tin nhắn chào hỏi, tin khuyến mãi, tin khảo sát ý kiến). |
| **Chiến lược xoay vòng mẫu tin (Template Rotation Strategy):** | Khi chọn nhiều mẫu tin, hệ thống cung cấp 2 thuật toán phân bổ thông minh phục vụ thử nghiệm hiệu quả nội dung (A/B Testing):<br>• <img src="https://api.iconify.design/lucide:repeat.svg?color=%23ff3333" width="16" alt="" /> `Xoay vòng tuần tự (ROUND_ROBIN)`: Khách hàng thứ nhất nhận mẫu A, khách hàng thứ hai nhận mẫu B, khách hàng thứ ba nhận mẫu C rồi quay lại mẫu A.<br>• <img src="https://api.iconify.design/lucide:shuffle.svg?color=%23ff3333" width="16" alt="" /> `Ngẫu nhiên (RANDOM)`: Phân bổ ngẫu nhiên các mẫu tin nhắn cho từng khách hàng theo tỷ lệ đồng đều. |

---

### Bước 3 — Cấu hình biến dữ liệu & Cơ chế Giá trị dự phòng (Fallback Value)

| Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- |
| **Danh sách biến trong mẫu tin:** | Hệ thống tự động phát hiện toàn bộ các biến dạng `{placeholder}` xuất hiện trong tất cả các mẫu tin đã chọn ở Bước 2. |
| **Chế độ gán giá trị biến:** | • `Biến động (Dynamic)`: Chọn cột tương ứng trong Bảng Động (ví dụ: Biến `{ten}` $\rightarrow$ Cột `Họ và tên`, Biến `{ma_don}` $\rightarrow$ Cột `Mã đơn hàng`).<br>• `Biến tĩnh (Static)`: Điền nội dung cố định cho biến. |
| **Cơ chế Giá trị dự phòng (Fallback Value - Cực kỳ quan trọng):** | Nhập chuỗi ký tự mặc định sẽ tự động hiển thị nếu ô dữ liệu trong bảng của khách hàng đó bị rỗng (ví dụ: Biến `{ten}` nếu ô bị trống thì tự động điền là *"Quý khách"*). Điều này đảm bảo câu văn gửi đi luôn mượt mà, chuyên nghiệp, tuyệt đối không bao giờ để lộ các khoảng trống vô nghĩa hoặc lỗi biến như *"Kính gửi {ten}"*. |

---

### Bước 4 — Lên lịch & Kích hoạt Chuỗi hành động phản hồi tự động

| Thành phần giao diện | Chi tiết tùy chọn & Quy tắc xử lý |
| :--- | :--- |
| **Lên lịch phát tin:** | Chọn phát tin ngay lập tức hoặc lên lịch hẹn giờ theo ngày giờ vàng. |
| **Trình quản lý hành động phản hồi (Campaign Actions Manager):** | Cấu hình các quy tắc phản ứng tự động khép kín dựa trên tương tác thực tế của khách hàng:<br>• **Sự kiện kích hoạt (Trigger Event):**<br>&nbsp;&nbsp;+ `SENT (Khi tin được gửi đi)`<br>&nbsp;&nbsp;+ `DELIVERED (Khi tin nhắn đã đến thiết bị)`<br>&nbsp;&nbsp;+ `READ (Khi khách hàng đã mở xem tin)`<br>&nbsp;&nbsp;+ `REPLIED (Khi khách hàng nhắn tin trả lời - Quan trọng nhất)`<br>&nbsp;&nbsp;+ `FAILED (Khi gửi tin nhắn thất bại)`.<br>• **Hành động phản hồi tự động:**<br>&nbsp;&nbsp;+ `Gán thẻ hội thoại (ADD_TAG)` / `Xóa thẻ (REMOVE_TAG)`: Tự động phân loại khách hàng.<br>&nbsp;&nbsp;+ `Chuyển trạng thái hội thoại (UPDATE_CONVERSATION_STATUS)`: Đổi sang *Đang xử lý* hoặc *Cần can thiệp gấp*.<br>&nbsp;&nbsp;+ **Bật trợ lý ảo AI Agent (TOGGLE_AI_AGENT):** Tự động bật AI Agent vào tiếp quản cuộc trò chuyện để tư vấn, trả lời câu hỏi và chốt đơn ngay lập tức khi khách nhắn lại.<br>&nbsp;&nbsp;+ `Cập nhật ô tính trong Bảng Động (UPDATE_FIELD)`: Điền trạng thái tương tác vào cột tương ứng.<br>&nbsp;&nbsp;+ `Kích hoạt Quy trình tự động (TRIGGER_WORKFLOW)`: Kích hoạt Workflow xử lý đơn hàng liên phòng ban. |

---

## Các bước thao tác tuần tự trên giao diện UI

| Bước | Thành phần giao diện | Cách thực hiện chi tiết trên Giao diện UI |
| :---: | :--- | :--- |
| **1** | **Mở tiện ích** | Trong Hộp thoại Trung Tâm Tiện Ích, nhấp vào thẻ <img src="https://api.iconify.design/lucide:messages-square.svg?color=%23ff3333" width="16" alt="" /> **Tạo chiến dịch gửi tin nhắn đa kênh**. Hộp thoại Wizard bước 1 hiển thị. |
| **2** | **Bước 1 — Chọn đối tượng** | Nguồn *Bảng Động (Custom Table)* được chọn sẵn. Nhấp vào công cụ lọc `FilterBuilder` để thêm điều kiện lọc khách hàng (ví dụ: Cột `Trạng thái` bằng `Tiềm năng`). Bấm nút **Tiếp tục**. |
| **3** | **Bước 2 — Chọn kênh & Mẫu** | Tích chọn tài khoản Zalo OA và Fanpage Facebook; tích chọn 2 mẫu tin nhắn khác nhau; chọn chiến lược xoay vòng `ROUND_ROBIN (Tuần tự)`. Bấm nút **Tiếp tục**. |
| **4** | **Bước 3 — Khớp biến & Giá trị dự phòng** | Khớp nối biến `{ten}` với cột `Họ và tên`, nhập giá trị dự phòng Fallback là *"Quý khách"*. Bấm nút **Tiếp tục**. |
| **5** | **Bước 4 — Lên lịch & Kích hoạt AI Agent** | Thiết lập quy tắc phản hồi: Khi có sự kiện `REPLIED (Khách hàng nhắn lại)` $\rightarrow$ Chọn hành động **Bật trợ lý ảo AI Agent** và **Gán thẻ 'Khách quan tâm'**. Bấm nút **Phát động chiến dịch**. |

---

## Kiểm tra kết quả

| Hạng mục kiểm tra | Dấu hiệu nhận biết thành công trên giao diện |
| :--- | :--- |
| **Kiểm tra gửi tin nhắn đa kênh** | Khách hàng nhận được tin nhắn trên Zalo hoặc Messenger Facebook với nội dung cá nhân hóa chỉn chu, các trường hợp tên bị trống hiển thị chữ *"Quý khách"* tự nhiên. |
| **Kiểm tra tương tác phản hồi tự động** | Khi khách nhắn tin trả lời trên điện thoại: hộp chat trên OmniChat lập tức chuyển trạng thái sang *Đang xử lý*, được gắn thẻ *Khách quan tâm*, và **trợ lý ảo AI Agent tự động gửi tin nhắn tư vấn tiếp theo chỉ trong 2 giây**. |

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
| **Lọc danh sách đối tượng gửi tin nhắn đa kênh** | `listRecords` | *"Hãy truy vấn bảng 'Khách Hàng', lọc danh sách các khách hàng chưa phản hồi tin nhắn trong 7 ngày qua để chuẩn bị tệp phát động chiến dịch gửi tin đa kênh tiếp cận lại."* |
| **Cập nhật trạng thái hội thoại sau chiến dịch** | `updateRecords` | *"Hãy cập nhật cột 'Kênh phản hồi' thành 'Đã tương tác lại' cho các khách hàng vừa trả lời tin nhắn trong chiến dịch đa kênh."* |

### Bảng kiểm tra chéo 2 chiều (UI ↔ AI Agent)

| Hành động thực hiện trên Giao diện UI | Kết quả kiểm tra xác thực bằng Tool Agent |
| :--- | :--- |
| Phát động chiến dịch Đa kênh trên giao diện | Gọi `listRecords` thấy danh sách đối tượng nhận tin trùng khớp hoàn toàn với các dòng bản ghi thỏa mãn bộ lọc của bảng. |
| **Lệnh thực hiện bởi AI Agent qua Tool** | **Vị trí và dấu hiệu kiểm tra trên Giao diện UI** |
| Agent lọc dữ liệu khách hàng | Người dùng mở Trình hướng dẫn chiến dịch Đa kênh Bước 1, số lượng khách hàng hiển thị đúng theo phân tích của Agent. |
