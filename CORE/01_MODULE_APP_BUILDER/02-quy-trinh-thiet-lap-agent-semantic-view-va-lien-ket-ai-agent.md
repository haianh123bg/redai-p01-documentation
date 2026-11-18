## Mở khu vực Agent Semantic View và AI Agent, Năng lực & Cấu hình

Để giúp trợ lý ảo AI Agent có thể đọc hiểu số liệu trực tiếp trên từng trang ứng dụng dưới dạng báo cáo Markdown chuẩn xác, đồng thời phân quyền vai trò và gắn ứng dụng vào AI Agent, bạn mở màn hình cấu hình theo một trong hai cách sau:

1. **Mở nhanh từ Trình xem App (`/app-builder/:appId`)**:
   - Bấm trực tiếp vào biểu tượng <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Cấu hình AI Agent đọc dữ liệu App)** trên thanh tiêu đề phía trên cùng để mở nhanh cửa sổ **Agent Semantic View**.
   - Hoặc bấm nút <img src="https://api.iconify.design/lucide:settings.svg?color=%23ff3333" width="16" alt="" /> **(Cài đặt)** để chuyển sang trang **Cài đặt App** (`/app-builder/:appId/settings`).
2. **Tại thanh danh mục bên trái của trang Cài đặt App (`/app-builder/:appId/settings`)**:
   - Nhấp vào mục <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> **(Agent Semantic View)** (`/app-builder/:appId/settings?tab=agentView`) để thiết lập bộ đọc dữ liệu trang cho AI Agent.
   - Nhấp vào mục <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(AI Agent, Năng lực & Cấu hình)** (`/app-builder/:appId/settings?tab=blueprint`) để quản lý **Hồ sơ cấu hình**, **Phân quyền Vai trò** và **AI Agent liên kết**.

---

## Các bước thực hiện

### Chọn phương án thiết lập Agent Semantic View phù hợp

Ở Giai đoạn 1, bạn có thể chọn một trong hai cách để tạo kịch bản đọc dữ liệu trang (`Transform Script`) cho trợ lý ảo AI Agent:

| Phương án | Khi nào nên sử dụng | Cách hoạt động |
| :--- | :--- | :--- |
| **Phương án 1 — Dùng nút Ask AI tự động sinh cấu hình** | Khuyên dùng cho hầu hết người dùng muốn tiết kiệm thời gian và đảm bảo mã kịch bản không bị lỗi cú pháp. | Hệ thống tự động phân tích mã nguồn trang VFS cùng các API gắn trên trang để sinh trọn bộ `Tool Name`, `Transform Script (JS)`, `Input Schema` và `Test Params`. |
| **Phương án 2 — Tự cấu hình Script & Schema thủ công** | Khi bạn muốn tùy chỉnh chi tiết cách lọc tham số đầu vào, thời gian lưu đệm (`Cache TTL`) hoặc định dạng bảng biểu Markdown trả về cho AI Agent. | Bạn tự nhập `Tool Name`, `Cache TTL`, `Mô tả Prompt` và biên tập trực tiếp trong 3 tab **Transform Script (JS)**, **Input Schema**, **Test Params**. |

---

### Giai đoạn 1 — Cấu hình và kiểm thử Agent Semantic View cho từng trang

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Chọn trang cần cấu hình và mở khung Script & Schema** | Tại mục <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> **(Agent Semantic View)**, trên thanh công cụ phía trên:<br>• Chọn trang muốn thiết lập tại ô **Trang:** (`Tìm & chọn trang...`).<br>• Bấm nút chuyển chế độ sang <img src="https://api.iconify.design/lucide:code.svg?color=%23ff3333" width="16" alt="" /> **(Script & Schema)** (hoặc bấm biểu tượng <img src="https://api.iconify.design/lucide:sliders.svg?color=%23ff3333" width="16" alt="" /> **(Hiện khối Script & Schema (Chế độ Cấu hình))**) để hiển thị khung biên tập bên trái. |
| **2. Sinh tự động bằng AI hoặc nhập thông tin định danh công cụ** | • **Nếu dùng AI tự động**: Bấm nút <img src="https://api.iconify.design/lucide:sparkles.svg?color=%23ff3333" width="16" alt="" /> **(Ask AI Sinh Agent View (VFS Playground))** trên thanh công cụ để AI tự động điền toàn bộ cấu hình.<br>• **Nếu thiết lập hoặc chỉnh sửa thủ công**, kiểm tra 3 trường thông tin cố định phía trên khung trái:<br>  1. **Tool Name (snake_case): \***: Tên định danh công cụ viết thường nối bằng dấu gạch dưới (ví dụ: `read_page_overview`).<br>  2. **Cache TTL (giây):**: Thời gian lưu kết quả vào bộ nhớ đệm (nhập `0` nếu luôn muốn đọc dữ liệu mới nhất).<br>  3. **Mô tả Prompt cho AI Agent:**: Mô tả ngắn gọn để AI Agent biết khi nào nên gọi bộ đọc của trang này. |
| **3. Thiết lập nội dung trong 3 tab kỹ thuật** | Lần lượt kiểm tra 3 tab con bên dưới:<br>1. Tab <img src="https://api.iconify.design/lucide:code.svg?color=%23ff3333" width="16" alt="" /> **(Transform Script (JS))**: Chứa mã nguồn tại ô **JavaScript Template Script: \*** dùng để gọi các API của trang và tổng hợp thành văn bản Markdown.<br>2. Tab <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(Input Schema)**: Chứa cấu trúc tham số đầu vào tại ô **JSON Schema: \*** (ví dụ: bộ lọc từ ngày, đến ngày, trạng thái...).<br>3. Tab <img src="https://api.iconify.design/lucide:play-circle.svg?color=%23ff3333" width="16" alt="" /> **(Test Params)**: Nhập giá trị tham số thử nghiệm vào ô **JSON Test Parameters:** để phục vụ chạy thử. |
| **4. Chạy thử nghiệm và lưu cấu hình** | • Bấm nút <img src="https://api.iconify.design/lucide:play.svg?color=%23ff3333" width="16" alt="" /> **(Chạy thử nghiệm với tham số (Execute/Preview))** trên thanh công cụ.<br>• Quan sát khung bên phải <img src="https://api.iconify.design/lucide:file-text.svg?color=%23ff3333" width="16" alt="" /> **(Xem trước nội dung (Runtime Markdown View))** và khung **CONSOLE LOGS:** bên dưới để đảm bảo báo cáo Markdown hiển thị đúng số liệu thật.<br>• Bấm nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cấu hình Agent View)** để kích hoạt trạng thái **AI Agent Enabled** cho trang (bạn cũng có thể dùng nút <img src="https://api.iconify.design/lucide:copy.svg?color=%23ff3333" width="16" alt="" /> **(Sao chép Markdown kết quả)** hoặc <img src="https://api.iconify.design/lucide:download.svg?color=%23ff3333" width="16" alt="" /> **(Tải file Markdown)** nếu cần xuất báo cáo). |

---

### Giai đoạn 2 — Tạo Hồ sơ cấu hình và Phân quyền Vai trò (Scope-Role)

Khi một ứng dụng được gắn vào nhiều trợ lý ảo AI Agent khác nhau (ví dụ: Agent tư vấn khách hàng chỉ được tạo đơn và thanh toán QR, không được dùng khuyến mãi hoặc vận chuyển), bạn sử dụng mục <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(AI Agent, Năng lực & Cấu hình)**:

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Tạo Hồ sơ cấu hình mới** | Tại mục <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(AI Agent, Năng lực & Cấu hình)**, chọn tab đầu tiên **(Hồ sơ cấu hình ({N}))**, sau đó bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo hồ sơ cấu hình mới)** trên thanh công cụ. |
| **2. Thiết lập Phân quyền tính năng (Capabilities) và Tham số JSON** | Trong hộp thoại **Tạo Hồ sơ cấu hình mới**, điền các thông tin:<br>• **Tên cấu hình \***: Nhập tên hồ sơ (ví dụ: `Cấu hình Chi nhánh Quận 1`).<br>• **Mô tả**: Nhập ghi chú mục đích sử dụng của hồ sơ.<br>• **Phân quyền tính năng (Feature Scope & Capabilities)**: Bấm chọn các thẻ tính năng có sẵn như **Quản lý đơn hàng (Orders)** (`business.order`), **Thanh toán VietQR** (`business.qr`), **Vận chuyển (Shipping)** (`business.shipping`), **Khuyến mãi (Vouchers)** (`business.voucher`), hoặc nhập mã quyền tùy chỉnh vào ô `Nhập mã quyền (vd: crm.leads) rồi nhấn Thêm...` và bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm)**.<br>• **Cài đặt tham số (JSON Settings)**: Nhập đối tượng cấu hình JSON (có thể bấm nút **(Định dạng JSON)** để làm đẹp mã).<br>• Bấm nút **(Lưu hồ sơ)** để hoàn tất. |
| **3. Thiết lập Phân quyền Vai trò (Scope-Role ↔ Kỹ năng AI)** | Chuyển sang tab thứ hai **(Phân quyền Vai trò ({N}))** và bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Gán quyền cho Vai trò mới)**. Trong hộp thoại **Gán quyền Role & Skill AI (Chọn nhiều)**:<br>• **Chọn vai trò (Scope-Role) \***: Chọn một hoặc nhiều vai trò trong ứng dụng (bao gồm vai trò khách hàng `Khách hàng (CUSTOMER)` hoặc các vai trò nội bộ).<br>• **Kỹ năng AI (Skill)**: Chọn nguồn **(Của tôi)** hoặc **(Hệ thống)**, sau đó tìm và chọn một hoặc nhiều Skill tương ứng với vai trò đó.<br>• Bấm nút **(Lưu phân quyền)**. Trên danh sách bên ngoài, bạn có thể bấm nút <img src="https://api.iconify.design/lucide:users.svg?color=%23ff3333" width="16" alt="" /> / <img src="https://api.iconify.design/lucide:brain.svg?color=%23ff3333" width="16" alt="" /> để đổi góc nhìn giữa **Gom theo Vai trò** và **Gom theo Kỹ năng**. |

---

### Giai đoạn 3 — Liên kết ứng dụng vào AI Agent

| Bước | Cách thực hiện |
| :--- | :--- |
| **1. Mở hộp thoại Liên kết AI Agent** | Chuyển sang tab thứ ba **(AI Agent liên kết ({N}))** trong mục **AI Agent, Năng lực & Cấu hình**, sau đó bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết AI Agent)**. |
| **2. Chọn AI Agent, Vai trò đảm nhiệm và Hồ sơ cấu hình** | Trong hộp thoại **Liên kết & Cấu hình AI Agent**, thiết lập 3 phần:<br>1. **AI Agent liên kết \***: Tìm kiếm tại ô `Tìm kiếm Agent theo tên hoặc ID...` và nhấp chọn trợ lý ảo AI Agent muốn gắn ứng dụng.<br>2. **Vai trò đảm nhiệm trong Ứng dụng (Scope-Role)**: Bấm **(Thay đổi)** để chọn cơ chế vận hành:<br>   • **Tự động thích ứng** (`TẤT CẢ`): Tự động nhận diện người đang chat là nhân viên nội bộ hay khách hàng để nạp đúng Kỹ năng tương ứng.<br>   • **Khách hàng (CUSTOMER)** (`base_customer`) hoặc một vai trò cố định: Khóa cứng quyền hạn của AI Agent ở vai trò đã chọn.<br>3. **Danh sách hồ sơ cấu hình**: Chọn **Mặc định (Không dùng hồ sơ cấu hình)** hoặc tích chọn một hồ sơ cấu hình đã tạo ở Giai đoạn 2 (có thể bấm **+ Thêm cấu hình mới** ngay trong hộp thoại này). |
| **3. Lưu liên kết** | Bấm nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Liên kết Agent)** (hoặc <img src="https://api.iconify.design/lucide:check.svg?color=%23ff3333" width="16" alt="" /> **(Lưu thay đổi)** khi chỉnh sửa). |

---

## Kiểm tra kết quả

1. **Tại mục Agent Semantic View**: Nhãn trạng thái trên thanh công cụ chuyển sang màu xanh **AI Agent Enabled**; khi bấm <img src="https://api.iconify.design/lucide:play.svg?color=%23ff3333" width="16" alt="" /> **(Chạy thử nghiệm với tham số (Execute/Preview))**, khung **Xem trước nội dung (Runtime Markdown View)** hiển thị báo cáo Markdown rõ ràng và không có báo lỗi đỏ trong **CONSOLE LOGS:**.
2. **Tại mục AI Agent, Năng lực & Cấu hình**:
   - Tab **Hồ sơ cấu hình** hiển thị hồ sơ mới kèm các nhãn quyền hạn (`business.order`, `business.qr`...) và cho phép bấm menu thao tác để **Đổi tên**, **Chỉnh sửa**, **Xem tham số JSON** hoặc **Xóa**.
   - Tab **AI Agent liên kết** hiển thị tên AI Agent vừa gắn kèm **Hồ sơ Cấu hình áp dụng** và **Vai trò đảm nhiệm (Scope-Role)**.

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn có thể yêu cầu trợ lý ảo AI Agent tự động viết kịch bản đọc dữ liệu trang (`Data Reader / Agent Semantic View`), chạy thử báo cáo Markdown và quản lý các **Hồ sơ cấu hình (`App Configuration`)** mà không cần thao tác thủ công.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

- **Kỹ năng (Skill) cần trang bị**: `RedAI - Module - App Builder` (ID: `58f36f44-2e1c-4aaf-8ca7-d73008169e95`)
- **Bộ công cụ (Tool) đi kèm trong kỹ năng**: `RedAI - Module - App Builder` (ID: `d16e4656-c070-43b6-b234-abcff883fd61`)
- **Quyền hạn tài khoản**: Tài khoản người dùng có quyền quản trị ứng dụng MiniApp trong Workspace.

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Xem cấu hình **Agent Semantic View** hiện tại của một trang | `pageData_getReaderConfig` | Lấy thông tin `Tool Name`, `Cache TTL`, `Transform Script`, `Input Schema` của một trang trong ứng dụng. |
| Điền **Transform Script (JS)**, **Input Schema** và bấm <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu cấu hình Agent View)** | `pageData_configureReader` | Lưu hoặc cập nhật kịch bản đọc dữ liệu ngữ nghĩa (Data Reader) cho một trang cụ thể. |
| Bấm <img src="https://api.iconify.design/lucide:play.svg?color=%23ff3333" width="16" alt="" /> **(Chạy thử nghiệm với tham số (Execute/Preview))** | `pageData_preview`, `pageData_readExecution` | Chạy thử kịch bản `Transform Script` với bộ tham số đầu vào để kiểm tra kết quả báo cáo Markdown và log thực thi. |
| Xóa bộ đọc dữ liệu của trang | `pageData_deleteReader` | Gỡ bỏ cấu hình Agent Semantic View khỏi trang được chỉ định. |
| Bấm <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Tạo hồ sơ cấu hình mới)** trong tab **Hồ sơ cấu hình** | `appConfiguration_create` | Tạo hồ sơ cấu hình mới gồm tên, mô tả, danh sách `capabilities` và đối tượng `settings` JSON. |
| Xem, chỉnh sửa hoặc xóa các hồ sơ trong tab **Hồ sơ cấu hình** | `appConfiguration_findAll`, `appConfiguration_getDetail`, `appConfiguration_update`, `appConfiguration_delete` | Liệt kê danh sách hồ sơ cấu hình của ứng dụng, xem chi tiết, cập nhật quyền tính năng/tham số JSON hoặc xóa hồ sơ. |

### Câu lệnh mẫu (Prompt mẫu)

```text
Hãy giúp tôi thiết lập Agent Semantic View và tạo Hồ sơ cấu hình cho ứng dụng trên App Builder:

1. Bối cảnh và Mục tiêu:
- Tôi muốn AI Agent có thể đọc báo cáo tổng hợp trên trang chủ (/home) của ứng dụng và tạo một hồ sơ cấu hình giới hạn tính năng cho chi nhánh bán lẻ.

2. Dữ liệu cung cấp:
- ID ứng dụng (appId): "[Điền ID ứng dụng của bạn]"
- Đường dẫn trang cần cấu hình: "/home"
- Tên công cụ đọc trang (Tool Name): "read_home_dashboard"
- Tên hồ sơ cấu hình mới: "Cấu hình Chi nhánh Bán lẻ"
- Các quyền tính năng (Capabilities) cần bật: ["business.order", "business.qr"]

3. Các bước yêu cầu thực hiện:
- Bước 1: Dùng agentAppVfs_read đọc mã nguồn trang /pages/home/page.tsx và /apis.json để nắm rõ các API đang dùng trên trang.
- Bước 2: Dùng pageData_configureReader để cấu hình Agent Semantic View cho trang "/home" với Tool Name "read_home_dashboard", viết Transform Script tổng hợp số liệu thành bảng Markdown rõ ràng.
- Bước 3: Dùng pageData_preview để chạy thử bộ đọc vừa lưu và kiểm tra nội dung Markdown trả về.
- Bước 4: Dùng appConfiguration_create để tạo hồ sơ "Cấu hình Chi nhánh Bán lẻ" với danh sách capabilities ["business.order", "business.qr"].

4. Yêu cầu phản hồi:
- Hiển thị bản xem trước báo cáo Markdown của trang "/home" và thông tin ID của Hồ sơ cấu hình vừa tạo.
```

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Thao tác thực hiện |
| :--- | :--- |
| **Cách 1 — Kiểm tra trực tiếp trên giao diện** | Mở `/app-builder/:appId/settings?tab=agentView` để xem kết quả Markdown tại khung **Xem trước nội dung (Runtime Markdown View)**, sau đó chuyển sang mục <img src="https://api.iconify.design/lucide:layers.svg?color=%23ff3333" width="16" alt="" /> **(AI Agent, Năng lực & Cấu hình)** để kiểm tra hồ sơ mới trong tab **Hồ sơ cấu hình**. |
| **Cách 2 — Yêu cầu trợ lý ảo AI Agent kiểm tra lại** | Gửi câu lệnh: *"Hãy gọi `pageData_getReaderConfig` cho trang `/home` và `appConfiguration_findAll` của ứng dụng để xác nhận toàn bộ cấu hình đã được lưu thành công."* |
