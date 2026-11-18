## Mở khu vực Nhà cung cấp dịch vụ tự tạo

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Trên thanh điều hướng chính ở cột bên trái của **nền tảng RedAI**, chọn mục <img src="https://api.iconify.design/lucide:blocks.svg?color=%23ff3333" width="16" alt="" /> **Tích hợp**. |
| **2** | Chọn tiếp tab <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ff3333" width="16" alt="" /> **Nhà cung cấp tự tạo** (tại đường dẫn `/integrations/my-integrations?tab=custom-providers`). |
| **3** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm nhà cung cấp tùy chỉnh)** ở góc trên bên phải để mở hộp thoại khai báo ứng dụng mới. |

---

## Các bước thực hiện

### Chọn chế độ và phương án thiết lập (Kiến trúc Dual-Mode)

Tính năng này cho phép doanh nghiệp đưa bất kỳ phần mềm chuyên biệt nào (hệ thống quản trị kho nội bộ, phần mềm kế toán riêng, website bán hàng, hay máy chủ trí tuệ nhân tạo riêng) vào **nền tảng RedAI** thông qua kiến trúc kép **Dual-Mode** tối ưu:

| Chế độ & Phương án | Dùng khi | Đặc điểm nổi bật |
| :--- | :--- | :--- |
| <img src="https://api.iconify.design/lucide:zap.svg?color=%23ff3333" width="16" alt="" /> **Chế độ Nhanh 30s (Quick Simple Mode)** | Thiết lập nhanh các cổng API chuẩn REST, mô hình LLM tương thích OpenAI hoặc kết nối API Key thông thường. | - Chọn nhanh từ Thư viện mẫu cấu hình sẵn (**Presets**: OpenAI, Anthropic Claude, Google Gemini, DeepSeek...).<br>- Tự động đấu nối biến và sinh trường nhập liệu.<br>- Xem trước câu lệnh cURL thời gian thực (**Live cURL Preview**) trực quan, hoàn thành chỉ trong 30 giây. |
| <img src="https://api.iconify.design/lucide:git-fork.svg?color=%23ff3333" width="16" alt="" /> **Chế độ Chuyên sâu (Advanced Canvas DAG Mode)** | Các hệ thống ngân hàng, cổng thanh toán hoặc phần mềm nội bộ yêu cầu xác thực đa bước phức tạp. | - Thiết kế trực quan trên đồ thị nút Canvas (DAG Workflow).<br>- Tùy biến chữ ký số bảo mật HMAC, quy trình ủy quyền OAuth2 3 bước, tự động làm mới mã Token.<br>- Tinh chỉnh chi tiết thứ tự thực thi và tiêu đề tùy biến (Custom Headers). |
| <img src="https://api.iconify.design/lucide:cpu.svg?color=%23ff3333" width="16" alt="" /> **Khai báo mô hình trí tuệ nhân tạo riêng** | Doanh nghiệp triển khai cụm máy chủ AI riêng (như mô hình Llama, Qwen, DeepSeek tự cài đặt trên hạ tầng riêng). | Máy chủ AI của bạn hỗ trợ chuẩn giao tiếp tương thích với OpenAI hoặc Anthropic, kết nối nhanh chóng và an toàn. |

---

### Giai đoạn 1 — Khai báo định danh và phạm vi hiển thị ứng dụng

Bước này giúp đồng nghiệp và nhân viên trong doanh nghiệp nhận biết rõ ràng phần mềm khi tìm kiếm trong Kho ứng dụng tích hợp:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | **Đặt tên hiển thị đa ngôn ngữ:** Nhập tên ứng dụng bằng Tiếng Việt (ví dụ: `Hệ Thống Kho Vận Nội Bộ`) và Tiếng Anh (ví dụ: `Internal Warehouse System`). |
| **2** | **Tải ảnh đại diện (Logo):** Bấm vào khung ảnh biểu trưng để tải lên file hình ảnh vuông (định dạng PNG hoặc SVG) làm logo nhận diện cho ứng dụng. |
| **3** | **Chọn danh mục nghiệp vụ:** Chọn nhóm ngành phù hợp (như *Bán hàng*, *Kho vận*, *Trí tuệ nhân tạo*, *Văn phòng*...) để thẻ ứng dụng nằm đúng vị trí phân loại trên kho. |
| **4** | **Phân quyền phạm vi sử dụng:** Tích chọn các khu vực trên **nền tảng RedAI** mà ứng dụng này được phép tham gia làm việc:<br>- <img src="https://api.iconify.design/lucide:message-square.svg?color=%23ff3333" width="16" alt="" /> **Khung chat thông minh (OmniChat):** Cho phép gọi ứng dụng trực tiếp trong các cuộc hội thoại.<br>- <img src="https://api.iconify.design/lucide:bot.svg?color=%23ff3333" width="16" alt="" /> **Trợ lý ảo AI Agent:** Cho phép **trợ lý ảo AI Agent** tự động truy xuất dữ liệu từ phần mềm này.<br>- <img src="https://api.iconify.design/lucide:git-fork.svg?color=%23ff3333" width="16" alt="" /> **Quy trình tự động hóa (Workflow):** Cho phép đưa phần mềm vào các kịch bản chạy tự động. |

---

### Giai đoạn 2 — Cấu hình phương thức bảo mật kết nối và Xem trước Live cURL

Lựa chọn chuẩn xác cách thức mà phần mềm yêu cầu để mở cổng tiếp nhận dữ liệu an toàn:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Chuyển sang thẻ cấu hình bảo mật trong hộp thoại. |
| **2** | **Nếu chọn Chế độ Nhanh (Quick Mode):**<br>- Chọn một mẫu nhà cung cấp có sẵn trong thư viện mẫu (**Preset**: OpenAI, Anthropic Claude, Google Gemini, DeepSeek...). Hệ thống sẽ tự động điền sẵn phương thức xác thực, tiêu đề Header và trường thông tin.<br>- Quan sát khung **Xem trước câu lệnh cURL (Live cURL Preview)** ở bên phải: Mỗi khi bạn thay đổi thông số hoặc thêm trường, câu lệnh cURL sẽ cập nhật theo thời gian thực để bạn kiểm tra cấu trúc gửi đi. |
| **3** | **Nếu chọn Chế độ Chuyên sâu (Advanced Canvas DAG Mode) hoặc tự cấu hình:**<br>- **Mã khóa kết nối API (API Key):** Phương thức phổ biến nhất, yêu cầu một chuỗi ký tự bí mật gửi kèm trong mỗi lần gọi.<br>- **Token định danh (Bearer Token):** Thường áp dụng cho các hệ thống máy chủ đám mây hiện đại.<br>- **Ủy quyền đăng nhập tự động (OAuth2):** Dành cho ứng dụng yêu cầu người dùng bấm nút đăng nhập và cấp quyền trực tiếp qua trình duyệt.<br>- **Chữ ký số an toàn chống giả mạo (HMAC Signature):** Dành cho hệ thống ngân hàng hoặc giao dịch tài chính yêu cầu mã hóa chữ ký số.<br>- **Không yêu cầu xác thực:** Áp dụng cho các cổng dữ liệu công khai nội bộ. |
| **4** | **Chọn vị trí gửi mã khóa bí mật:** Chọn nơi tiếp nhận chìa khóa kết nối (gửi trong phần tiêu đề gói tin `Header`, trong đường dẫn truy cập `Query`, hoặc trong phần nội dung gửi đi `Body`). |
| **5** | **Thử nghiệm chữ ký số trực tiếp (Nếu dùng HMAC):** Bấm nút <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ff3333" width="16" alt="" /> **(Thử nghiệm chữ ký số)** để hệ thống chạy thử thuật toán băm dữ liệu, đảm bảo hai bên mã hóa đồng nhất trước khi lưu. |

---

### Giai đoạn 3 — Thiết kế các ô nhập liệu cho người dùng

Tạo sẵn biểu mẫu nhập thông tin chuẩn xác để khi đồng nghiệp bấm "Kết nối ngay", màn hình sẽ hiện rõ những gì họ cần điền *(Lưu ý: Nếu dùng Chế độ Nhanh với Preset, các ô này đã được tạo tự động 100%)*:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Chọn nút <img src="https://api.iconify.design/lucide:plus.svg?color=%23ff3333" width="16" alt="" /> **(Thêm ô nhập liệu)** để thêm một trường thông tin mới. |
| **2** | **Thiết lập thông số cho từng ô:**<br>- **Tên hiển thị:** Nhãn tiếng Việt thân thiện với người dùng (ví dụ: `Địa chỉ máy chủ ERP`, `Mã khóa bí mật`).<br>- **Tên biến nhận dạng:** Tên kỹ thuật viết liền không dấu (ví dụ: `server_url`, `api_key`).<br>- **Kiểu dữ liệu:** Chọn dạng chữ thông thường (`Văn bản`), dạng mật khẩu ẩn giấu hoa thị (`Bảo mật / Password`), dạng số (`Số`), hoặc danh sách lựa chọn sẵn (`Menu thả xuống`).<br>- **Tính bắt buộc:** Bật công tắc nếu trường này bắt buộc phải điền mới được kích hoạt kết nối. |
| **3** | Nhập câu gợi ý mẫu (Placeholder) để đồng nghiệp nhìn vào biết ngay cần điền theo dạng nào (ví dụ: `https://erp.congty.com/api/v1`). Khung Live cURL Preview sẽ lập tức phản ánh biến vừa thêm vào câu lệnh mẫu. |

---

### Giai đoạn 4 — Soạn thảo hướng dẫn và tự động kiểm tra an toàn

Giúp các nhân sự khác trong công ty có thể tự thực hiện cắm dây kết nối thành công mà không cần làm phiền đội ngũ kỹ thuật:

| Bước | Cách thực hiện |
| :---: | :--- |
| **1** | Tại khung soạn thảo **Hướng dẫn kết nối**, nhập các bước hướng dẫn cụ thể bằng Tiếng Việt dễ hiểu (chỉ rõ nhân viên cần vào đâu trên phần mềm ngoài để lấy chìa khóa kết nối). *(Bạn cũng có thể dùng tính năng sinh tự động bằng AI như hướng dẫn tại Bài 2)*. |
| **2** | **Chạy kiểm tra tự động trước khi lưu:** Chọn nút <img src="https://api.iconify.design/lucide:check-square.svg?color=%23ff3333" width="16" alt="" /> **(Kiểm tra tính hợp lệ)**. **Nền tảng RedAI** sẽ tự động rà soát toàn bộ các trường dữ liệu, cấu hình bảo mật và đường dẫn để phát hiện xem có lỗi cú pháp hoặc thiếu sót nào không. |
| **3** | **Lưu và công bố:** Khi thanh kiểm tra hiển thị trạng thái hoàn hảo (100% hợp lệ), chọn nút <img src="https://api.iconify.design/lucide:save.svg?color=%23ff3333" width="16" alt="" /> **(Lưu và công bố)**. |

---

## Kiểm tra kết quả

Sau khi hoàn tất quy trình lưu, bạn kiểm tra ứng dụng mới tạo qua hai khu vực:

| Vị trí kiểm tra | Dấu hiệu nhận biết thành công |
| :--- | :--- |
| **Tại tab Nhà cung cấp tự tạo** | Ứng dụng mới xuất hiện ngay trên đầu danh sách, hiển thị đúng logo, tên hiển thị và huy hiệu màu xanh **Đã xuất bản (PUBLISHED)**. |
| **Tại Kho ứng dụng tích hợp (Catalog)** | Chuyển sang mục **Kho tích hợp**, phần mềm của doanh nghiệp bạn đã hiển thị như một thẻ dịch vụ chuyên nghiệp, sẵn sàng cho toàn thể nhân sự bấm nút kết nối sử dụng. |

---

## Hướng dẫn thao tác qua trợ lý ảo AI Agent

Bạn chỉ cần cung cấp tài liệu kỹ thuật hoặc địa chỉ máy chủ của phần mềm nội bộ vào khung trò chuyện, **trợ lý ảo AI Agent** sẽ tự động phân tích và khởi tạo trọn vẹn nhà cung cấp dịch vụ trên **nền tảng RedAI** cho bạn.

### Chuẩn bị kỹ năng (Skill) cho trợ lý ảo AI Agent

| Yêu cầu chuẩn bị | Chi tiết kiểm tra |
| :--- | :--- |
| **Kỹ năng cần kích hoạt (Skill)** | Kỹ năng Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `d5731aab-1a2b-48a6-a904-5dd84ec1d4bd`. |
| **Bộ công cụ sử dụng (Tool Suite)** | Bộ công cụ Quản lý Tích hợp (`RedAI - Module - Integration`). Mã ID: `ae8afc9a-1180-48d6-b672-d30171ccf3a6`. |
| **Quyền tài khoản** | Quyền Quản trị viên trong không gian làm việc. |

### Bảng liên kết thao tác giao diện và công cụ của trợ lý ảo AI Agent

| Thao tác trên giao diện | Công cụ trợ lý ảo AI Agent sử dụng | Nhiệm vụ của công cụ |
| :--- | :--- | :--- |
| Khởi tạo hồ sơ ứng dụng mới | `integration_provider_create` | Trợ lý ảo AI Agent tự động khai báo thông tin định danh, tên gọi đa ngôn ngữ, logo và phạm vi sử dụng. |
| Cập nhật phương thức bảo mật & ô nhập liệu | `integration_auth_strategy_upsert` | Trợ lý ảo AI Agent cấu hình chiến lược bảo mật (API Key, Bearer Token...) và tạo sẵn các ô nhập thông tin cho người dùng. |
| Kiểm tra an toàn trước khi công bố | `integration_provider_validation_validate` | Trợ lý ảo AI Agent tự động rà soát toàn diện cấu hình để đảm bảo không có lỗi cú pháp hoặc thiếu sót an toàn. |
| Thử nghiệm ký chữ ký số an toàn HMAC | `integration_auth_signing_test` | Trợ lý ảo AI Agent chạy thử thuật toán mã hóa chữ ký để đảm bảo tương thích tuyệt đối với máy chủ nội bộ. |

---

### Câu lệnh mẫu (Prompt mẫu)

> Sao chép câu lệnh dưới đây, cung cấp thông tin phần mềm nội bộ của bạn và gửi cho **trợ lý ảo AI Agent**:

```text
Hãy sử dụng kỹ năng Quản lý Tích hợp để giúp tôi tạo mới một nhà cung cấp dịch vụ tùy chỉnh:

1. Bối cảnh & Mục tiêu: Doanh nghiệp của tôi có phần mềm nội bộ tên là [Tên phần mềm, ví dụ: Phần mềm Quản lý Kho ABC] và muốn đưa lên Kho tích hợp của nền tảng RedAI để nhân viên kết nối sử dụng.
2. Dữ liệu cung cấp:
   - Tên hiển thị Tiếng Việt: [Tên Tiếng Việt]
   - Tên hiển thị Tiếng Anh: [Tên Tiếng Anh]
   - Danh mục nghiệp vụ: [Quản lý kho / Vận hành / Bán hàng]
   - Phương thức bảo mật: Sử dụng Mã khóa kết nối API truyền qua phần tiêu đề Header với tên Authorization.
   - Các ô thông tin cần người dùng điền: Địa chỉ máy chủ (server_url) và Mã khóa bảo mật (api_key).
3. Các bước yêu cầu:
   - Khởi tạo nhà cung cấp dịch vụ mới với các thông tin định danh trên.
   - Thiết lập cấu hình bảo mật và tạo các trường nhập liệu tương ứng.
   - Chạy công cụ kiểm tra tự động để đảm bảo cấu hình hoàn toàn chuẩn xác.
4. Yêu cầu phản hồi: Sau khi hoàn thành, hãy thông báo lại mã nhận diện của ứng dụng và tóm tắt các trường thông tin đã thiết lập cho tôi.
```

---

### Kiểm tra kết quả sau khi ra lệnh cho trợ lý ảo AI Agent

| Cách kiểm tra | Cách thực hiện | Dấu hiệu nhận biết thành công |
| :--- | :--- | :--- |
| **Kiểm tra trong khung chat** | Đọc báo cáo phản hồi của trợ lý ảo AI Agent. | Trợ lý ảo AI Agent thông báo khởi tạo thành công kèm bảng tóm tắt các trường cấu hình đã được kiểm tra tính hợp lệ 100%. |
| **Kiểm tra trên màn hình quản lý** | Mở tab Nhà cung cấp tự tạo trên nền tảng RedAI. | Ứng dụng mới xuất hiện ngay trên đầu danh sách và có thể bấm vào xem chi tiết cấu hình. |
