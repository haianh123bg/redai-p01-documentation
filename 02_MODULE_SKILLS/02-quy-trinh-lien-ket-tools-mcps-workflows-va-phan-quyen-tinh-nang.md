## Mở khu vực Tài nguyên Kỹ năng (Tools, MCPs, Workflows)

Để trang bị khả năng thực thi hành động thực tế cho một Kỹ năng (gọi API, truy vấn cơ sở dữ liệu, tương tác máy chủ MCP hoặc kích hoạt quy trình tự động hóa), bạn mở trang **Chi tiết Kỹ năng** (`/skills/:skillId`) từ màn hình **Thư viện Kỹ năng** (`/skills`).

Tại phần thân của trang **Chi tiết Kỹ năng**, bạn sẽ làm việc với 3 tab tài nguyên thực thi nằm cạnh tab **Docs**:

1. Tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **(Tools)**: Quản lý danh sách các công cụ API (Custom Tools) thuộc các nhóm dự án (`Project Schema`) được gắn vào Kỹ năng, đồng thời thiết lập **Phân quyền tính năng (Capability Tag)** cho từng công cụ.
2. Tab <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(MCPs)**: Quản lý danh sách các máy chủ giao thức ngữ cảnh mô hình (MCP Servers) được liên kết với Kỹ năng.
3. Tab <img src="https://api.iconify.design/lucide:workflow.svg?color=%23ff3333" width="16" alt="" /> **(Workflows)**: Quản lý các kịch bản quy trình tự động hóa đa bước được gắn vào Kỹ năng.

---

## Các bước thực hiện

### Chọn loại tài nguyên thực thi cần tích hợp vào Kỹ năng

Trước khi gắn tài nguyên ở Giai đoạn 1, hãy đối chiếu bảng dưới đây để chọn đúng loại tài nguyên cần tích hợp:

| Loại tài nguyên | Khi nào nên sử dụng | Tiện ích hỗ trợ trên thẻ tài nguyên |
| :--- | :--- | :--- |
| **Công cụ API (`Tools`)** (<img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" />) | Khi Kỹ năng cần gọi các hàm API RESTful hoặc thao tác với Bảng dữ liệu động (Dynamic Tables) đã được định nghĩa trong `Project Schema`. | Hỗ trợ lọc theo nhóm `Project Schema`, mở nhanh trang quản lý Project Tools (<img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" />) và cài đặt **Phân quyền tính năng** (<img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" />). |
| **Máy chủ MCP (`MCPs`)** (<img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" />) | Khi Kỹ năng cần kết nối tới một cụm công cụ chuẩn MCP (Model Context Protocol) nội bộ hoặc bên thứ ba. | Hiển thị tên máy chủ, mô tả, loại kết nối và trạng thái hoạt động (`Active` / `Inactive`). |
| **Quy trình tự động (`Workflows`)** (<img src="https://api.iconify.design/lucide:workflow.svg?color=%23ff3333" width="16" alt="" />) | Khi Kỹ năng cần kích hoạt một chuỗi tác vụ tự động hóa đã được thiết kế sẵn trên phân hệ Workflow. | Hiển thị tên quy trình, mô tả và trạng thái sẵn sàng thực thi. |

---

### Giai đoạn 1 — Liên kết Công cụ (Tools), Máy chủ MCP và Quy trình (Workflows)

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Liên kết Công cụ API trong tab Tools** | 1. Chọn tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **(Tools)** và bấm vào thẻ đầu tiên <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Create New)**.<br>2. Trong hộp thoại **Thêm công cụ vào kỹ năng**:<br>   • Chọn tab phân vùng nguồn: **(Của tôi)** hoặc **(Hệ thống)**.<br>   • Ở cột bên trái (**Project Schema**), nhấp chọn một nhóm dự án để lọc công cụ theo nhóm (có thể bấm nút **(Chọn cả nhóm)** hoặc **(Bỏ chọn nhóm)** để chọn nhanh toàn bộ công cụ trong dự án đó).<br>   • Ở cột bên phải, sử dụng ô tìm kiếm <img src="https://api.iconify.design/lucide:search.svg?color=%23ff3333" width="16" alt="" /> **(Tìm kiếm công cụ...)** và tích chọn các công cụ cần gắn.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Thêm {số lượng} mục)** ở góc dưới bên phải. |
| **2. Liên kết Máy chủ MCP trong tab MCPs** | 1. Chuyển sang tab <img src="https://api.iconify.design/lucide:server.svg?color=%23ff3333" width="16" alt="" /> **(MCPs)** và bấm vào thẻ đầu tiên <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Create New)**.<br>2. Trong hộp thoại **Thêm MCP vào kỹ năng**, chọn nguồn **(Của tôi)** hoặc **(Hệ thống)**, tìm kiếm tại ô **Tìm kiếm MCP...**, tích chọn các máy chủ MCP cần dùng.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Thêm {số lượng} mục)**. |
| **3. Liên kết Quy trình trong tab Workflows** | 1. Chuyển sang tab <img src="https://api.iconify.design/lucide:workflow.svg?color=%23ff3333" width="16" alt="" /> **(Workflows)** và bấm vào thẻ đầu tiên <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Create New)**.<br>2. Trong hộp thoại **Thêm workflow vào kỹ năng**, tìm kiếm tại ô **Tìm kiếm workflow...**, tích chọn các quy trình cần gắn.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Thêm {số lượng} mục)**. |

---

### Giai đoạn 2 — Cài đặt Phân quyền tính năng (Capability Tag) cho từng Công cụ

Khi một Kỹ năng chứa nhiều công cụ thuộc các mảng nghiệp vụ khác nhau (ví dụ: tạo đơn hàng, tạo mã QR thanh toán, đẩy vận đơn giao hàng, áp dụng mã giảm giá), bạn có thể gắn mã **Phân quyền tính năng (Capability Tag)** cho từng công cụ để hệ thống tự động ẩn công cụ đó nếu ứng dụng (MiniApp) đang chạy không bật tính năng tương ứng (*Adaptive Tool Filtering / Dynamic Tool Pruning*):

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Cài đặt phân quyền tính năng** | Tại tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **(Tools)**, tìm đến thẻ của công cụ cần thiết lập và bấm vào biểu tượng cái khiên <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt phân quyền tính năng)** ở góc trên bên phải của thẻ. |
| **2. Chọn hoặc nhập mã Phân quyền tính năng (Capability Tag)** | Trong hộp thoại **Cài đặt Phân quyền Tính năng cho Công cụ**:<br>• **Nếu là công cụ cốt lõi luôn được phép sử dụng**: Bấm chọn nút **(Dùng chung (Toàn quyền - Core))** (hoặc xóa trống ô nhập liệu).<br>• **Nếu chỉ cho phép nạp công cụ khi ứng dụng bật tính năng tương ứng**: Nhập mã quyền vào ô **Phân quyền tính năng (Capability Tag)** hoặc bấm chọn nhanh một trong các thẻ gợi ý có sẵn:<br>  - **Đơn hàng (`business.order`)**: Các công cụ tạo, sửa, hủy, duyệt đơn hàng.<br>  - **Mã QR (`business.qr`)**: Các công cụ sinh mã thanh toán VietQR.<br>  - **Vận chuyển (`business.shipping`)**: Các công cụ tính phí giao hàng và cập nhật mã vận đơn.<br>  - **Khuyến mãi (`business.voucher`)**: Các công cụ kiểm tra và quản lý mã giảm giá.<br>*(Bạn có thể bấm vào nút **`?`** bên cạnh tiêu đề để xem sơ đồ giải thích cơ chế lọc công cụ tự động).* |
| **3. Lưu thiết lập** | Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cài đặt)**. Ngay sau khi lưu, trên thẻ công cụ sẽ xuất hiện nhãn hiển thị quyền tương ứng (ví dụ: `Quyền: business.order` hoặc `Dùng chung (Toàn quyền)`). |

---

### Giai đoạn 3 — Mở Project Tools để kiểm tra và cập nhật chỉ thị định tuyến

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở nhanh trang quản lý Project Tools gốc (Khi cần)** | Trên bất kỳ thẻ công cụ nào trong tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **(Tools)**, bạn có thể bấm vào biểu tượng <img src="https://api.iconify.design/lucide:external-link.svg?color=%23ff3333" width="16" alt="" /> **(Mở project tools)** ở góc trên bên phải thẻ để chuyển thẳng sang trang quản lý Project Schema (`/tools/projects/:projectSchemaId`) của công cụ đó (nơi cấu hình URL máy chủ, phương thức xác thực và chuyên biệt hóa công cụ). |
| **2. Chèn tham chiếu công cụ vào Nội dung Skill** | 1. Quay lại đầu trang **Chi tiết Kỹ năng** (`/skills/:skillId`), bấm nút <img src="https://api.iconify.design/lucide:edit.svg?color=%23ff3333" width="16" alt="" /> **(Chỉnh sửa)** trên thẻ tổng quan Kỹ năng.<br>2. Tại ô **Nội dung Skill**, gõ ký tự **`@`** để mở danh sách tài nguyên vừa gắn, chọn các công cụ (`tools/...`) và tài liệu (`docs/...`) để hoàn thiện bảng định tuyến cho AI Agent.<br>3. Bấm nút <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu thay đổi)**. |

---

## Kiểm tra kết quả

1. **Tại các tab Tools, MCPs, Workflows**: Hiển thị đầy đủ các thẻ tài nguyên vừa được liên kết; khi bấm vào nút phễu lọc <img src="https://api.iconify.design/lucide:filter.svg?color=%23ff3333" width="16" alt="" /> **(Lọc theo Project Schema)** trên thanh công cụ ở tab **Tools**, danh sách hiển thị đúng các nhóm dự án đang có công cụ trong Kỹ năng.
2. **Trên từng thẻ công cụ trong tab Tools**: Hiển thị đúng nhãn phân quyền tính năng (`Dùng chung (Toàn quyền)` hoặc `Quyền: {capability}`) khớp với cấu hình vừa lưu.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Toàn bộ các thao tác gắn hoặc gỡ công cụ (`Tools`), máy chủ `MCPs`, quy trình `Workflows` và thiết lập mã phân quyền tính năng (`Capability Tag`) cho từng công cụ trong Kỹ năng đều có thể thực hiện tự động qua trợ lý ảo AI Agent.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - Skill` (ID: `57cc282f-a2d2-4dfc-9981-153fe58f7cf5`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - Skill` (ID: `7534d86e-8a3c-4e74-aaec-5f0da403ec41`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền chỉnh sửa Kỹ năng và truy cập các tài nguyên Tools, MCPs, Workflows trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Mở các tab **Tools**, **MCPs**, **Workflows** để xem danh sách tài nguyên đang gắn | `getSkillTools`, `getSkillMcps`, `getSkillWorkflows` | Liệt kê danh sách các công cụ, máy chủ MCP và quy trình tự động hiện đang được liên kết trong Kỹ năng. |
| Bấm thẻ <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Create New)** và chọn **Thêm {N} mục** | `addSkillResources` | Liên kết đồng thời một hoặc nhiều `toolIds`, `mcpIds`, `workflowIds` hoặc `docIds` vào Kỹ năng. |
| Bấm nút <img src="https://api.iconify.design/lucide:shield.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt phân quyền tính năng)** trên thẻ công cụ | `updateSkillToolCapability` | Gán hoặc xóa mã phân quyền tính năng (`capability`, ví dụ: `business.order`, `business.qr`...) cho một công cụ cụ thể trong Kỹ năng. |
| Tích chọn các thẻ tài nguyên và bấm nút <img src="https://api.iconify.design/lucide:trash.svg?color=%23ff3333" width="16" alt="" /> **(Delete)** trên thanh công cụ | `removeSkillResources` | Gỡ liên kết các công cụ, máy chủ MCP, quy trình hoặc tài liệu đã chọn khỏi Kỹ năng (không xóa tài nguyên gốc). |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi liên kết bộ công cụ vào Kỹ năng và thiết lập phân quyền tính năng (Capability Tag) theo yêu cầu sau:

1. Bối cảnh và Mục tiêu:
- Tôi cần gắn các công cụ xử lý đơn hàng và thanh toán QR vào Kỹ năng bán hàng, đồng thời gán mã capability để hệ thống tự động lọc công cụ theo cấu hình cửa hàng.

2. Dữ liệu cung cấp:
- ID Kỹ năng (skillId): "[Điền ID Kỹ năng của bạn]"
- Danh sách ID công cụ cần gắn (toolIds): ["[toolId_1]", "[toolId_2]"]
- Phân quyền tính năng cần thiết lập:
  + Công cụ "[toolId_1]": gán capability = "business.order"
  + Công cụ "[toolId_2]": gán capability = "business.qr"

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng công cụ addSkillResources để gắn danh sách toolIds trên vào Kỹ năng.
- Bước 2: Dùng công cụ updateSkillToolCapability để gán capability "business.order" cho "[toolId_1]" và "business.qr" cho "[toolId_2]".
- Bước 3: Dùng getSkillTools để kiểm tra lại danh sách công cụ và nhãn capability trong Kỹ năng.

4. Yêu cầu phản hồi:
- Báo cáo bảng danh sách các công cụ đã gắn trong Kỹ năng kèm theo tên công cụ, ID và mã capability hiện tại.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở trang `/skills/:skillId`, chuyển sang tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **(Tools)** để kiểm tra các thẻ công cụ mới xuất hiện kèm nhãn `Quyền: business.order` và `Quyền: business.qr`. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `getSkillTools`, `getSkillMcps` và `getSkillWorkflows` của Kỹ năng này để liệt kê toàn bộ tài nguyên đang được liên kết."* |
